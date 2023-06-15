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

  

