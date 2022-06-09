## Getting started:

### Usage:
```
mkdir $USER/projects
cd $USER/projects

git clone git@github.com:drpott/mymodules.git

cd $USER/projects/kickOff/
./kickoff.sh

```

### GIT Basics:

## Show config file and remote target:
```
git config -l
git remote -v
git remote add <myLocalRepo> <RemoteRepo>
git pull <myLocalRepo> master
git push <myLocalRepo> master
```

## Create the repo:
```
mkdir TestREpo
cd TestREpo
git init
```

## go back to previous change (or commit in read only):
```
git status
git checkout <filename or commit>
git status
```
## Revert to previous commit, but dont change or delete previous commits:
```
git log --oneline
git show <SHA1 hash>
git revert<SHA1 hash>
```
## Create a branch and work on it:
```
git branch dev
git branch
git checkout dev
```
## Merge dev to master branch:
```
git branch
git checkout master
git merge dev master
```

## Reset, delete commits from history and unstage files
```
git log --oneline
git reset --mixed <id of previous commit>
### if you want to delete the changes from the files
git checkout .
```

## Soft, delete commits and keep files staged
```
git reset --soft <id of prev commit>
```
### if you need to make changes to the file, unstage them:
```
git reset .
git checkout .
```
## Hard, delete commits and file changes
git reset --hard <id of prev commit>

test from git hub commit 1
