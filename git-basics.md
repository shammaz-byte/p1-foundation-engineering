
shammaz-byte@shammaz-byte-Lenovo-V15-G4-AMN:~/git-practice$ cat git-basics.md 
# Git Basics Notes

## Git kyun?
Code ka backup rakhne ke liye aur alag-alag versions manage karne ke liye, taaki agar koi galti ho jaye toh purana sahi version wapas la sakein.

## 3 dabbe (apni picture/example)
- **Working Directory (Shelf):** Jahan hum file edit karte hain (table par saara samaan pada hai).
- **Staging Area (Cart):** Jahan hum chun kar woh cheezein rakhte hain jo commit karni hain.
- **Repository / .git (Diary):** Jahan final commits save ho kar permanent book ban jaati hai.

## Meri commands aur har ek kya karti hai
- Reinitialized existing Git repository in /home/shammaz-byte/git-practice/.git/: Naya .git folder banata hai (diary shuru karta hai).
- On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   notes.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	git-basics.md
	todo.txt

no changes added to commit (use "git add" and/or "git commit -a"): Batata hai ki abhi file ka kya haal hai (untracked, modified ya staged).
- : File ko cart (staging area) mein daalta hai.
- On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   notes.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	git-basics.md
	todo.txt

no changes added to commit (use "git add" and/or "git commit -a"): Cart ki cheezein diary (.git) mein save karta hai.
- commit b1a5ff33e43820f84e1f57081b8b68a5ed3a89be
Author: Shammaz Byte <shammaz.byte@gmail.com>
Date:   Mon Oct 19 18:35:37 2026 +0530

    test staging

commit 81e4d6c54fe658e0f4aaaa23637f7d7996704f97
Author: Shammaz Byte <shammaz.byte@gmail.com>
Date:   Mon Oct 19 18:31:20 2026 +0530

    add SNI note

commit 4f9c96ef0447fecd5118c0dfc8815fa50ca1c913
Author: Shammaz Byte <shammaz.byte@gmail.com>
Date:   Mon Oct 19 18:19:22 2026 +0530

    add new heading

commit c9c3e1a8b376ff80241e9b74121648373ec4e2ea
Author: Shammaz Byte <shammaz.byte@gmail.com>
Date:   Mon Oct 19 18:12:09 2026 +0530

    add TTL note

commit 83d5e50e05e9b92b7ad846e4bdfd94739fee13cc
Author: Shammaz Byte <shammaz.byte@gmail.com>
Date:   Mon Oct 19 17:39:20 2026 +0530

    Add first notes: Saare purane pages (commits) ki history dikhata hai.

## Aaj ki galti aur kaise theek ki
Maine bina  kiye seedha commit karne ki koshish ki thi jisse error aaya. Phir samajh aaya ki pehle file ko cart () mein daalna zaroori hai.

## 🔐 Security: history mein password kyun nahi jaata
Password safe nahi rehta agar commit ho jaye, kyunki .git diary mein har ek purana version permanent save ho jata hai. Line delete karne se sirf current file theek hoti hai, purane commit ka record nahi mitta.
shammaz-byte@shammaz-byte-Lenovo-V15-G4-AMN:~/git-practice$ 

