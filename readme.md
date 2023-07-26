# Git exercises

This is the file where you can find all git project

- Bundle1: Exercise 1

´´´
git init
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
git add .
git commit -m "initial project"
[main (root-commit) 1d12a27] initial project
 create mode 100644 readme.md
git remote add origin https://github.com/Jmukakalisa/git-exercise.git
git push
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
git checkout -b dev
Switched to a new branch 'dev'
git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

upstream, see 'push.autoSetupRemote' in 'git help config'.
git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/dev
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      dev -> dev
git checkout -b test
Switched to a new branch 'test'
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/test
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      test -> test
branch 'test' set up to track 'origin/test'.
git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
git branch -D test
Deleted branch test (was 1d12a27).


´´´

- Bundle1: Exercise 2

```
git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)
git stash list 
git add home.html
git stash save homepage
Saved working directory and index state On main: homepage       
git stash list 
stash@{0}: On main: homepage
git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
git add about.html
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

git stash save about page
Saved working directory and index state On main: about page
git stash list
stash@{0}: On main: about page
stash@{1}: On main: homepage
git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
nothing added to commit but untracked files present (use "git add" to track)
git add team.html
git stash save team page
Saved working directory and index state On main: team page
git stash list
stash@{0}: On main: team page
stash@{1}: On main: about page
stash@{2}: On main: homepage
git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

git stash pop stash@{1}

error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index
```

```

$ git stash list
stash@{0}: On main: team page
stash@{1}: On main: about page
stash@{2}: On main: homepage


$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (47876c08cb574526400d97bad92fa6c4c2b13567)


$ git stash list
stash@{0}: On main: team page
stash@{1}: On main: homepage


$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (987164a6d0ed74ee3fe406545bacfea6a82c3121)


$ git add .


$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html



$ git commit -m "git exercises"
[main cd36c40] git exercises
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html


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


$ git stash list
stash@{0}: On main: team page


$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (3838284cf2167ee8825c55754717d8a6f50f18a6)


$ git reset --hard
HEAD is now at cd36c40 git exercises


$ git status
On branch main
Your branch is up to date with 'origin/main'.  

nothing to commit, working tree clean


```

# Bundle 2

- Bundle2 Exercise 1

```

$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'   
$ git branch
  dev
* ft/bundle-2   
$ git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.


$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2       
$ git add .       
$ git commit -m "dfghjk"
[ft/bundle-2 12a8759] dfghjk
 1 file changed, 11 insertions(+)
 create mode 100644 service.html       
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 620 bytes | 13.00 KiB/s, done.
From https://github.com/Jmukakalisa/git-exercise
 * branch            main       -> FETCH_HEAD
   723a473..efe3381  main       -> origin/main
Merge made by the 'ort' strategy.       
$ git log
commit 64d399d2770aedd410c6ffda14cd92bc2b8ec9c1 (HEAD -> ft/bundle-2)
Merge: 12a8759 efe3381       
$ git add .       
$ git reset --soft HEAD~1       
$ git commit -m "Bundle 2 exercise 1"
On branch ft/bundle-2
nothing to commit, working tree clean       
$ git add .       
$ git commit -m "Bundle 2 exercise 1"
On branch ft/bundle-2
nothing to commit, working tree clean       
$ git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.


$ git pull origin main
From https://github.com/Jmukakalisa/git-exercise
 * branch            main       -> FETCH_HEAD
Updating 50ba9c7..efe3381
Fast-forward


$ git status
On branch dev
Your branch is ahead of 'origin/dev' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean


$ git add .


$ git status
On branch dev
Your branch is ahead of 'origin/dev' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean


$ git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Jmukakalisa/git-exercise.git
   50ba9c7..efe3381  dev -> dev


$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'       
$ git pull origin main
From https://github.com/Jmukakalisa/git-exercise
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.


$ git status
On branch ft/bundle-2
nothing to commit, working tree clean


$ git add .


$ git commit -m "ft(): "bundle 2 exercise 1"
> git commit -m "ft(): bundle 2 exercise 1"
bash: syntax error near unexpected token `('


$ git commit -m "ft(): "bundle 2 exercise 1"
git commit -m "ft(): bundle 2 exercise 1"
bash: syntax error near unexpected token `('       
$ git commit -m "ft(): bundle 2 exercise 1"
[ft/bundle-2 75b468a] ft(): bundle 2 exercise 1
 1 file changed, 1 insertion(+)       
$ git status
On branch ft/bundle-2
nothing to commit, working tree clean       
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
       
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
$
```

- Bundle 2 Exercise 2

```

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)
$ git branch
  dev
* ft/bundle-2
  main

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 6 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 621 bytes | 124.00 KiB/s, done.
From https://github.com/Jmukakalisa/git-exercise
   e12d838..5fda5e5  main       -> origin/main
Updating 723a473..5fda5e5
Fast-forward
 readme.md    | 222 +++++++++++++++++++++++++++++++++++++++++++++++------------
 service.html |  12 ++++
 2 files changed, 190 insertions(+), 44 deletions(-)
 create mode 100644 service.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git commit  -m "ft(): new span element"
[ft/service-redesign ab7a212] ft(): new span element
 1 file changed, 1 insertion(+), 1 deletion(-)

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 322 bytes | 322.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/ft/service-redesign
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git add service.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git commit -m "main b changes"
[main 1982c69] main b changes
 1 file changed, 1 insertion(+), 1 deletion(-)

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 331 bytes | 331.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Jmukakalisa/git-exercise.git
   5fda5e5..1982c69  main -> main

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
M       readme.md
Your branch is up to date with 'origin/ft/service-redesign'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git diff
diff --git a/readme.md b/readme.md
index 85abdc5..e79e62c 100644
--- a/readme.md
+++ b/readme.md
@@ -370,4 +370,87 @@ To https://github.com/Jmukakalisa/git-exercise.git
  * [new branch]      ft/bundle-2 -> ft/bundle-2
 branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign|MERGING)
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign|MERGING)
$ git commit -m "ft(): merge main changes"
[ft/service-redesign 394304e] ft(): merge main changes

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$ git push
Enumerating objects: 10, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1.08 KiB | 555.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/Jmukakalisa/git-exercise.git
   ab7a212..394304e  ft/service-redesign -> ft/service-redesign

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/service-redesign)
$
```


### Bundle 3

- Bundle3 Exercise 1

```
mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/team-page)
$ git add team.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/team-page)
$ git commit -m "ft(): team page"
[ft/team-page cf12321] ft(): team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 436 bytes | 218.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/ft/team-page
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/team-page)
$ git log
commit cf12321ab00a7301f2197a614188fa19204302ca (HEAD -> ft/team-page, origin/ft/team-page)
Author: Jmukakalisa <j.mukakalis@alustudent.com>
Date:   Wed Jul 26 11:30:49 2023 +0200

    ft(): team page

commit 5fda5e564daf6d54aa1c99fb0869930e06d63dd5
Merge: e12d838 37a37d0
Author: Jmukakalisa <90443432+Jmukakalisa@users.noreply.github.com>
Date:   Thu Jul 13 14:47:18 2023 +0200

    Merge pull request #5 from Jmukakalisa/ft/bundle-2

    Ft/bundle 2

commit 37a37d03c1e290042b1296d20e63bfd94cd0c695 (origin/ft/bundle-2, ft/bundle-2)
Merge: c6329eb e12d838
Author: Jmukakalisa <j.mukakalis@alustudent.com>
Date:   Thu Jul 13 14:45:20 2023 +0200

    Merge branch 'main' of https://github.com/Jmukakalisa/git-exercise into ft/bundle-2
:...skipping...
commit cf12321ab00a7301f2197a614188fa19204302ca (HEAD -> ft/team-page, origin/ft/team-page)
Author: Jmukakalisa <j.mukakalis@alustudent.com>
Date:   Wed Jul 26 11:30:49 2023 +0200

    ft(): team page

commit 7710c1daf2da3316d04b51b82a0b8388072b0817 (origin/main, origin/HEAD, main, ft/contact-page)
Author: Jmukakalisa <j.mukakalis@alustudent.com>
Date:   Tue Jul 25 10:59:08 2023 +0200

    main b changes

commit 5fda5e564daf6d54aa1c99fb0869930e06d63dd5
Merge: e12d838 37a37d0
Author: Jmukakalisa <90443432+Jmukakalisa@users.noreply.github.com>
Date:   Thu Jul 13 14:47:18 2023 +0200

    Merge pull request #5 from Jmukakalisa/ft/bundle-2

    Ft/bundle 2

commit 37a37d03c1e290042b1296d20e63bfd94cd0c695 (origin/ft/bundle-2, ft/bundle-2)
Merge: c6329eb e12d838
Author: Jmukakalisa <j.mukakalis@alustudent.com>
Date:   Thu Jul 13 14:45:20 2023 +0200

    Merge branch 'main' of https://github.com/Jmukakalisa/git-exercise into ft/bundle-2

commit c6329ebb7459cab08ee7820b2cd2ad9246dc08d5
Merge: efe3381 d7c7c8a
Author: Jmukakalisa <90443432+Jmukakalisa@users.noreply.github.com>
Date:   Thu Jul 13 11:58:31 2023 +0200

    Merge pull request #3 from Jmukakalisa/ft/bundle-2

    Ft/bundle 2

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/contact-page)
$ git cherry-pick cf12321ab00a7301f2197a614188fa19204302ca
[ft/contact-page 62f5d64] ft(): team page
 Date: Wed Jul 26 11:30:49 2023 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/contact-page)
$ git add --all

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/contact-page)
$ git commit -m "ft(): Add contact page"
[ft/contact-page 32b4b14] ft(): Add contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 704 bytes | 352.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/ft/contact-page
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/faq-page)
$ git add .

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/faq-page)
$ git commit -m "ft(): Add FAQ"
[ft/faq-page 9da1ba1] ft(): Add FAQ
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 445 bytes | 222.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Jmukakalisa/git-exercise/pull/new/ft/faq-page
remote:
To https://github.com/Jmukakalisa/git-exercise.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/faq-page)
$ git revert 62f5d64abc6e6f17332192617801cd96ba9f4e20
[ft/faq-page 8a7c21d] Revert "ft(): team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 276 bytes | 276.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Jmukakalisa/git-exercise.git
   9da1ba1..8a7c21d  ft/faq-page -> ft/faq-page

mukak@Killer MINGW64 ~/OneDrive/Desktop/git-exercise (ft/faq-page)
$
```