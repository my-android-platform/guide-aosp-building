# Guide for using repo

## Repo source code
**Link:** [git-repo](https://gerrit.googlesource.com/git-repo/)

## Installing
```bash
mkdir ~/bin
PATH=~/bin:$PATH
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo
```

## Basic commands
###### repo help
```bash
abandon        Permanently abandon a development branch
branch         View current topic branches
branches       View current topic branches
checkout       Checkout a branch for development
cherry-pick    Cherry-pick a change.
diff           Show changes between commit and working tree
diffmanifests  Manifest diff utility
download       Download and checkout a change
gitc-delete    Delete a GITC Client.
gitc-init      Initialize a GITC Client.
grep           Print lines matching a pattern
info           Get info on the manifest branch, current branch or unmerged branches
init           Initialize repo in the current directory
list           List projects and their associated directories
overview       Display overview of unmerged project branches
prune          Prune (delete) already merged topics
rebase         Rebase local branches on upstream branch
smartsync      Update working tree to the latest known good revision
stage          Stage file(s) for commit
start          Start a new branch for development
status         Show the working tree status
sync           Update working tree to the latest revision
upload         Upload changes for code review
```

###### switch repo version
```bash
repo init --repo-rev=REV
repo selfupdate
repo version
```

## Issues tracking
[continues ...]
