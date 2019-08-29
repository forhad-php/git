Git Commands
============

_A list of my commonly used Git commands_

-->

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
| `git commit -m "first line" -m "second line" -m "third line"` | Multiline commit message |
| git commit -a -m "message" | Git add and commit in one command |
| `git rm -r [file-name.txt]` | Remove a file or folder. `r` for using recursive command. To remove a folder inside another folder `git rm -r [parentFolder/childFolder]` |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branchName]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash list` | View a list of stashed changes |
| `git stash clear` | Remove all stashed entries |

> Situation : Rename a Git branch locally and remotely..

| Command | Description |
| ------- | ----------- |
| `git branch -m [old_name] [new_name]` | move locally |
| `git push origin -u [new_name]` | -u to set upstream is optional, it configure the new local branch to track the pushed one |
| `git push origin -d [old_name]` | delete finally |

> Merge conflict issue :

| Command | Description |
| ------- | ----------- |
| `git pull/merge origin [branch-name] --allow-unrelated-histories` | to merge the disparate branches which is now disabled by default in git but can be enabled with the `--allow-unrelated-histories` flag. Error look like `fatal: refusing to merge unrelated histories` |
| `git checkout --ours/--theirs directory_name/*` | `--ours` to Accept Current Change, and for `--theirs` to Accept Incoming Change. `directory_name/*` to accept all file in the name of directory(multiple purpose) |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin git@github.com/[username]/[repository-name].git` | Add a new remote |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes. (type `q` to exit from git log screen) |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch]` | Preview changes before merging |
