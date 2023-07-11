# Git exercises

This is the file where you can find all git project

- Bundle1: Exercise 1

´´´
PS C:\Users\User\Desktop\git-exercise> git init
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\User\Desktop\git-exercise> git add .
PS C:\Users\User\Desktop\git-exercise> git commit -m "initial project"
[main (root-commit) 1d12a27] initial project
 create mode 100644 readme.md
PS C:\Users\User\Desktop\git-exercise> git remote add origin https://github.com/Jmukakalisa/git-exercise.git
PS C:\Users\User\Desktop\git-exercise> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 300 bytes | 300.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      main -> main
PS C:\Users\User\Desktop\git-exercise> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\User\Desktop\git-exercise> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\User\Desktop\git-exercise> git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/dev
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      dev -> dev
PS C:\Users\User\Desktop\git-exercise> git checkout -b test
Switched to a new branch 'test'
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/test
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      test -> test
branch 'test' set up to track 'origin/test'.
PS C:\Users\User\Desktop\git-exercise> git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\User\Desktop\git-exercise> git branch -D test
Deleted branch test (was 1d12a27).
PS C:\Users\User\Desktop\git-exercise> 

´´´