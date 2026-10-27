# HTTP and Proxy Notes

## 1. Request aur Response ke Hisse (Lab 1 Example)

Jab humne `curl -v http://127.0.0.1:8000/hello.txt` chalaya, toh uska structure kuch is tarah tha:

### Request Anatomy:
* **Request Line:** `GET /hello.txt HTTP/1.1` (Method = GET, Path = /hello.txt, Version = HTTP/1.1)
* **Headers:** 
  * `Host: 127.0.0.1:8000`
  * `User-Agent: curl/8.18.0`
  * `Accept: */*`
* **Khali Line:** Headers ke theek baad ek blank line hoti hai jo headers aur body ko alag karti hai (GET request mein body khali hoti hai).

### Response Anatomy:
* **Status Line:** `HTTP/1.0 200 OK` (Version = HTTP/1.0, Status Code = 200, Reason = OK)
* **Headers:**
  * `Server: SimpleHTTP/0.6 Python/3.14.4`
  * `Date: Tue, 20 Oct 2026 12:06:55 GMT`
  * `Content-type: text/plain; charset=utf-8`
  * `Content-Length: 6`
* **Khali Line:** Response headers ke baad blank line.
* **Body:** `hello` (sath mein ek invisible newline `\n` milkar total 6 bytes).
                                                                             
+## Burp intercept (23 Oct)
+1. Burp ek HTTP proxy tool hai jo browser aur server ke beech ke traffic ko intercept aur modify karne mein kaam aata hai.
+2. Intercept ON karne par request browser se nikal kar Burp mein ruk gayi, aur server tak tab tak nahi gayi jab tak forward na kiya.
+3. /hello.txt ko /badla.txt karne par server ne file na milne ki wajah se 404 Not Found diya.
+4. Attacker ke liye fayda ye hai ki wo request ke kisi bhi byte (headers, path, parameters) ko badal kar client-side limits ko bypass kar sakta hai.
+5. Defender ko client-side UI ya headers par bharosa nahi karna chahiye, balki server-side strict validation aur logic lagana chahiye.
