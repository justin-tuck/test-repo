# Git & Git hub - The Full Course

A fast-paced course for getting up to speed with git and github

## Basics

### Config

`git config --global user.name "User"`
`git config --global user.email "hello@gmail.com"`

`git config --list`

### Create a repository

`git init`

### Common

View the current status of a repo
`git status`

#### Add

Add an entire working directory to the staging area:
`git add .`

Add a file
`git add somefile.txt`

Remove a file from the staging area:
`git reset .`

#### Commit

Commit staged files to a repository
`git commit -m "initial commit 🚀"`

Add files and commit in a single command
`git commit -a -m "additional commit"`
`git commit -am "additional commit"`

view history of commits
`git log`

#### Remote

List current remotes in the local repo:
`git remote`

Create a new remote
`git remote add origin <url-to-your-github-repo>`

#### Push

`git push origin <branch name>`
-u flag is used to set origin as the upstream remote in your git config so git pull can be used without any arguments in the future.

#### Merge

get remote repositories
`git fetch`
merge that repository  
`git merge origin/master`

Combine the fetch & merge from the previous section with the pull command.
`git pull` need to do -u command first or specify remote branch `git pull origin <branch>`

View merge conflicts
`git diff`

Abort Merge
`git merge --abort`

#### clone

`git clone <repo-url> <local-directory>`

##### Forked

In order to get changes from upstream Add the remote
`git remote add upstream <original repo>`

Download the changes;
`git fetch upstream`

Add changes
`git rebase upstream/main `

#### Branch

list of all branches
`git branch`

rename your branch
`git branch -M <new name>`

Create a branch
`git branch <new branch name>`
`git checkout -b <new branch name>`

Delete a branch

`git branch -d <branch name>` Only will delete if it hasn't been merged into an origin
`git branch -D <branch name>` will delete no mater what

Switching branches
`git checkout <branch name>`

Checkout the previous branch you were on
`git checkout -`

### Trouble shooting

Remove a file from the staging area: (one that has been added)
`git reset .`

Go back to a previous commit without deleting previous state
`git reset <commit id>`

Go back to previous commit and delete commits after it
`git reset --hard <commit id>`

Note: never do a reset if you have already pushed if you remove it, it can be hard to reconcile the changes.

If you have a bad commit and have pushed you can Undo a commit with a new commit
`git revert <commit-ID> -m "reverting last commit"`

Change commit message

`git commit --amend -m "better message"`

Include a file you forgot on your last commit. (--no-edit means not changing the message)
`git add <your-file>`
`git commit --amend --no-edit`

Save your work without committing to repo with stash
`git stash list`
`git stash save <name>`
`git stash pop` takes the most recent stash
`git stash apply <index>`

Use git rebase to merge updates with a clean commit history
How to make your code look like your working from the latest commit?
`git rebase main`

If you want to squash your commits
`git rebase main --interactive`

replace <b>pick</b> with <b>squash</b>

Test
