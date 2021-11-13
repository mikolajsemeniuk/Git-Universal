# Git-Universal
All most common git command lines

## Git Config
```sh
git config --global user.name "mikolaj semeniuk"
git config --global user.email "m.semeniuk@icloud.com"
# show git configuration
git config -l
```
## Git repo
```sh
# initialize a repository
git init .
# add origin
git remote add origin git@github.com:mikolajsemeniuk/git-universal.git
# remove a repository
rm -rf .git
```

## Git staging area
```sh
# working directory -> staging area -> commit history/commit area -> remote server

# show all tracked and untracked changes in staging area on local branch
git status

# add all
git add -A # all files with directories
git add . # all in directory
git add index.html # single file
git add index.html index.js # multiple files

# remove files from staging area
git reset # all
git reset HEAD -- . # all
git rm -r --cached . # all
git rm --cached index.css # single
git rm --cached index.js index.css # multiple

# remove file from staging area and also delete from file system
git rm -f index.css # single
git rm -r -f . # all

# restore changes made to files
git restore {file} # single file
git restore . # restore all changes
```

## Commits
```sh
git log
git log --branches --not --remotes # show all commits in commit history/commit area
git log --branches --not --remotes --simplify-by-decoration --decorate --oneline # the same but simplify
git show {commit_id} # show info about commit

git commit -m "commit name" # create new commit
git commit -n -m "Initial commit." # create commit which is able to delete
git commit --allow-empty -n -m "Initial commit." # create empty commit which is able to delete

git add {file} # update changes to already commited file
git restore {file} # rollback changes made to already commited file

git commit --amend -m "new name for last created commit"
```
