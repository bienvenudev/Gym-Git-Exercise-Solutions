# Bundle 1

## #1 Exercise 1
```bash
cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions
$ git init
Initialized empty Git repository in C:/Users/cbien/Documents/The-Gym/Gym-Git-Exercise-Solutions/.git/

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (master)
$ git add .

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (master)
$ git commit -m 'create readme file'
[master (root-commit) 3cca6c9] create readme file
 1 file changed, 3 insertions(+)
 create mode 100644 README.md

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (master)
$ git branch -M main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git remote add origin https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean        

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git branch
* dev
  main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git branch test

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git branch
* dev
  main
  test

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git branch -d test
Deleted branch test (was 3cca6c9).

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git branch
* dev
  main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/bienvenudev/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
 ```

 ## #1 Exercise 2

```bash
cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git add home.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash push -m "add home file"
Saved working directory and index state On dev: add home file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: On dev: add home file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git statu
git: 'statu' is not a git command. See 'git --help'.

The most similar commands are
        status
        stage
        stash

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git add about.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash push -m "add about file"
Saved working directory and index state On dev: add about file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: On dev: add about file
stash@{1}: On dev: add home file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git add team.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash push -m "add team file"
Saved working directory and index state On dev: add team file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: On dev: add team file
stash@{1}: On dev: add about file
stash@{2}: On dev: add home file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (e2c083ff1db37a3fbf276c7bb2edcc2ad4b42899)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{2}
fatal: log for 'stash' only has 2 entries

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (7bf34f3a25ec2638dc13af3a4be7e6f83424d039)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git commit -m "add about page and home page file"
[dev dd32379] add about page and home page file
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git push -u origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 529 bytes | 264.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git
   8cb5a06..dd32379  dev -> dev
branch 'dev' set up to track 'origin/dev'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: On dev: add team file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (bdec4e8874b26335ef5f9a15397ea13b0497f4a1)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git log --oneline
dd32379 (HEAD -> dev, origin/dev) add about page and home page file
8cb5a06 (checkout) delete
9612e5d add bundle#1 exercise 1
3cca6c9 create readme file

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git reset --hard
```
# Bundle 2

## #2 Exercise 1

```bash
cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git branch
* ft/bundle-2
  dev
  main
  
cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git add services.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m 'add services page'
[ft/bundle-2 75111be] add services page
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git push -u origin ft/bundle-2 
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 4 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (12/12), 1.87 KiB | 382.00 KiB/s, done.
Total 12 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), done.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/bienvenudev/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```
## #2 Exercise 2
```bash

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ma$ git checkout main
Your branch is up to date with 'origin/main'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ma$ git pull
Already up to date.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ma$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ftrvice-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ftrvice-redesign)
$ git add services.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ftrvice-redesign)
$ git commit -m "add service redesigning"
[ft/service-redesign 1d7ce17] add service redesigning
 1 file changed, 1 insertion(+)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ftrvice-redesign)
$ git push -u origin ft/service-redesign 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 332 bytes | 332.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
esign' on GitHub by visiting:
remote:      https://github.com/bienvenudev/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git       
 * [new branch]      ft/service-redesign -> ft/service-redesign        
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

es in working directory)        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")      

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git add services.html

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git commit -m "add new services before redesign"
[main 32b2198] add new services before redesign
 1 file changed, 1 insertion(+)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 352 bytes | 352.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.  
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git       
   dd66c5e..32b2198  main -> main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign 
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff main ft/
ft/bundle-2           ft/service-redesign   

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff main ft/service-redesign 
diff --git a/services.html b/services.html
index 16c0310..e24a9bf 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
   </head>
   <body>
     <h1>Our Services</h1>
-    <p>New Services Before Redesigning</p>
+    <p>Service Redesigning</p>
   </body>
 </html>

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git add services.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git commit -m "merge services and main"
[ft/service-redesign fc2d241] merge services and main

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push -u origin ft/service-redesign 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 338 bytes | 338.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git
   1d7ce17..fc2d241  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
```

# Bundle 3
## #3 Exercise 1
```bash
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what wi
        team.html

nothing added to commit but untracked files presrack)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/team-page)
$ git add team.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/team-page)
$ git commit -m "add team page file"
[ft/team-page 7ff5b69] add team page file
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/team-page)
$ git push -u origin ft/team-page 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 430 bytes | 430.00 
Total 3 (delta 1), reused 0 (delta 0), pack-reus
remote: Resolving deltas: 100% (1/1), completed 
remote:
remote:
To https://github.com/bienvenudev/Gym-Git-Exerci
 * [new branch]      ft/team-page -> ft/team-pag
branch 'ft/team-page' set up to track 'origin/ft

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Gitin)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/contact-page)
$ git checkout ft/team-page 
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-p

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/team-page)
$ git log
commit 7ff5b69c0f449defca379770707edc6b6b508265 
origin/ft/team-page)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Dec 17 12:25:01 2024 +0200

    add team page file

commit 52296935bc8cf31caf2064a2c73c33d0feddef0e contact-page)
Author: bienvenudev <cbienvenu007@gmail.com>
Date:   Tue Dec 17 12:10:11 2024 +0200

    add bundle 2 exercise 2

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git/team-page)
Switched to branch 'ft/contact-page'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/contact-pse-Solutions (ft/contact-page)                         265
$ git cherry-pick 7ff5b69c0f449defca379770707edc6b6b508265
[ft/contact-page fa9c268] add team page file
 Date: Tue Dec 17 12:25:01 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html                          se-Solutions (ft/contact-p

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git status
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contact.html

nothing added to commit but untracked files present (use "git add" to track)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add contact.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m "add contact page"
[ft/contact-page 03f54dd] add contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push -u origin ft/contact-page 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 698 bytes | 349.00 KiB/s, 
done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 
local object.
remote:
remote: Create a pull request for 'ft/contact-page' on 
GitHub by visiting:
remote:      https://github.com/bienvenudev/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-pagebranch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add faq.html 

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "add faq html page"
[ft/faq-page 5c38bd2] add faq html page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push -u origin ft/faq-page 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 441 bytes | 441.00 KiB/s, 
done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 
local object.
remote: 
 by visiting:                                             by visiting:
remote:      https://github.com/bienvenudev/Gym-Git-Exercise-Solutions/pull/new/fise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.gitons.git
 * [new branch]      ft/faq-page -> ft/faq-page          .
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'e'.                                                      -Solutions (ft/faq-page)

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercisese-Solutions (ft/faq-page)
$ git revert 7ff5b69c0f449defca379770707edc6b6b508265    
[ft/faq-page 9b3a3b9] Revert "add team page file"      
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercisese-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)       

nothing to commit, working tree clean

cbien@HP-321 MINGW64 ~/Documents/The-Gym/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
To https://github.com/bienvenudev/Gym-Git-Exercise-Solutions.git
   5c38bd2..9b3a3b9  ft/faq-page -> ft/faq-page
   ```