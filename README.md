# learn_git

## Reading list

- https://rachelcarmena.github.io/2018/12/12/how-to-teach-git.html
- https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc
- https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
- https://datasift.github.io/gitflow/IntroducingGitFlow.html
- https://nvie.com/posts/a-successful-git-branching-model/

## First

0. Dev IDE (Visual Studio Code, ...)
1. Install GIT
    - https://git-scm.com/download/win
2. Change Config on path C:\Users\User\.gitconfig
    - git config --global user.email “petrujanTest@gmail.com”  
    - git config --global user.name "Jan Petru"

## What is git

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

Clone repository (Clone from "Remote repository" to "Working directory" and "Local repository"
1. git clone https://github.com/airbally/learn_git

### Make change

**Add, commit, push**

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
     6. git log --graph --decorate --pretty=oneline --abbrev-commit
 4. git push

### Branching

**Add branch**
    1. git branch [branchName]  //Add branch to "Local Repository". "Working area" and "Staging area" don't care. 
    2. git checkout develop //Switch bettween branches
        1. git checkout -b change_alice //Creates branch and switch to it
    3. git branch -a //list all branches
       1. git branch //list local
       2. git branch -r //list remote
    4. Change file created before and go ADD -> COMMIT -> PUSH

### Merging

**Merging branches**
    1. git checkout master
    2. git merge develop

## GIT FLOW

- https://nvie.com/posts/a-successful-git-branching-model/

1. Save way to merge
   1. git checkout master
   2. git pull origin master
   3. git merge [branch]
      1. git branch -d myfeature
   4. git push origin master
2. Suspecticting conflict in merge
   1. git checkout [branch]
   2. git pull
   3. git checkout master
   4. git pull
   5. git merge --no-ff --no-commit [branch]

3. Add branch
   1. git checkout [branch]
   2. git pull
      1. git fetch --all
      2. git pull
   3. git checkout -b [name]/[featureBranch]

### NEXT

- colisions
- cherry-picking
