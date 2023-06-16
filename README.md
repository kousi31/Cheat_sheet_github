# Git commands

Git is a distributed version control system
### Configure Git

One can configure git at the system (for all users), global (for current user) or local (for current repository) level.

```
git config --global user.name typename
git config --global user.email typeemail
git config --global code.editor "code --wait"
git config --global code.autocrlf true
```
code.autocrlf is to configure the end-of-line. (type true for windows and input for mac)

### To open the default editor

```
git config --global -e
```
### Three stages of Git
  1. Working directory - Untracked and modified files are in the working directory
  2. Staging area - Where we organize the files for committing
  3. Repository - where committed files are stored

### Initializing git
  1. create a project directory
  2. `cd` to the project directory
  3. And type `git init` - a .git folder will be created. (check this with `ls -al`)

### Ignoring files 
If we want Git to ignore some private files and prevent them from committing:
  1. Create a .gitignore file with `touch .gitignore` command
  2. open the .gitignore file in a text editor and add a list of filenames to be ignored
  3. Add the .gitignore file to the staging area and commit (so that git will know the filenames to be ignored)

### Adding files to the staging area
`git add filename` - to add a single file  
`git add filename1 filename2` - to add multiple files  
`git add -A` - to add all modified files  

### Remove files from the staging area
`git reset filename` - to remove a single file
`git reset` - to remove all the files from the staging area

### First commit
`git commit -m "Initial commit"` use this command to commit. The text within double quotes is the description about the changes in the file
`git log` will give the details of the commits made

![image](https://github.com/kousi31/Cheat_sheets/assets/48381427/9b8df75d-a51f-4470-b912-5631c82d0fb4)

### Clone a remote repository
When you want to clone a remote repository (say one given by the company) and start developing on it:  
  `git clone <URL> <where to clone>`  

### Viewing the remote project
`git remote -v` gives the information about the remote repo
`git branch -a` gives details of the branches

### Committing changes to the remote repo
#### Committing locally 
`git diff` - shows the changes made to the file  
`git add modified-filename` - add the file to staging area  
`git commit -m "message"` - commit the change locally  

#### Committing remotely
`git pull origin main` - always pull before pushing changes to the remote repo (to see if others working on the repo made any changes)  
`git push origin main` - push changes to remote repo. origin is the name of the remote repo, main is the name of the branch  

### Creating a branch and working on it
`git branch branchname` - to create a branch  
`git checkout branchname` - to switch working to a desired branch  
`git branch -a` - lists the name of all branches in a repo. `*` indicates current working branch  

![image](https://github.com/kousi31/Cheat_sheets/assets/48381427/77246a9e-ca37-40a9-9af2-a05d1c1afd81)

#### make changes in a file and commit to local repo
`git add -A`  
`git commit -m "message"`   

#### commit to remote repo
`git push -u origin branchname` - this is for the first time. 
This will associate the branch in the local and remote repo. After this one can just use `git pull` or `git push`

### Merge a branch
To finally merge branches to the main branch:
1. checkout to the main branch in the local repo - `git checkout main`
2. pull the main branch from the remote repo to check for changes - `git pull origin main`
3. Merge the desired branch - `git merge --branchname`
4. check the branches merged so far - `git branch --merged`
5. push the changes to the main branch in the remote repo - `git push origin main`

### Delete a branch
1. `git branch -d branchname` - deletes the branch in the local repo
2. `git push origin --delete branchname` - deletes the branch in the remote repo
3. Finally check with `git branch -a`
