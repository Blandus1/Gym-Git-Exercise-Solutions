# Git exercises
## Bundle 1
### exercise 1

***
$ git init
Initialized empty Git repository in C:/Users/HP/OneDrive/Desktop/Git/.git/

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (master)
$ git branch -m "main"

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git commit -m "creating files"
[main (root-commit) 24db797] creating files
 3 files changed, 21 insertions(+)
 create mode 100644 project/index.html
 create mode 100644 project/script.js
 create mode 100644 project/style.css

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git remote add origin https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git push -u origin main
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is 
behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so 
with:

    git branch --set-upstream-to=origin/<branch> main


HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git pull origin main
From https://github.com/Blandus1/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git push -u origin main --force
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (6/6), 609 bytes | 87.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
 + b5f9574...24db797 main -> main (forced update)
branch 'main' set up to track 'origin/main'.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git switch -c "dev"
Switched to a new branch 'dev'

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git switch -c "test"
Switched to a new branch 'test'

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (test)
$ git checkout dev
Switched to branch 'dev'

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git branch -d "test"
Deleted branch test (was 24db797).

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git commit -a -m "adding README.md file"
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        project/README.md

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git commit -m "adding README.md file"
[dev ebe35bc] adding README.md file
 1 file changed, 86 insertions(+)
 create mode 100644 project/README.md

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git push 
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git push -u origin main
branch 'main' set up to track 'origin/main'.
Everything up-to-date

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git reset --hard HEAD
HEAD is now at ebe35bc adding README.md file

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git status
On branch dev
nothing to commit, working tree clean

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git checkout dev
Switched to branch 'dev'

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git status
On branch dev
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    project/README.md

no changes added to commit (use "git add" and/or "git commit -a")

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git commit -m "adding a README file"
[main 491a760] adding a README file
 1 file changed, 7 insertions(+)
 create mode 100644 project/README.md

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 435 bytes | 217.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
   24db797..491a760  main -> main
***