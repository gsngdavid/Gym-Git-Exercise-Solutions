# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1

```bash
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions
$ git init
Initialized empty Git repository in C:/Users/gsngd/Documents/Gym-Git-Exercise-Solutions/.git/

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ echo "The branch is already called main by default"
The branch is already called main by default

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ echo "This is a test" > test.txt

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git add .
warning: in the working copy of 'test.txt', LF will be replaced by CRLF the next time Git touches it
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git commit -m "initial commit"
[main (root-commit) 0df72c0] initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git remote add origin https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git branch dev

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git switch dev
Switched to branch 'dev'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git branch test

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git switch dev
Already on 'dev'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git branch -d test
Deleted branch test (was 0df72c0).
```

### Exercise 2

```bash
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ touch home.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
Saved working directory and index state WIP on dev: 0df72c0 initial commit

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ touch about.hmtl

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ rm about.hmtl

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)
$ touch about.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
No local changes to save

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git add about.html 

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
Saved working directory and index state WIP on dev: 0df72c0 initial commit

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ touch team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git add team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
Saved working directory and index state WIP on dev: 0df72c0 initial commit

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (c9a55d0aec5aafa0f2162356d4098431ae08863e)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (8710265a403dc58299b7ca61c95c92080c628a6e)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git commit -m "Add about and home html file"
[dev cb5d1f5] Add about and home html file
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 528 bytes | 528.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/gsngdavid/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (2b29310c3a55c36b0ad72446fabb758572e8ac56)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git reset --hard
HEAD is now at cb5d1f5 Add about and home html file
```