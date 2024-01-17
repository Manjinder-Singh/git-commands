# git-commands
Git Commands for Beginners

# Demo
## Basic Git Commands

### Check version
git --version

git clone -b https://github.com/Manjinder-Singh/git-commands.git
Git and GitHub

Team's GitHub Repo
https://gitlabe2.ext.net.nokia.com/csf/co-op-student-projects.git

YouTube Video Doc https://gist.github.com/gwenf/19e5748a5391929e8e938a22c8a4b3f2

You Tube Video
https://www.youtube.com/watch?v=RGOj5yH7evk&t=905s
----------------------------------------------------------------------
YouTube Video Doc Commands
repo -> repository
clone -> bring a repo down from the internet (remote repository like Github) to your local machine
add -> track your files and changes with Git
commit -> save your changes into Git
push -> push your changes to your remote repo on Github (or another website)
pull -> pull changes down from the remote repo to your local machine
status -> check to see which files are being tracked or need to be commited
init -> use this command inside of your project to turn it into a Git repository and start using Git with that codebase
----------------------------------------------------------------------

ctrl + terminal shortcut for VS Code

0. git --version
1. git clone -b master "URL"
2. git status : Shows all of the files that were updated/deleted/created but haven't been saved to commit yet.
3. git add . : Tells git to track all of the files under untracked(new files) and modified(previous file updated) section displayed by git status command.
4. git commit -m "Message" -m "Some description"
5. git push : pushed code to online repo
or git push origin master

GIT PUSH

Now pushing a folder with file which is newly created locally to git hub after *

Inside the folder execute the commands that you are gonna push:
git init
git status
git add README.md (README.md - file added under new folder
git status
git commit -m "Created readme" -m "description"
git push origin master // gives error as repo is created locally not on git*

now create empty git repo on github
git remote add origin "ssh url which just above created"
git remote -v
git push -u origin master : here -u refers to that next time when we use only "git push" then it will automtically push  to master.

GIT WORKFLOW:
Write Code -----> Commit Changes -----> Make a pull request

Local Git Workflow:
Write Code ----> Stage Changes (git add) -----> Commit Changes (git commit) ----> Push Changes (git push) ----> Make  a pull request 

Making a pull request : Meaning we want others to review our code first then make changes then we need to make a pull request.

Git Branching:
git branch : q to get out of it and star sign shows the current brnach
git checkout -b feature-11-develop : switch between branches and if used -b means to create new branch and switch to new one.
git branch
git checkout master : switch to master branch
git branch
git checkout feature-11-develop
#Add changes to readme.md file.
git status
git add Readme.md
git commit -m "updated readme"
git checkout master
git diff feature-11-develop : use to compare the differeneces that is merging in from branch feature-11-develop to master branch.
**git merge feature-11-develop : Merge the changes but We dont do this instead create a PR.
git checkout feature-11-develop  : Push chnages to that branch on github and making a PR.
git status
git push : push upto github.  As you are on new branch " feature-11-develop " currently, you need to tell on which branch you are going to push 
answer is branch on github and the branch on local - which will be same for sure.

git push --set-upstream origin feature-readme-instructions
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









