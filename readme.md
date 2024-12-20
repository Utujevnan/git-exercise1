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

gymiribaii@Iribas-iMac-2 git-exercise1 % git push --set-upstream origin ft/service-redesig
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 737 bytes | 737.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesig' on GitHub by visiting:
remote:      https://github.com/Utujevnan/git-exercise1/pull/new/ft/service-redesig
remote: 
To https://github.com/Utujevnan/git-exercise1.git
 * [new branch]      ft/service-redesig -> ft/service-redesig
branch 'ft/service-redesig' set up to track 'origin/ft/service-redesig'.
'''
## BUNDLE 3
### EXERCISE 1
'''bash
Already up to date.
PS C:\Users\User\git-exercise1> git log
commit 8df18f22f6dd265181ab032423696630baeb11bf (HEAD -> ft/team-page, origin/ft/team-page)
Merge: 827ce8b 49489d2
Date:   Fri Dec 20 05:37:23 2024 +0200

     setup team.html page

commit 827ce8bcbbb0398d0a64a2ab60b2af50734c88d7
Author: Vanessa Utuje <utujevan@gmail.com>
PS C:\Users\User\git-exercise1> git checkout ft/contact-page
PS C:\Users\User\git-exercise1> git cherry-pick 8df18f22f6dd265181ab032423696630baeb11bf
error: commit 8df18f22f6dd265181ab032423696630baeb11bf is a merge but no -m option was given.
fatal: cherry-pick failed
PS C:\Users\User\git-exercise1> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\User\git-exercise1> git add --all
PS C:\Users\User\git-exercise1> git commit -m " setup team.html page"        
On branch ft/team-page
Your branch is up to date with 'origin/ft/team-page'.

PS C:\Users\User\git-exercise1> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\User\git-exercise1> git cherry-pick 8df18f22f6dd265181ab032423696630baeb11bf
error: commit 8df18f22f6dd265181ab032423696630baeb11bf is a merge but no -m option was given.
fatal: cherry-pick failed
PS C:\Users\User\git-exercise1> git cherry-pick -m 1 8df18f22f6dd265181ab032423696630baeb11bf
>>
On branch ft/contact-page
You are currently cherry-picking commit 8df18f2.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)        

The previous cherry-pick is now empty, possibly due to conflict resolution.  
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
PS C:\Users\User\git-exercise1> git commit --allow-empty
 Date: Fri Dec 20 05:37:23 2024 +0200
PS C:\Users\User\git-exercise1> git branch
  dev
  ft/bundle-2
* ft/contact-page
  ft/service-redesig
  main
  test
PS C:\Users\User\git-exercise1> git show
commit 7fb514d50ffd103f58922e8e354a1a8349345fcf (HEAD -> ft/contact-page)    
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 05:37:23 2024 +0200

     setup team.html page
PS C:\Users\User\git-exercise1> git push origin ft/contact-page
>>
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 433 bytes | 144.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:   
remote:      https://github.com/Utujevnan/git-exercise1/pull/new/ft/contact-page
remote:
To https://github.com/utujevnan/git-exercise1
 * [new branch]      ft/contact-page -> ft/contact-page
PS C:\Users\User\git-exercise1> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\User\git-exercise1> git log
commit 8df18f22f6dd265181ab032423696630baeb11bf (HEAD -> ft/team-page, origin/ft/team-page)
Merge: 827ce8b 49489d2
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 05:37:23 2024 +0200

     setup team.html page

commit 827ce8bcbbb0398d0a64a2ab60b2af50734c88d7
Author: Vanessa Utuje <utujevan@gmail.com>
PS C:\Users\User\git-exercise1> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\User\git-exercise1> 
 *  History restored 

PS C:\Users\User\git-exercise1> git cherry-pick -m 1 8df18f22f6dd265181ab032423696630baeb11bf
>>
On branch ft/contact-page
You are currently cherry-picking commit 8df18f2.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.  
If you wish to commit it anyway, use:


Otherwise, please use 'git cherry-pick --skip'
PS C:\Users\User\git-exercise1> ^C
PS C:\Users\User\git-exercise1> git commit --allow-empty
[ft/contact-page 2aa2cd6]  setup team.html page
 Date: Fri Dec 20 05:37:23 2024 +0200
PS C:\Users\User\git-exercise1> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\User\git-exercise1> git log
commit 8df18f22f6dd265181ab032423696630baeb11bf (HEAD -> ft/team-page, origin
/ft/team-page)
Merge: 827ce8b 49489d2
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 05:37:23 2024 +0200    

     setup team.html page

Author: Vanessa Utuje <utujevan@gmail.com>
PS C:\Users\User\git-exercise1> git checkout ft/contact-page
PS C:\Users\User\git-exercise1> git cherry-pick 8df18f22f6dd265181ab032423696630baeb11bf
error: commit 8df18f22f6dd265181ab032423696630baeb11bf is a merge but no -m option was given.
fatal: cherry-pick failed
PS C:\Users\User\git-exercise1> git cherry-pick -m 8df18f22f6dd265181ab032423696630baeb11bf
error: option `mainline' expects a number greater than zero
PS C:\Users\User\git-exercise1> git cherry-pick -m 1 8df18f22f6dd265181ab032423696630baeb11bf
On branch ft/contact-page
You are currently cherry-picking commit 8df18f2.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)        

nothing to commit, working tree clean

    git commit --allow-empty
Otherwise, please use 'git cherry-pick --skip'
PS C:\Users\User\git-exercise1> git checkout ft/team-page
Switched to branch 'ft/team-page'
warning: cancelling a cherry picking in progress
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\User\git-exercise1> git add team.html
PS C:\Users\User\git-exercise1> git commit -m "ft: add team page"
[ft/team-page 8fbdcfe] ft: add team page
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\User\git-exercise1> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 290 bytes | 145.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.        
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
To https://github.com/utujevnan/git-exercise1
   8df18f2..8fbdcfe  ft/team-page -> ft/team-page
PS C:\Users\User\git-exercise1> git log
commit 8fbdcfe4e2d96fc191260b5be733496a0f7bd49e (HEAD -> ft/team-page, origin/ft/team-page)
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 06:23:22 2024 +0200

    ft: add team page

commit 8df18f22f6dd265181ab032423696630baeb11bf
Merge: 827ce8b 49489d2
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 05:37:23 2024 +0200

     setup team.html page

commit 827ce8bcbbb0398d0a64a2ab60b2af50734c88d7
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 05:27:46 2024 +0200

     setup team.html page

commit 944dc348a720805f8c4bfe84c53445620eb774a5
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 04:55:58 2024 +0200

    added a team page in ft/team-page

commit 1711a80fadb8f0dd18f921dddd8f5651f2a3339b (origin/dev, dev)
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 04:39:02 2024 +0200

    added exercise2 bundle 2 description

commit 49489d2ca0e4478f1fe97de6a79c74838d739b93 (main)
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Fri Dec 20 03:40:22 2024 +0200

    edited a service page in the main branch

commit f628b222b0aaff677e02660211d848eccbbc6b6c (origin/main, origin/HEAD)   
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 19:59:03 2024 +0200

    setup of services page

commit de62bbf7e26f5c540f4e741057f99ffb1e6b4b02
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 19:53:41 2024 +0200

    setup services page

commit 0017aa5f4980e188851bd8aac0d34c9f2c5f47c9
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 19:50:46 2024 +0200

    setup services page

commit 75523603d86f0b9273dea64d17f80e0cddb53b26
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 19:31:58 2024 +0200

    added bundle 2 on readme

commit b795bdb413f7ab69a035d89d60fc0c4a9bcc9f31
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 19:28:07 2024 +0200

    added added bundle 2 on readme file

commit 5498adc06312446a2045ff4882a6935d3c58f0ce
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 19:22:00 2024 +0200

    added a service list

commit aaf4e703f4f1aa75462e09d65816a4165e27d234
Merge: e53f0a0 8a01c6a
Author: Utujevnan <utujevan@gmail.com>
Date:   Thu Dec 19 19:12:02 2024 +0200

    Merge pull request #4 from Utujevnan/ft/bundle-2

    created a page

commit 8a01c6a90ee2670b4cb23c6298cc02b89f1d8969 (origin/ft/bundle-2, ft/bundle-2)
Merge: 4cfdadf e53f0a0
Author: Utujevnan <utujevan@gmail.com>
Date:   Thu Dec 19 18:27:56 2024 +0200

    Merge branch 'main' into ft/bundle-2

commit 4cfdadffabbf80f645240a54ae29a390eb6c0673
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 17:36:52 2024 +0200

    created a page

commit e53f0a009bf884b1e33e109261f060306f724751
Merge: 0189e11 ace5954
Author: Utujevnan <utujevan@gmail.com>
Date:   Thu Dec 19 16:13:06 2024 +0200

    Merge pull request #3 from Utujevnan/ft/bundle-2

    created a sevices page

commit ace5954d6676c16570291b820fe5fe5b8ea8fc98
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 16:12:30 2024 +0200

    created a sevices page

commit 0189e11312b5f3963374821c2fc93d37b8e43944
Merge: 319dec5 67100e9
Author: Utujevnan <utujevan@gmail.com>
Date:   Thu Dec 19 15:44:25 2024 +0200

    Merge pull request #2 from Utujevnan/test

    added a readme file

commit 67100e97c2bd28fc17b8a038a75bc588fc6c206c (origin/test, test)
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 15:41:38 2024 +0200

    added a readme file

commit 319dec5dc024dd543368ca5c4ecc27027c299698
Merge: 780b8a0 9bf1be5
Author: Utujevnan <utujevan@gmail.com>
Date:   Thu Dec 19 13:54:09 2024 +0200

    Merge pull request #1 from Utujevnan/test

    Test

commit 9bf1be5fedf5506babd748aa252aaffe24dc120b
Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 13:44:24 2024 +0200

    about setup page

commit 1d406a399b303e334c9b657e17e861528c19756d

    Test

Author: Vanessa Utuje <utujevan@gmail.com>
Date:   Thu Dec 19 13:44:24 2024 +0200

    about setup page

commit 1d406a399b303e334c9b657e17e861528c19756d
PS C:\Users\User\git-exercise1> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\User\git-exercise1> fit cherry-pick 8fbdcfe4e2d96fc191260b5be733496a0f7bd49e
fit : The term 'fit' is not recognized as the name of a cmdlet, function, 
path was included, verify that the path is correct and try again.
At line:1 char:1
+ fit cherry-pick 8fbdcfe4e2d96fc191260b5be733496a0f7bd49e
+ ~~~
    + CategoryInfo          : ObjectNotFound: (fit:String) [], CommandNotFo  
   undException
    + FullyQualifiedErrorId : CommandNotFoundException
 
PS C:\Users\User\git-exercise1> git cherry-pick 8fbdcfe4e2d96fc191260b5be733496a0f7bd49e
Auto-merging team.html
error: could not apply 8fbdcfe... ft: add team page
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
hint: Disable this message with "git config advice.mergeConflict false"      
96a0f7bd49e
error: your local changes would be overwritten by cherry-pick.
hint: commit your changes or stash them to proceed.
fatal: cherry-pick failed
PS C:\Users\User\git-exercise1> git add --all
PS C:\Users\User\git-exercise1> git commit -m "resolved conflict"
[ft/contact-page 89508d9] resolved conflict
 Date: Fri Dec 20 06:23:22 2024 +0200
 1 file changed, 10 insertions(+)
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\git-exercise1> git push --set-upstream origin ft/contact-pagTo https://github.com/utujevnan/git-exercise1
 ! [rejected]        ft/contact-page -> ft/contact-page (fetch first)        
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not 
hint: have locally. This is usually caused by another repository pushing to  
hint: the same ref. If you want to integrate the remote changes, use
hint: See the 'Note about fast-forwards' in 'git push --help' for details.   
PS C:\Users\User\git-exercise1> git pull ft/contact-page
fatal: 'ft/contact-page' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
PS C:\Users\User\git-exercise1> git checkout ft/contact-page
Already on 'ft/contact-page'
PS C:\Users\User\git-exercise1> git pull ft/contact-page    
fatal: 'ft/contact-page' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\User\git-exercise1> git cherry-pick 8fbdcfe4e2d96fc191260b5be733496a0f7bd49e
On branch ft/contact-page
You are currently cherry-picking commit 8fbdcfe.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)        

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.  
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
unknown option: -D
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]   
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-l           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]   
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]
PS C:\Users\User\git-exercise1> git branch -D ft/team-page
Deleted branch ft/team-page (was 8fbdcfe).
PS C:\Users\User\git-exercise1> git branch -D ft/contact-page
error: cannot delete branch 'ft/contact-page' used by worktree at 'C:/Users/User/git-exercise1'
PS C:\Users\User\git-exercise1> git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use


To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\git-exercise1> git push origin --delete ft/team-page        
remote:   https://github.com/Utujevnan/git-exercise1.git
 - [deleted]         ft/team-page
PS C:\Users\User\git-exercise1> git checkout main
Switched to branch 'main'
warning: cancelling a cherry picking in progress
and have 1 and 16 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)     
Deleted branch ft/contact-page (was 89508d9).
PS C:\Users\User\git-exercise1> git push origin --delete ft/contact-page     
remote:   https://github.com/Utujevnan/git-exercise1.git
PS C:\Users\User\git-exercise1> git checkout - ft/team-page
error: pathspec '-' did not match any file(s) known to git
error: pathspec 'ft/team-page' did not match any file(s) known to git        
PS C:\Users\User\git-exercise1> git checkout - ft/team-page
error: pathspec '-' did not match any file(s) known to git
PS C:\Users\User\git-exercise1> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\User\git-exercise1> git add team.html
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

PS C:\Users\User\git-exercise1> git commit -m "ft: add team page"
[ft/team-page 58ed211] ft: add team page
 1 file changed, 10 insertions(+)
 create mode 100644 team.html
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\git-exercise1> ^C
PS C:\Users\User\git-exercise1> git push --set-upstream origin ft/team-page  
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 758 bytes | 252.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:      
remote:
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 1 and 16 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)     
PS C:\Users\User\git-exercise1> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\User\git-exercise1> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\User\git-exercise1> git log
/ft/team-page)
Author: Vanessa Utuje <utujevan@gmail.com>

    ft: add team page

commit 49489d2ca0e4478f1fe97de6a79c74838d739b93 (main, ft/contact-page)      
PS C:\Users\User\git-exercise1> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\User\git-exercise1> git cherry-pick 58ed2119931badbe2ea7c07b2ad49277a6cadf28
[ft/contact-page 8943f22] ft: add team page                                  277a6cadf28
 1 file changed, 10 insertions(+)
 create mode 100644 team.html
PS C:\Users\User\git-exercise1> git add --all
On branch ft/contact-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   contact.html

PS C:\Users\User\git-exercise1> git commit -m "ft: added contact page"       
[ft/contact-page bb7ab02] ft: added contact page
 1 file changed, 10 insertions(+)
 create mode 100644 contact.html
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\git-exercise1> git push --set-upstream origin ft/contact-page
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 1024 bytes | 170.00 KiB/s, done.
Total 9 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), done.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:   
age
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
PS C:\Users\User\git-exercise1> git checkout ft/contact-page
Already on 'ft/contact-page'
Your branch is up to date with 'origin/ft/contact-page'.
PS C:\Users\User\git-exercise1> git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
PS C:\Users\User\git-exercise1> git add faq.html
PS C:\Users\User\git-exercise1> git commit -m "ft: added an faq page"        
[ft/faq-page e7fbcd6] ft: added an faq page
 1 file changed, 10 insertions(+)
PS C:\Users\User\git-exercise1> git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\User\git-exercise1> git push --set-upstream origin ft/faq-page   
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 4 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 1.25 KiB | 142.00 KiB/s, done.
Total 12 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), done.
remote:   https://github.com/Utujevnan/git-exercise1.git
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:       
remote:
To https://github.com/utujevnan/git-exercise1
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
PS C:\Users\User\git-exercise1> git revert 58ed2119931badbe2ea7c07b2ad49277a6cadf28
[ft/faq-page f68d4fd] Revert "ft: add team page"
 1 file changed, 10 deletions(-)
 delete mode 100644 team.html
To https://github.com/utujevnan/git-exercise1
 ! [rejected]        ft/faq-page -> ft/faq-page (fetch first)
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not 
hint: have locally. This is usually caused by another repository pushing to  
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.   
To https://github.com/utujevnan/git-exercise1
 ! [rejected]        ft/faq-page -> ft/faq-page (fetch first)
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not 
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.   
PS C:\Users\User\git-exercise1> git pull ft/fq-page
fatal: 'ft/fq-page' does not appear to be a git repository

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\User\git-exercise1> git pull ft/faq-page
fatal: 'ft/faq-page' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
To https://github.com/utujevnan/git-exercise1
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: have locally. This is usually caused by another repository pushing to  
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.   
PS C:\Users\User\git-exercise1> git add --all
PS C:\Users\User\git-exercise1> git commit -m "ft: reverted the commits of team branch"
[ft/faq-page 5ed8a54] ft: reverted the commits of team branch
 1 file changed, 1 insertion(+), 1 deletion(-)
To https://github.com/utujevnan/git-exercise1
 ! [rejected]        ft/faq-page -> ft/faq-page (fetch first)
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not 
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.   
PS C:\Users\User\git-exercise1> git pull ft/faq-page
fatal: 'ft/faq-page' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\User\git-exercise1> git push
 ! [rejected]        ft/faq-page -> ft/faq-page (fetch first)
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not 
hint: have locally. This is usually caused by another repository pushing to  
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.   
PS C:\Users\User\git-exercise1> git push origin ft/team-page
>>
 ! [rejected]        ft/team-page -> ft/team-page (fetch first)
error: failed to push some refs to 'https://github.com/utujevnan/git-exercise1'
hint: Updates were rejected because the remote contains work that you do not 
hint: have locally. This is usually caused by another repository pushing to  
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.   
PS C:\Users\User\git-exercise1> git fetch origin
>>
remote: Counting objects: 100% (14/14), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 8 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)        
Unpacking objects: 100% (8/8), 2.99 KiB | 21.00 KiB/s, done.
From https://github.com/utujevnan/git-exercise1
   e7fbcd6..86219ac  ft/faq-page     -> origin/ft/faq-page
   bb7ab02..f26f0d5  ft/contact-page -> origin/ft/contact-page
   58ed211..b2cf499  ft/team-page    -> origin/ft/team-page
PS C:\Users\User\git-exercise1> git pull origin ft/faq-page
>>
From https://github.com/utujevnan/git-exercise1
 * branch            ft/faq-page -> FETCH_HEAD
Merge made by the 'ort' strategy.
 about.html    |   9 +
 services.html |  12 +-
 5 files changed, 541 insertions(+), 10 deletions(-)
 create mode 100644 .DS_Store
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\User\git-exercise1> git add --all
PS C:\Users\User\git-exercise1> git commit -m "ft: reverted the team commits"

On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 3 commits.

nothing to commit, working tree clean
PS C:\Users\User\git-exercise1> git add --all
PS C:\Users\User\git-exercise1> git status
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\User\git-exercise1> git push
Enumerating objects: 11, done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 853 bytes | 284.00 KiB/s, done.
Total 7 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.        
remote: This repository moved. Please use the new location:
remote:   https://github.com/Utujevnan/git-exercise1.git
To https://github.com/utujevnan/git-exercise1
   86219ac..0420cb7  ft/faq-page -> ft/faq-page
PS C:\Users\User\git-exercise1> git pull origin ft/faq-page
From https://github.com/utujevnan/git-exercise1
 * branch            ft/faq-page -> FETCH_HEAD
Already up to date.
PS C:\Users\User\git-exercise1> 
'''