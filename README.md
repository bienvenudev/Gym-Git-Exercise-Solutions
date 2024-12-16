# Bundle 1

## Exercise 1
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

 ## Exercise 2

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
