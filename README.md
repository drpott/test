# Getting started: empty/new repo
#### 1. create the repo first in GITHUB
#### 2. on your PC, locally, init git in the directory:
```
git init
```
#### 3. connect the locally created repo to the remote
```
git remote add origin git@github.com:drpott/<repo_name>.git
git remote -v
```
#### 4. Fetch the remote repo
```
git fetch --all
```
#### 5. checkout the main branch
```
git checkout main
```
#### 6. push or upate the remote repo with main branch (or any other branch)
```
git push --set-upstream origin main
git branch --set-upstream-to=passmgmt/main origin
git push origin main
```

## Existing repo usage:
```
mkdir $USER/projects
cd $USER/projects

git clone git@github.com:drpott/mymodules.git

cd $USER/projects/kickOff/
./kickoff.sh
```

# GIT usage basics:

#### Show config file and remote target:
```
git config -l
git remote -v
git remote add <myLocalRepo> <RemoteRepo>
git pull <myLocalRepo> master
git push <myLocalRepo> master
```

#### Init new repo:
```
mkdir TestREpo
cd TestREpo
git init
```

#### go back to previous change (or commit in read only):
```
git status
git checkout <filename or commit>
git status
```

#### Revert to previous commit, but dont change or delete previous commits:
```
git log --oneline
git show <SHA1 hash>
git revert<SHA1 hash>
```

#### Create a branch and work on it:
```
git branch
git branch dev
git checkout dev
git checkout -b dev
```

#### Merge dev to master branch:
```
git branch
git checkout master
git merge dev master
```

#### Reset, delete commits from history and unstage files
```
git log --oneline
git reset --mixed <id of previous commit>
git checkout . ### if you want to delete the changes from the files
```

#### Soft, delete commits and keep files staged
```
git reset --soft <id of prev commit>
```

### if you need to make changes to the file, unstage them:
```
git reset .
git checkout .
```

#### Hard, delete commits and file changes
```
git reset --hard <id of prev commit>
```

#### Test your commits here:

```
test from git hub commit 1
test from git hub commit 2
  
test from git hub dev commit 1
test from git hub dev commit 2
test from git hub dev commit 3
```
