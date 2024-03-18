``` git config --global alias.stash 'stash --all' ```

``` git config --global alias.bb !better-branch.sh  ```

### conditional configs 
 ```
[includeIf "gitdir:~/projects/work/"]
  path = ~/projects/work/.gitconfig

[includeIf "gitdir:~/projects/oss/"] 
  path = ~/projects/oss/.gitconfig
 ```

### Blame
Showing authors of modified lines 
``` git blame -L 23,34 /path/to/file  ```

### Logs
Showing commit logs 
 ``` git logs -L 23,34:/path/to/file  ```

 
# Git Cheat Sheet

## Basic Commands

```bash
# Initialize a new Git repository
git init

# Clone a repository from a remote URL
git clone <remote-url>

# Add file(s) to the staging area
git add <file(s)>

# Commit changes with a message
git commit -m "Your commit message"


# Create a new branch
git checkout -b <branch-name>

# Switch to an existing branch
git checkout <branch-name>

# Merge changes from one branch into another
git merge <branch-name>


# View the status of files in the working directory
git status

# View the commit history
git log

# Undo changes in the working directory
git checkout -- <file(s)>
