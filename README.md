# git-commands
Git Commands for Beginners

### YouTube Video Document referred for learning
https://gist.github.com/gwenf/19e5748a5391929e8e938a22c8a4b3f2

### You Tube Video for learning / Reference
https://www.youtube.com/watch?v=RGOj5yH7evk&t=905s


# Demo
## Basic Git Commands

### Check version
git --version

### Cloning git Repo
git clone -b main https://github.com/Manjinder-Singh/git-commands.git


----------------------------------------------------------------------
### YouTube Video Doc Commands
1. repo -> repository
2. clone -> bring a repo down from the internet (remote repository like Github) to your local machine
3. add -> track your files and changes with Git
4. commit -> save your changes into Git
5. push -> push your changes to your remote repo on Github (or another website)
6. pull -> pull changes down from the remote repo to your local machine
7. status -> check to see which files are being tracked or need to be commited
8. init -> use this command inside of your project to turn it into a Git repository and start using Git with that codebase
----------------------------------------------------------------------

ctrl + terminal shortcut for VS Code to open Terminal.

### Practice Basic Git commands to push changes done on git directly if you have authorization.
0. git --version
1. git clone -b branch-name "URL"
git clone -b main https://github.com/Manjinder-Singh/git-commands.git

2. git status : Shows all of the files that were updated/deleted/ newly created but haven't been saved to commit yet.

3. git add . : Tells git to track all of the files under untracked(new files) and modified(previous file updated) section displayed by git status command.
or git add filename
git add . OR
git add index.html, README.md

4. git commit -m "Message" -m "Some description"
git commit -m "first commit" -m "updating changes to READEME.md and adding new file index.html"

5. git push : pushed code to online repo
or git push origin main

----------------------------------------------------------------------
### GIT PUSH AFTER CREATING A NEW FILE and FOLDER LOCALLY:

#### Now pushing a folder with file which is newly created locally to git hub after *

Inside the folder execute the commands that you are gonna push:
1. git init
2. git status
3. git add README.md (README.md - file added under new folder
4. git status
5. git commit -m "Created readme" -m "description"
6. git push origin main // gives error as repo is created locally not on github*

7. Now create empty git repo on github
8. git remote add origin "ssh url which just above created"
git remote add origin git@github.com:Manjinder-Singh/git-commands.git
9. git remote -v
10. git push -u origin main : here -u (means upstream) refers to that next time when we use only "git push" then it will automtically push to main.

----------------------------------------------------------------------
### GIT WORKFLOW:
Write Code -----> Commit Changes -----> Make a pull request

----------------------------------------------------------------------
### Local Git Workflow:
Write Code ----> Stage Changes (git add) -----> Commit Changes (git commit) ----> Push Changes to git repo (git push) ----> Make  a pull request 

----------------------------------------------------------------------
### Making a pull request 
#### Meaning we want others to review our code first then make changes then we need to make a pull request.

#### Git Branching:
1. git branch : q to get out of it and star sign shows the current brnach
2. git checkout -b feature-11-develop : switch between branches and if used -b means to create new branch and switch to new one.
3. git branch
4. git checkout main : switch to main branch
5. git branch
6. git checkout feature-11-develop

#### Add new changes to readme.md file.
1. git status
2. git add Readme.md
3. git commit -m "updated readme"
4. git checkout main
5. git diff feature-11-develop : use to compare the differeneces that is merging in from branch feature-11-develop to master branch.
**git merge feature-11-develop : Merge the changes but We dont do this instead create a PR.
6. git checkout feature-11-develop  : Push chnages to that branch on github and making a PR.
7. git status
8. git push : push upto github.  As you are on new branch " feature-11-develop " currently, you need to tell on which branch you are going to push 
answer is branch on github and the branch on local - which will be same for sure.

9. git push --set-upstream origin feature-readme-instructions
or
git push -u origin feature-readme-instructions : here -u means  --set-upstream origin

then online work. refer video

git checkout master : now master branch on github has latest chnages but not the local one.
git  pull origin master : use this command if upstream is not set but we already set above so we can use the blow command
git pull : updates to local branch
git branch : shows the branch named " feature-11-develop". Usally once the branch is merged we dont use so we will delete the " feature-11-develop" branch.
git branch -d  feature-11-develop
git branch

In real life multiple people update the same file, so merge will give conflicts. we resolve those chnages manually as we dont know which changes to keep.
git checkout -b quick-test
add things in index.html
git status : good to use this before commit
git diff
git add . : we wont use this as index file is already added to git. so we can use the below command
git commit -am "added world"   : Only works for modified files not for newly created files.
git checkout master 
now chnage line 2 in master branch in file index.html









