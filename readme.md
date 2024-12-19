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

