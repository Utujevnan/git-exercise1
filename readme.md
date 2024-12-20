# GIT EXERCISES
## BUNDLE1

### EXERCISE1

'''bash 
gymiribaii@Iribas-iMac-2 git-exercise1 % git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 346 bytes | 346.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Utujevnan/git-exercise1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
gymiribaii@Iribas-iMac-2 git-exercise1 %  git push
Everything up-to-date
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout -b dev
Switched to a new branch 'dev'
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch dev
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

gymiribaii@Iribas-iMac-2 git-exercise1 % 
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

gymiribaii@Iribas-iMac-2 git-exercise1 % git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Utujevnan/git-exercise1/pull/new/dev
remote: 
To https://github.com/Utujevnan/git-exercise1.git
 * [new branch]      dev -> dev
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch -D test
error: branch 'test' not found.
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch -M test
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch -D test
error: Cannot delete branch 'test' checked out at '/Users/gymiribaii/git-exercise1'
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch -M dev
gymiribaii@Iribas-iMac-2 git-exercise1 % git status        
On branch dev
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch -M test
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch -D test
error: Cannot delete branch 'test' checked out at '/Users/gymiribaii/git-exercise1'
gymiribaii@Iribas-iMac-2 git-exercise1 % 
'''

### EXERCISE2
'''bash

gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
gymiribaii@Iribas-iMac-2 git-exercise1 % git add home.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git satus
git: 'satus' is not a git command. See 'git --help'.

The most similar command is
        status
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

gymiribaii@Iribas-iMac-2 git-exercise1 % git stash
Saved working directory and index state WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git add about.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash           
Saved working directory and index state WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git add team.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash
Saved working directory and index state WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
stash@{1}: WIP on test: 780b8a0 initiated project
stash@{2}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop stash@{2}
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped stash@{2} (e36212acb2ffffcdd731aebe8ae5513533fb98c3)
gymiribaii@Iribas-iMac-2 git-exercise1 % git add --all
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
stash@{1}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop stash@{1}:
fatal: 'stash@{1}:' is not a stash-like commit
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop stash@{1}
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (341c24770369878d874d2dd14435ef58b5822a58)
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped refs/stash@{0} (867641d24591ae5258931e245bcc96abe89acae0)
gymiribaii@Iribas-iMac-2 git-exercise1 % git add --all
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

gymiribaii@Iribas-iMac-2 git-exercise1 % git add team.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash
Saved working directory and index state WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git add --all
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git add home.html
fatal: pathspec 'home.html' did not match any files
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git add all
fatal: pathspec 'all' did not match any files
gymiribaii@Iribas-iMac-2 git-exercise1 % 
gymiribaii@Iribas-iMac-2 git-exercise1 % git add --all
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "setup home and about page"
On branch test
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git add home.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash
Saved working directory and index state WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
stash@{1}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git add about.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash
Saved working directory and index state WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git add team.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash
Saved working directory and index state WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
stash@{1}: WIP on test: 780b8a0 initiated project
stash@{2}: WIP on test: 780b8a0 initiated project
stash@{3}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash show stash@{3}
 about.html | 9 +++++++++
 home.html  | 9 +++++++++
 team.html  | 9 +++++++++
 3 files changed, 27 insertions(+)
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash show stash@{2}
 home.html | 9 +++++++++
 1 file changed, 9 insertions(+)
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash show stash@{1}
 about.html | 9 +++++++++
 1 file changed, 9 insertions(+)
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash show stash@{0}
 team.html | 9 +++++++++
 1 file changed, 9 insertions(+)
gymiribaii@Iribas-iMac-2 git-exercise1 % 
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash drop stash@{3}
Dropped stash@{3} (b56388afe95dd67985db03fc6669663a5079354f)
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
stash@{1}: WIP on test: 780b8a0 initiated project
stash@{2}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop stash@{2}
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped stash@{2} (2c2b3fa4b4cccf811830b33fa50d4ce55f0a1d6e)
gymiribaii@Iribas-iMac-2 git-exercise1 % git add home.tml
fatal: pathspec 'home.tml' did not match any files
gymiribaii@Iribas-iMac-2 git-exercise1 % git add home.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "setup home page"
[test 1d406a3] setup home page
 1 file changed, 9 insertions(+)
 create mode 100644 home.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop about.html
error: about.html is not a valid reference
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash show{1}
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token 'show{1}'
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash show stash@{2}
fatal: log for 'stash' only has 2 entries
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
stash@{1}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash show stash@{1}
 about.html | 9 +++++++++
 1 file changed, 9 insertions(+)
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop stash@{1}
On branch test
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (3c32cce3a2230852c8fd6a65935cf0c26999ad1c)
gymiribaii@Iribas-iMac-2 git-exercise1 % git add about.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "about setup page"
[test 9bf1be5] about setup page
 1 file changed, 9 insertions(+)
 create mode 100644 about.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
fatal: The current branch test has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin test

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

gymiribaii@Iribas-iMac-2 git-exercise1 % git add --all
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
fatal: The current branch test has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin test

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
stash@{0}: WIP on test: 780b8a0 initiated project
gymiribaii@Iribas-iMac-2 git-exercise1 % git push origin main
Everything up-to-date
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
fatal: The current branch test has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin test

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

gymiribaii@Iribas-iMac-2 git-exercise1 % git push --set-upstream origin test
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 696 bytes | 696.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Utujevnan/git-exercise1/pull/new/test
remote: 
To https://github.com/Utujevnan/git-exercise1.git
 * [new branch]      test -> test
branch 'test' set up to track 'origin/test'.
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash pop       
On branch test
Your branch is up to date with 'origin/test'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (ae931471ee5f3fa59473e885e97eb1241a60d7fc)
gymiribaii@Iribas-iMac-2 git-exercise1 % git reset --hard
HEAD is now at 9bf1be5 about setup page
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch -a
  main
* test
  remotes/origin/dev
  remotes/origin/main
  remotes/origin/test
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
Everything up-to-date
gymiribaii@Iribas-iMac-2 git-exercise1 % 
'''
## BUNDLE 2
### EXERCISE1
'''bash
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch ft/bundle-2
gymiribaii@Iribas-iMac-2 git-exercise1 % git add services.html
fatal: pathspec 'services.html' did not match any files
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git switch ft/bundle-2
Switched to branch 'ft/bundle-2'
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch ft/bundle-2
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git stash list
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch ft/bundle-2
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout test
Switched to branch 'test'
Your branch is up to date with 'origin/test'.
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch test
Your branch is up to date with 'origin/test'.

nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git restore home.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "restored a page"
On branch test
Your branch is up to date with 'origin/test'.

nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
Everything up-to-date
gymiribaii@Iribas-iMac-2 git-exercise1 % git restore services.html
error: pathspec 'services.html' did not match any file(s) known to git
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout !DOCTYPE html>
<html>
    <head>
        <title>Git Exercise | services</title>
    </head>
    <body>
        <h1>These are our services</h1>
    </body>
</html>
zsh: event not found: DOCTYPE
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout html>
<html>
    <head>
        <title>Git Exercise | services</title>
    </head>
    <body>
        <h1>These are our services</h1>
    </body>
</html>
zsh: parse error near `\n'
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout ft/bundle-2 
Switched to branch 'ft/bundle-2'
gymiribaii@Iribas-iMac-2 git-exercise1 % git restore services.html
error: pathspec 'services.html' did not match any file(s) known to git
gymiribaii@Iribas-iMac-2 git-exercise1 % git branch --contains services.html
error: malformed object name services.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git log --all -- git-exercise1/services.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git ls-files | grep git-exercise1/services.html

gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch ft/bundle-2
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout test
Switched to branch 'test'
Your branch is up to date with 'origin/test'.
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout dev
branch 'dev' set up to track 'origin/dev'.
Switched to a new branch 'dev'
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'
gymiribaii@Iribas-iMac-2 git-exercise1 % git add services.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "created a page"
[ft/bundle-2 4cfdadf] created a page
 1 file changed, 9 insertions(+)
 create mode 100644 services.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 397 bytes | 397.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Utujevnan/git-exercise1/pull/new/ft/bundle-2
remote: 
To https://github.com/Utujevnan/git-exercise1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
gymiribaii@Iribas-iMac-2 git-exercise1 % git fetch origin main
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 6 (delta 1), reused 3 (delta 1), pack-reused 0 (from 0)
Unpacking objects: 100% (6/6), 2.92 KiB | 597.00 KiB/s, done.
From https://github.com/Utujevnan/git-exercise1
 * branch            main       -> FETCH_HEAD
   780b8a0..e53f0a0  main       -> origin/main
gymiribaii@Iribas-iMac-2 git-exercise1 % git merge main
Already up to date.
gymiribaii@Iribas-iMac-2 git-exercise1 % git add .
git commit -m "Resolve merge conflicts"
git push origin ft/bundle-2

On branch ft/bundle-2
nothing to commit, working tree clean
Everything up-to-date
gymiribaii@Iribas-iMac-2 git-exercise1 % git push origin ft/bundle-2
Everything up-to-date
gymiribaii@Iribas-iMac-2 git-exercise1 % git status
On branch ft/bundle-2
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout ft/bundle-2
Already on 'ft/bundle-2'
gymiribaii@Iribas-iMac-2 git-exercise1 % git add .
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "Add or fix changes for services.html"
On branch ft/bundle-2
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git add .                                           
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "Add or fix changes for services.html"
On branch ft/bundle-2
nothing to commit, working tree clean
gymiribaii@Iribas-iMac-2 git-exercise1 % git push origin ft/bundle-2

Everything up-to-date
gymiribaii@Iribas-iMac-2 git-exercise1 % git merge main

Already up to date.
gymiribaii@Iribas-iMac-2 git-exercise1 % git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 7 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
gymiribaii@Iribas-iMac-2 git-exercise1 % git pull
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 967 bytes | 161.00 KiB/s, done.
From https://github.com/Utujevnan/git-exercise1
   4cfdadf..8a01c6a  ft/bundle-2 -> origin/ft/bundle-2
Updating 780b8a0..e53f0a0
Fast-forward
 about.html    |   9 +++
 home.html     |   9 +++
 readme.md     | 316 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 services.html |   9 +++
 4 files changed, 341 insertions(+), 2 deletions(-)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
gymiribaii@Iribas-iMac-2 git-exercise1 % git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 888 bytes | 888.00 KiB/s, done.
From https://github.com/Utujevnan/git-exercise1
   e53f0a0..aaf4e70  main       -> origin/main
Updating e53f0a0..aaf4e70
Fast-forward
 services.html | 9 ++++-----
 1 file changed, 4 insertions(+), 5 deletions(-)
 '''bash
 ### EXERCISE2
'''bash
ymiribaii@Iribas-iMac-2 git-exercise1 % git checkout -b ft/service-redesig 
Switched to a new branch 'ft/service-redesig'
gymiribaii@Iribas-iMac-2 git-exercise1 % git add --all
gymiribaii@Iribas-iMac-2 git-exercise1 % git commit -m "added a service list"
[ft/service-redesig 5498adc] added a service list
 2 files changed, 7 insertions(+), 1 deletion(-)
 create mode 100644 .DS_Store
gymiribaii@Iribas-iMac-2 git-exercise1 % git push
fatal: The current branch ft/service-redesig has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesig

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\git-exercise1> git branch contains services.html
fatal: not a valid object name: 'services.html'
Switched to branch 'ft/bundle-2'
Your branch is up to date with 'origin/ft/bundle-2'.
PS C:\Users\User\git-exercise1> git checkout main
Your branch is behind 'origin/main' by 16 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
Switched to branch 'main'
Your branch is behind 'origin/main' by 16 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
error: The following untracked working tree files would be overwritten by checkout:
        services.html
Please move or remove them before you switch branches.
Aborting
PS C:\Users\User\git-exercise1> git add services.html
PS C:\Users\User\git-exercise1> git commit -m "edited a service page in the main branch"
[main 49489d2] edited a service page in the main branch
 1 file changed, 14 insertions(+)
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\User\git-exercise1>
PS C:\Users\User\git-exercise1>
PS C:\Users\User\git-exercise1>
PS C:\Users\User\git-exercise1>
PS C:\Users\User\git-exercise1> git push origin
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the tip of your current branch is behind
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
Your branch is up to date with 'origin/ft/service-redesig'.
PS C:\Users\User\git-exercise1> git add services.html
PS C:\Users\User\git-exercise1> git commit -m "edited a service page in the main branch"
[ft/service-redesig f12f2d6] edited a service page in the main branch
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\User\git-exercise1> git push origin
Enumerating objects: 5, done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 303 bytes | 60.00 KiB/s, done.
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
To https://github.com/utujevnan/git-exercise1
   e47006b..f12f2d6  ft/service-redesig -> ft/service-redesig
PS C:\Users\User\git-exercise1> git add services.html
PS C:\Users\User\git-exercise1> git commit -m "edited a service page in the main branch"
[ft/service-redesig 311c58b] edited a service page in the main branch
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\User\git-exercise1> git push origin
Enumerating objects: 5, done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 306 bytes | 306.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
   f12f2d6..311c58b  ft/service-redesig -> ft/service-redesig
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
Your branch is up to date with 'origin/ft/service-redesig'.
PS C:\Users\User\git-exercise1> git merge
Already up to date.
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Already on 'ft/service-redesig'
Your branch is up to date with 'origin/ft/service-redesig'.
PS C:\Users\User\git-exercise1> git diff
PS C:\Users\User\git-exercise1> git diff main
diff --git a/.DS_Store b/.DS_Store
diff --git a/.DS_Store b/.DS_Store
index 0000000..eeea75b
Binary files /dev/null and b/.DS_Store differ
diff --git a/about.html b/about.html
new file mode 100644
index 0000000..206793e
--- /dev/null
+++ b/about.html
@@ -0,0 +1,9 @@
PS C:\Users\User\git-exercise1> git diff main services.html
>>
diff --git a/services.html b/services.html
index 604848f..b6d36b4 100644
--- a/services.html
diff --git a/services.html b/services.html
index 604848f..b6d36b4 100644
--- a/services.html
+++ b/services.html
@@ -5,7 +5,7 @@
         <title>Git Exercise | Services</title>
     </head>
     <body>
-        <h1>these are  our services</h1>   
+        <h1>here are  our services</h1>   
PS C:\Users\User\git-exercise1> git add services.html   
PS C:\Users\User\git-exercise1> git commit -m "solved a conflict"                       
[ft/service-redesig 5124575] solved a conflict
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\User\git-exercise1> git push origin  
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 292 bytes | 146.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
To https://github.com/utujevnan/git-exercise1
PS C:\Users\User\git-exercise1> git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 1 and 16 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
Your branch is up to date with 'origin/ft/service-redesig'.
PS C:\Users\User\git-exercise1> git diff main services.html
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
Your branch is up to date with 'origin/ft/service-redesig'.
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
  (use "git pull" if you want to integrate the remote branch with yours)
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
  (use "git pull" if you want to integrate the remote branch with yours)
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\User\git-exercise1> git checkout ft/service-redesig
Switched to branch 'ft/service-redesig'
PS C:\Users\User\git-exercise1> git diff main services.html
>>
Already up to date.
PS C:\Users\User\git-exercise1> ^C
PS C:\Users\User\git-exercise1> https://github.com/Utujevnan/git-exercise1/pull/6/#issue-2751775806^C
PS C:\Users\User\git-exercise1> ^C
PS C:\Users\User\git-exercise1> P^C
PS C:\Users\User\git-exercise1> git add readme.md
PS C:\Users\User\git-exercise1> git commit -m "added exercise2 bundle 2 description"
[ft/service-redesig af5aeaf] added exercise2 bundle 2 description
PS C:\Users\User\git-exercise1> git push origin
To https://github.com/utujevnan/git-exercise1
 ! [rejected]        ft/service-redesig -> ft/service-redesig (fetch first)
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\User\git-exercise1> git push
To https://github.com/utujevnan/git-exercise1
 ! [rejected]        ft/service-redesig -> ft/service-redesig (fetch first)
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
fatal: invalid gitfile format: readme.md
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\User\git-exercise1> git checkout dev
Switched to branch 'dev'
Your branch is ahead of 'origin/dev' by 16 commits.
PS C:\Users\User\git-exercise1> git pull origin
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 976 bytes | 31.00 KiB/s, done.
From https://github.com/utujevnan/git-exercise1
   5124575..cda73f6  ft/service-redesig -> origin/ft/service-redesig
Already up to date.
Unpacking objects: 100% (3/3), 976 bytes | 31.00 KiB/s, done.
From https://github.com/utujevnan/git-exercise1
   5124575..cda73f6  ft/service-redesig -> origin/ft/service-redesig
Already up to date.
PS C:\Users\User\git-exercise1> git push origin
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
To https://github.com/utujevnan/git-exercise1
   780b8a0..f628b22  dev -> dev
PS C:\Users\User\git-exercise1> git ^C
PS C:\Users\User\git-exercise1>





Unpacking objects: 100% (3/3), 976 bytes | 31.00 KiB/s, done.
From https://github.com/utujevnan/git-exercise1
   5124575..cda73f6  ft/service-redesig -> origin/ft/service-redesig
Already up to date.
PS C:\Users\User\git-exercise1> git push origin
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: This repository moved. Please use the new location:
From https://github.com/utujevnan/git-exercise1
   5124575..cda73f6  ft/service-redesig -> origin/ft/service-redesig
Already up to date.
PS C:\Users\User\git-exercise1> git push origin
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
To https://github.com/utujevnan/git-exercise1
   780b8a0..f628b22  dev -> dev
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
To https://github.com/utujevnan/git-exercise1
   780b8a0..f628b22  dev -> dev
   780b8a0..f628b22  dev -> dev
   '''