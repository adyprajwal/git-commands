# A list of commonly used git commands.
---------------------------------------

### Git global setup

| Command | Description |
| ------- | ----------- |
| `git config --global user.name "[username]"` | Set global username |
| `git config --global user.email "[email]"` | Set global email |

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [new branch name]` | Rename a local branch (If you are on branch you want to rename)|
| `git branch -m [old branch name] [new branch name]` | Rename a local branch (If you are on a different branch) |
| `git push origin :[old branch name] [new branch name]` | Delete the old remote branch and push the new local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

-------------------------------
## Setting up projects with git
-------------------------------

### Create a new repository

| Command | Description |
| ------- | ----------- |
| `cd [new folder]` | Change working directory to new folder to be used as new git repo |
| `echo "# [title]" >> README.md` | Create README file with a title |
| `git init` | Initialize a local Git repository |
| `git add README.md` | Add the file "README.md" to the staging area |
| `git commit -m "add README"` | Commit changes with commit message "add README" |
| `git remote add origin https://github.com/[username]/[repository-name].git` | Add a remote repository |
| `git push -u origin master` | Push changes to remote repository (and remember the branch) |

### Create a new repository by cloning remote repository

| Command | Description |
| ------- | ----------- |
| `git clone https://github.com/[username]/[repository-name].git` | Create a local copy of a remote repository  |
| `cd [repository-name]` | Change working directory to the cloned repository |
| `touch README.md` | Create a README file |
| `git add README.md` | Add the file "README.md" to the staging area |
| `git commit -m "add README"` | Commit changes with commit message "add README" |
| `git push -u origin master` | Push changes to remote repository (and remember the branch) |

### Push existing folder to Github

| Command | Description |
| ------- | ----------- |
| `cd [existing-folder]` | Change working directory to the project folder |
| `git init` | Initialize a local Git repository |
| `git add .` | Add all changes to the staging area |
| `git commit -m "Initial commit"` | Commit changes with commit message "Initial commit" |
| `git remote add origin https://github.com/[username]/[repository-name].git` | Add a remote repository |
| `git push -u origin master` | Push changes to remote repository (and remember the branch) |

### Push existing Git repository to Github

| Command | Description |
| ------- | ----------- |
| `cd [existing-repository]` | Change working directory to the existing Git repository |
| `git remote add origin https://github.com/[username]/[repository-name].git` | Add a remote repository |
| `git push -u origin master` | Push changes to remote repository (and remember the branch) |

