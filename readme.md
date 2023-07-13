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

- Bundle1: Exercise 2

```
C:\Users\mukak\OneDrive\Desktop\git-exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash list 
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git add home.html
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash save homepage
Saved working directory and index state On main: homepage       
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash list 
stash@{0}: On main: homepage
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git add about.html
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash save about page
Saved working directory and index state On main: about page
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash list
stash@{0}: On main: about page
stash@{1}: On main: homepage
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git add team.html
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash save team page
Saved working directory and index state On main: team page
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash list
stash@{0}: On main: team page
stash@{1}: On main: about page
stash@{2}: On main: homepage
PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS C:\Users\mukak\OneDrive\Desktop\git-exercise> git stash pop stash@{1}

error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS C:\Users\mukak\OneDrive\Desktop\git-exercise>

```

```

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git stash list
stash@{0}: On main: team page
stash@{1}: On main: about page
stash@{2}: On main: homepage

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (47876c08cb574526400d97bad92fa6c4c2b13567)

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git stash list
stash@{0}: On main: team page
stash@{1}: On main: homepage

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (987164a6d0ed74ee3fe406545bacfea6a82c3121)

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git commit -m "git exercises"
[main cd36c40] git exercises
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 539 bytes | 539.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Jmukakalisa/git-exercise.git
   d8d3fc6..cd36c40  main -> main

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git stash list
stash@{0}: On main: team page

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (3838284cf2167ee8825c55754717d8a6f50f18a6)

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git reset --hard
HEAD is now at cd36c40 git exercises

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.  

nothing to commit, working tree clean

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
```

# Bundle 2

- Bundle2 Exercise 1

```
mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)    
$ git branch
  dev
* ft/bundle-2

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)    
$ git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'
mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git commit -m "dfghjk"
[ft/bundle-2 12a8759] dfghjk
 1 file changed, 11 insertions(+)
 create mode 100644 service.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 620 bytes | 13.00 KiB/s, done.
From https://github.com/Jmukakalisa/git-exercise
 * branch            main       -> FETCH_HEAD
   723a473..efe3381  main       -> origin/main
Merge made by the 'ort' strategy.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git log
commit 64d399d2770aedd410c6ffda14cd92bc2b8ec9c1 (HEAD -> ft/bundle-2)
Merge: 12a8759 efe3381

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git reset --soft HEAD~1

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git commit -m "Bundle 2 exercise 1"
On branch ft/bundle-2
nothing to commit, working tree clean

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git commit -m "Bundle 2 exercise 1"
On branch ft/bundle-2
nothing to commit, working tree clean

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git pull origin main
From https://github.com/Jmukakalisa/git-exercise
 * branch            main       -> FETCH_HEAD
Updating 50ba9c7..efe3381
Fast-forward

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git status
On branch dev
Your branch is ahead of 'origin/dev' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git status
On branch dev
Your branch is ahead of 'origin/dev' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Jmukakalisa/git-exercise.git
   50ba9c7..efe3381  dev -> dev

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (dev)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git pull origin main
From https://github.com/Jmukakalisa/git-exercise
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)
$ git status
On branch ft/bundle-2
nothing to commit, working tree clean

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)
$ git commit -m "ft(): "bundle 2 exercise 1"
> git commit -m "ft(): bundle 2 exercise 1"
bash: syntax error near unexpected token `('

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)
$ git commit -m "ft(): "bundle 2 exercise 1"
git commit -m "ft(): bundle 2 exercise 1"
bash: syntax error near unexpected token `('

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git commit -m "ft(): bundle 2 exercise 1"
[ft/bundle-2 75b468a] ft(): bundle 2 exercise 1
 1 file changed, 1 insertion(+)

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git status
On branch ft/bundle-2
nothing to commit, working tree clean

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 864 bytes | 864.00 KiB/s, done.
Total 7 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 1 local object.      
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:    
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/ft/bundle-2
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)        
$
```