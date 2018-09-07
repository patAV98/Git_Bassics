# GIT

## Some bassic commands

* *git init* initializes a repository in a folder. This creates a folder ‘.git’ file, which will safe certain info about the project, but it is not a backup. This file could be sent in order to grant access to the repository.
* *git status* provides info about current folders (untracked files, for instance).
* *git add* sets a file ready to be committed (files added will be now tracked). Must be used when changes have been applied to the afterwards committed folder. This is called STAGING. REMARK: ```git add .``` updates everything. ALSO: git rm --cached file removes file ‘file’ from the staged step.
* *git commit* commits. BUT: ```git commit -m ‘update statement’``` avoids intermediate steps. The addition step can be avoided IN ALREADY ADDED files through the command: ```git commit -a -m ‘update statement’```.
* *git log* lists commits history.
* *git branch <branch_name>*  creates a branch of the current. To switch to it: git checkout branch_name (git checkout master).
* *git merge name_of_branch* adds to the current branch we are in, the changes made in the specified branch.
* *git mergetool* ???
* *git stash* saves uncommitted but added changes in a certain branch.
* *git stash* apply restores the previously saved changes in the branch once you have returned without committing.

### GIT REMOTE

* *git remote* lists remote devices. REMARK: git remote -v shows remote devices with their url.
* *git clone <url>* exactly clones a remote repository.
* git fetch <remote_device> will get any changes since your last clone or fetch. Besides, it will pull it to your local repository but will not merge into your work.
* *git pull <remote_device>* will automatically pull and merge to your local repository every update in the remote repository.
* *git push <remote_device>* certain_branch will join the current work to the specified combination of repository and branch. BEWARE: this must be done after adding and committing in the local repository.
* *git remote add <repository_name> <url>* will add a new repository to the specified url.

### GIT CONFIG

* ```git config --global user.name ‘My Name Is’```
* ```git config --global user.email ‘myemailis@this.shit’```

## CREATING REMOTE BRANCHES

* First, you create your branch locally:
  ```git checkout -b <branch-name> # Create a new branch and check it out```
* The remote branch is automatically created when you push it to the remote server. So when you feel ready for it, you can just do:
  ```git push <remote-name> <branch-name>```
  
## IMPORTANT ISSUES

The name of the local branch must be the same as the one in the remote repo if something is to be pushed to it.
