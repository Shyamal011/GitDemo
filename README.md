s1. git installation
====================
https://git-scm.com/

Git for Windows/x64 Setup.


git --version

2. Configure Git (First Time Setup)
========================

git config --global user.name "mvsanthi123"

git config --global user.email "mvsanthi.devops@gmail.com"

git config --list

mkdir gitdemo

cd gitdemo

git init

vim file1.txt(esc insert, escape:wq)

git add file1

git commit -m "First commit"

git status

git log


create a repo in GitHub like gitdemo(dont select the readme, keep it as public repo)


git branch

git branch -M main

git remote add origin https://github.com/mvsanthi123/gitdemo.git

git push -u origin main( for very first time it will ask authentication)

now add one more file as file2.txt and push it, now here it will not ask for origin add.

now add a file3.txt via git ui

now try to create one more file in local like file4.txt(vim file4.txt(esc insert, escape:wq), git add file4, git commit -m "Fourth commit")

git push -u origin main(throw u  an error like content mismatched, that time do git pull)

git pull origin main(here it will ask for commit message do that),now here if u hit ls then file3 also would have been came from remote to local.

git push -u origin main(now if u refresh the git hub page it will show you the file4 in in git ui)

how to change the branch
==========git =========
git branch----show u on which branch u are.

now create one branch in git ui like feature

git fetch-will fetch all branches to local, here if u do git branch also it will show  main only later u can switch the branch after that u hit like git branch then it will show both branches.

git checkout feature( when u run this at the prompt it will change from main to feature)



how to merge
=====================
create one file in feature branch locally-vim file5.txt

git add file5.txt

git commit -m "Added file5 in feature branch"

git push 

next change to main branch- git checkout main/git switch main

before merge-----git diff main feature

git merge feature

git push -u origin main//automatic merge will happen

for merge conflicts----
now modify file1 from both main and feature and push and try merge in main branch like git merge feature (will throw an error like merge conflicts and gives compare and pull request for first time, for second tie it will show u contribute option in feature there again go with compare and pull or else from locally how to do means git status, vim file3.txt---in this, keep only from feature and save it, git add ., git commit -m "conflict resolved", git push)  suppose if u did it in remote using pr then after that in main branch git merge --abort, so that from main|MERGE it will come back to main, now pull again. 

delete a file
=====================
in feature branch vim file6.txt, git add . ,git commit -m "file6", git push

git rm -rf file6.txt

git status

git add .

git commit -m "file6 is deleted"

git push origin feature


how to do PR-pull request-team based
===============================

now switch to feature branch-git checkout feature

team based pr ----before adding collaborator open the another GitHub account in incognito mode

how to add collaborators-go to repo, click on repo settings, when u add the user it will send one invite that they have to accept it---mvsanthi.devops18@gmail.com -->username i have to give during that time invitation will be sent ,pls accept that)


now create file7, add file7, commit file7 and push, now automatic merge will com when u raise pr.

to mandate pr-under setting of git repo go to branches and check the with out pr approve don't merge, target as main default branches, ruleset name, ruleset active), in this case git merge will be blocked.

git merge-from local how to merge

pr-from remote how to merge


git clone
=============
git clone https://github.com/mvsanthi123/simple-java-maven-app.git

git fork
===========
https://github.com/dnlnln/sql-server-samples/


removing origin
==================
git remote -v

git remote remove origin


git log
=============
shows commit ids along with commit messages, to come out esc:q


git diff
=======
before doing the git add, create one file and check the git diff. or git diff commitid1 commitid2 

git issues
============
show in UI

markdown formatting
==================
README.md
=============

# My Text Project

## Description
This project is about managing simple text files using Git.

## Features
- Create text files
- Edit content

## Project Structure
- file1.txt
- file2.txt
- README.md

## Commands Used
```bash
git add .
git commit -m "message"
git push

in feature after this git add . ,git commit -m "readme updated", git push.
