# Introduction to Git
---
### Key takeaways
1. What is Git
2. Why do we need Git?
3. Basic Git commands
---
## What is Git?
+++
### Git is a file version control tool.
  A version control tool is used for the following:
  1. Identify differences in versions
  2. Keep backups of previous versions
  3. Allow easy navigation to previous versions
  4. Syncing versions across local and remote repository.
  5. Manage and resolve version conflicts.
+++
### What is local and remote repository?
  A repository is basically a storage.
  Local refers to the files stored on your computer.
  Remote refers to the files stored on other computers.
---
## Why do we need Git?
+++
### As an individual
In coding, not all new versions of code will work as expected.
When that happens, you need to reference/ return to previous working versions, or check the history of changes made.
Git is a tool that allows easy version control.
However, the most common use case is ...
+++
### As a group
You'll have multiple people working on the same files. 
Each person has their own local version of the file, and their changes may conflict with your changes.
Git version control allows you to manage the conflicts that may arise to create a single merged file.

Additionally, with Github, you will have a central repository(storage) for your file versions remotely, 
which everyone can sync their versions with to get the latest versions.
+++
Now you know the What and Why, so it's time for the How.
---
## Basic Git Commands
Note: 
1. All the following commands are executed in the terminal
2. Remember where you are located in the terminal (check using pwd)
+++
### git init
Set up git for a particular folder of files. 
+++
Usage:
I want to set up git for the files in my_project folder:
```
- my_project
  - app.js
```
1. Go to into the folder (make sure you're in the right location)
```sh
cd my_project
```
2. Call git init
```sh
git init
```
Now you can start using git!
+++
### git status
Checks for changed, untracked, uncommited files.
+++
Usage:
In your my_project folder, run 
```sh
git status
```
You will see that all your files are currently untracked.
+++ 
### git clone <link>
Copy an existing project from Github
+++
Usage:
Create a test repository on your github account. Obtain the link to clone.
```sh
git clone <link>
```
This will copy the folder and paste it at the location your terminal is in within the computer.
+++
### git add <file>
Start tracking file changes for a particular file
+++
Usage:
In my_project folder:
```sh
git add app.js
```
If you type `git status` now, it will show you that it is currently tracked, but not your saved into your versions.
Additionally, you can call `git add .` to track all files in my_project.
+++
### git commit -m "<message>"
Saves the file version into your git history.
+++
Usage:
Once you've git added your files, you can run the command
```sh
git commit -m "first commit"
```
This will commit your changes as changes under the version with the message "first commit".
If you run `git status` now, there are no changes detected.
+++
### git log
Shows the history of all git commits
+++
Usage:
Run
```sh
git log
```
This will show a list of all the versions and messages in your git history.
+++
### git remote add <remote> <link>
Adds a reference to your local repository for the remote repository
+++
Usage:
This will create a link between your local files with the remote files to make it easier to sync versions.
```
git remote add origin <your link>
```
`origin` is the name we set for your particular link, which we will use to reference which remote repository.
+++
### git push <remote> <branch>
Pushes the file changes to the remote repository
+++
Usage:
Once you've added and commited your changes, you can update your github remote repository with your new changes.
```sh
git push origin master
```
This will push your local changes to the remote repository located on the `origin` we set in the previous step. 
+++
`master` is the default main branch of all repositories. For now, you won't need to know too much about branches, just that when you want to edit your remote repository, make it edit the master branch.
Know that editting the master branch directly is not good practice, but it is acceptable for now as a beginner.
