# learn_git

## Reading list
- https://rachelcarmena.github.io/2018/12/12/how-to-teach-git.html
- https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc


## First 
0. Dev IDE (Visual Studio Code, ...)
1. Install GIT 
    1. https://git-scm.com/download/win
2. Change Config on path C:\Users\User\.gitconfig
    1. git config --global user.email “petrujanTest@gmail.com”  
    2. git config --global user.name "Jan Petru"


## What is git?
"Git is a distributed version-control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows."

- https://rachelcarmena.github.io/2018/12/12/how-to-teach-git.html
- https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc

- **Server**
    - Remote repository
- **Dev environment**
    - Local repository
    - Staging area
    - Working directory

## Try

### Clone
3. Clone repository (Clone from "Remote repository" to "Working directory" and "Local repository"
    1. git clone https://github.com/airbally/learn_git

### Make change
3. Add, commit, push
    1. Create file
        1. mkdir test01_[yourName]
        2. create File
        3. git status
        4. git diff [file]
    2. git add [file]
        1. git diff --name-only --cached //changes between the index and your last commit and Show only names of changed files.
        2. git add file-name-1 file-name-2 file-name-3
    3. git commit -m "message"
        1. git log --pretty=oneline
        2. git log --pretty=format:"%h - %an, %ar : %s"
        3. git log --pretty=format:"%h %an %s" --graph //Display an ASCII graph of the branch and merge history beside the log output.
        4. git log --pretty=format:"%h %an %s"  --stat  //Show statistics for files modified in each commit.
        5. git log --since=2.weeks
    4. git push 

### Branching
4. Add branch
    1. git branch [branchName]  //Add branch to "Local Repository". "Working area" and "Staging area" don't care. 
    2. git checkout develop //Switch bettween branches

## GIT FLOW
1. Add branch
2. Make changes
3. 

https://dev.to/bdbch/setting-up-ssh-and-git-on-windows-10-2khk
