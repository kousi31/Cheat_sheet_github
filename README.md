# Git commands

Git is distributed version control system
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
  2. Staging area - Where we organise the files for commiting
  3. Repository - 
