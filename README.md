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