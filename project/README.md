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

###exercise2
***

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ cd project/

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git commit -m "adding home file"
[main daf9213] adding home file
 1 file changed, 12 insertions(+)
 create mode 100644 project/home.html

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash
No local changes to save

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git reset HEAD~1

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash
No local changes to save

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git reset --soft HEAD~1

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash
Saved working directory and index state WIP on main: 24db797 creating 

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash pop
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwa
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md
        new file:   home.html

Dropped refs/stash@{0} (9288a1dc8789075dbf3bcb8f10ad93c2ab0d2567)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git pull
Updating 24db797..491a760
error: Your local changes to the following files would be overwritten 
        project/README.md
Please commit your changes or stash them before you merge.
Aborting
$ git stash
Saved working directory and index state WIP on main: 24db797 creating n main: 24db797 creating files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)      /Git/project (main)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash
Saved working directory and index state WIP on main: 24db797 creating files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash
Saved working directory and index state WIP on main: 24db797 creating files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash list
stash@{0}: WIP on main: 24db797 creating files
stash@{1}: WIP on main: 24db797 creating files
stash@{2}: WIP on main: 24db797 creating files
~
~
~

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git log
commit 24db7972bd3dbcb9cfae58211ad01dc29e850421 (HEAD -> main)
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 10:33:35 2025 +0200

    creating files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash pop 0
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
                                             stage)
Dropped refs/stash@{0} (8da3f571cd7975a21fc8c60cd417799e4d2ae50b)
                                             60cd417799e4d2ae50b)
HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)                          /Git/project (main)
$ git stash pop 1
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md
        new file:   home.html
        new file:   team.html

Dropped refs/stash@{1} (ce7718bc273404ab4fe5ce4fcf30c459a8ba6c29)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash pop 2
fatal: log for 'refs/stash' only has 1 entries

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git stash pop
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped refs/stash@{0} (216b0e5a9ea1c2a4c9fc5d9ea3b3104160f4a406)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git commit -m "adding  newly added files"
[main 03dfc5f] adding  newly added files
 4 files changed, 206 insertions(+)
 create mode 100644 project/README.md
 create mode 100644 project/about.html
 create mode 100644 project/home.html
 create mode 100644 project/team.html

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git push
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git pull origin main --allow-unrelated-histories
From https://github.com/Blandus1/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Auto-merging project/README.md
CONFLICT (add/add): Merge conflict in project/README.md
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main|MERGING)
$ git add README.md 

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main|MERGING)
$ git commit -m "adding README.md file"
[main d7741b1] adding README.md file

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git/project (main)
$ git push -u origin main
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (8/8), 2.55 KiB | 870.00 KiB/s, done.
Total 8 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
   491a760..d7741b1  main -> main
branch 'main' set up to track 'origin/main'.

***