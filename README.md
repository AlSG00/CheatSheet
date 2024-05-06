# Console basics

## Navigation
- **pwd** - _show current directory._
- **ls** - _show list of files and folders in the current directory._
- **cd** [directory] - _move to specified folder._
- **cd** .. - _move to parent folder._
- **cd** ~ - _move to home directory._
- **cd** / - _move to root directory._

## Working with files and folders

### Creating
- **touch** [filename] - _create file with specified name._
- **touch** [filename_1] [filename_2] ... - _create few files with specified names._
- **mkdir** [foldername] - _create directory ith specified name._

### Copying and moving
- **cp** [filename] [directory] - _copy specified file to a specified directory._
- **mv** [filename] [directory] - _move specified file to a specified directory._

### Reading
- **cat** [filename] - _read text file content._

### Removing
- **rm** [filename] - _remove specified file._
- **rmdir** [folder-name] - _remove specified directory._
- **rm -r** [directory] - _remove specified directory and all nested files and directories._

# Useful Features
* You do not have to type and execute commands in turn.<br>You can specify them by a list - divide by two ampersands (&&).
* The console has its own memory - a buffer with the last few commands.<br>They can be moved with up and down arrow keys.
* To avoid typing the name of a file or folder completely,<br>you can type the first name characters and double-click Tab.<br>If the file or folder is in the current directory,<br>the command line will add the path itself.

---

# Git basics

## Repository initialization
- **git init** - _initialise a repository._

## Synchronizing local and remote repositories
- **git remote add** origin [remote-repo-url] - _bind a local repository to a remote one with specified URL._
- **git remote -v** - _check if repos was really binded._
- **git push -u** origin main - _at first time, upload all the commits from a local repository to a remote one._
- **git push** - _upload commits to a remoted repository after it was binded with -u flag._

## Preparing file for a commit
- **git add** [filename]- _prepare specified file for commit._
- **git add --all** - _prepare all the new and modified files for commit._
- **git add .** - _prepare a current folder and all nested files for commit._

## Creating and publishing a commit
- **git commit -m** "[message]" - _make a commit and leave a commentary for easier understanding of what changes was made._
- **git push** - _add changes to remote repository._

## Checking informtaion about commits
- **git log** - _show detailed commit history._
- **git log --oneline** - _show brief information about commits: shortened hash and the message._

## Checking for files state
- **git status** - _show currrent repository state._

## Adding changes to last commit
- **git commit --amend --no-edit** - _add changes to a last commit and keep message the same._
- **git commit --amend -m** "[message]" - _replace message for a last commit with new [message]._

## Rollback files and commits
- **git restore --staged** [filename]- _change specified file from staged state to untracked or modified state._
- **git restore** [filename] - _return file to its last version that was saved via git commit or git add._
- **git reset --hard** [commit-hash]- _remove all the changes from workzone and staging zone and rollback them to a specified commit._

## Checking for changes
- **git diff** - _show the difference between modified files and last saved files._
- **git diff** [commit-hash-1] [commit-hash-2] - _show the difference between two commits._
- **git diff --staged** - _show the changes in staged files._

---

# Git branches

## Cloning someone's els repository
- **git clone** [remote-repo-url] - _clone specified remote repository on local machine._

## Branches creating
- **git branch** [branch-name] - _create a new branch called [branch-name] from the current._
- **git checkout -b** [branch-name] - _create a new branch called [branch-name] and switch to it._

## Navigating through branches
- **git branch** - _show available branches in a current repository._
- **git checkout** [branch-name] - _switch to a specified branch._

## Branches comparing
- **git diff main HEAD** - _show the difference between main branch and pointer to HEAD._
- **git diff HEAD~2 HEAD** - _sow the difference between the commit that was two commits ago and the current one._

## Branches removing
- **git branch -d** [branch-name] - _remove specified branch but only if it's part of the main branch._
- **git branch -D** [branch-name] - _remove specified branch even if it's not the part of the main branch._

## Branches merging
- **git merge** [branch-name] - _merge specified branch with current active branch._

## Working with remote repository
- **git push -u origin** [branch-name] - _push new branch to a remote repository and bind a local branch with a remote one, so for further commits and puashes you could use the command without -u._
- **git push** [branch-name] - _push aadditional changes to a specified branch, which is already exists in a remote repository._
- **git pull** - _download changes for a current branch from a remote repository._
