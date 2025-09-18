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
## Bundle 2
### Exercise 2
***
HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/bundle-2|MERGING)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/bundle-2|MERGING)
$ git commit -m "adding changes to README.md"
[ft/bundle-2 d2b5671] adding changes to README.md

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/bundle-2)
$ git pull origin main
From https://github.com/Blandus1/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Already up to date.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/bundle-2)
$ git push origin main
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/Blandus1/Gym-Git-Exercise-Solutio
hint: Updates were rejected because a pushed branch tip is behind its remote
hint: counterpart. If you want to integrate the remote changes, use 'git pull'
hint: before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 15, done.
Counting objects: 100% (15/15), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (9/9), 3.36 KiB | 860.00 KiB/s, done.
Total 9 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git  
 * [new branch]      ft/bundle-2 -> ft/bundle-2

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/bundle-2)

$ git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git pull
Auto-merging project/README.md
CONFLICT (content): Merge conflict in project/README.md
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main|MERGING)
$ git add README.md
fatal: pathspec 'README.md' did not match any files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main|MERGING)
$ git add README.md
fatal: pathspec 'README.md' did not match any files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main|MERGING)
$     git add README.md
fatal: pathspec 'README.md' did not match any files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main|MERGING)
$ git commit -a -m "Readme file"
[main 5ffd003] Readme file

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)       
$ git pull
Already up to date.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)       
$ git switch -c 
error: switch `c' requires a value

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)       
$ git switch -c 
error: switch `c' requires a value

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)       
$ git switch -c "ft/service-redesign"
Switched to a new branch 'ft/service-redesign'

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)       
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 887 bytes | 126.00 KiB/s, done.
From https://github.com/Blandus1/Gym-Git-Exercise-Solutions
   d7741b1..ae96401  main       -> origin/main
Auto-merging project/README.md
CONFLICT (content): Merge conflict in project/README.md
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main|MERGING)
$ git add README.md
fatal: pathspec 'README.md' did not match any files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main|MERGING)
$ git add .

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main|MERGING)
$ git commit -m "merging files"
[main 58642b9] merging files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git push origin main
Enumerating objects: 2, done.
Counting objects: 100% (2/2), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 393 bytes | 393.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
   ae96401..58642b9  main -> main

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git checkout ft/service-redesign 
Switched to branch 'ft/service-redesign'

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git pull 
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> ft/service-redesign


HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git pull origin main
From https://github.com/Blandus1/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Updating 5ffd003..58642b9
Fast-forward
 project/services.html |  13 ++++
 2 files changed, 193 insertions(+)
 create mode 100644 project/services.html

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git log
commit 58642b91a365eff216193cc9dea76b2aa270e865 (HEAD -> ft/service-redesign, origin/main, origin/HEAD, main)
Merge: 5ffd003 ae96401
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 15:24:24 2025 +0200

    merging files

commit ae964012e8a4a2f67eb3523117f5db2b90178d5a
Merge: d7741b1 d2b5671
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 15:22:29 2025 +0200

    Merge pull request #1 from Blandus1/ft/bundle-2

    Ft/bundle 2

commit 5ffd003622f2da103c49180be3a4724414f4b21f
Merge: 65d43dc d7741b1
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 14:53:11 2025 +0200

    Readme file

commit d2b5671fc3af196e99c0d69baf306e165d15b9b4 (origin/ft/bundle-2, ft/bundle-2)       
Merge: 367350a d7741b1
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 14:28:33 2025 +0200

    adding changes to README.md

commit 367350a10ebef2000408cac2f3b8c00794277e68
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 14:25:16 2025 +0200

    feature branch

commit 65d43dc487806222aae9e7e78878c0d7b24aac04
Merge: 03dfc5f 491a760
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 11:50:31 2025 +0200

    adding README.md file

commit d7741b1cd4948886ab491d6ea8982cd2b742ce9b
Merge: 03dfc5f 491a760
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 11:50:31 2025 +0200

    adding README.md file

commit 03dfc5f82231d9e5562f705caf49fe9e1c4202cf
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 11:45:33 2025 +0200

    adding  newly added files

commit 491a7601d27f527411cb5eec8af0595fac451ca8
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 11:06:55 2025 +0200

    adding a README file

commit 24db7972bd3dbcb9cfae58211ad01dc29e850421
Author: Blandus1 <blandine0045@gmail.com>
Date:   Thu Sep 18 10:33:35 2025 +0200

    creating files

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git commit --amend --no-edit
[ft/service-redesign d022440] merging files
 Date: Thu Sep 18 15:24:24 2025 +0200

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git push 
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git push origin ft/service-redesign
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 217 bytes | 217.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Blandus1/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git checkout main
M       project/services.html
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git commit -a -m "making changes to services file"
[main c5e34a1] making changes to services file
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 435 bytes | 25.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Blandus1/Gym-Git-Exercise-Solutions.git
   58642b9..c5e34a1  main -> main

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git pull origin main
From https://github.com/Blandus1/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Updating c5e34a1..35d5d5d
Fast-forward

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git checkout ft/
ft/bundle-2           ft/service-redesign

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git pull origin main
From https://github.com/Blandus1/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Updating d022440..35d5d5d
Fast-forward
 project/services.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-3TFO1V0 MINGW64 ~/OneDrive/Desktop/Git (ft/service-redesign)
$ git diff
***