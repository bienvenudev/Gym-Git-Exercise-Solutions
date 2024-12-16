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