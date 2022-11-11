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

#### clone

`git clone <repo-url> <local-directory>`

#### Branch

list of all branches
`git branch`

rename your branch
`git branch -M <new name>`
