## git setting up

- You can view all of your settings and where they are coming from using
- setting the name and email

```git
 git config --list --show-origin
 git config --global user.name "John Doe"
 git config --global user.email johndoe@example.com

```

## Initializing a Repository

- git init create a new file .git in your project
- git clone is used to clone a existing project 

```git
 git init
 git clone https://github.com/libgit2/libgit2 mylibgit
```

## Staging and Commit

- adding a file to staging, example adding a readme file
- git diff --staged/cached show your staged changes
- git diff show your untracked changes
- git commit -m adding a commit with a message

```git
 git add readme
 git commit -m "Story 182: fix benchmarks for speed"
```

- to avoid adding each file to staging and the doing a commit git provide -a to stage and commit in single git command

```git
  git commit -a -m 'Add new benchmarks'
```

#### amend 
 git amend is used in case you missed to commit a file to your previous commit you can use amend
 - use --no-edit when you don't want to add a commit msg and use previous message

>Note never update the previously commited file while using amend.
`can be done using rebase command as well`

```git
  git commit --amend

  git commit --amend --no-edit
```

#### log 

- git log command display the commits that been done in the repo, in order as most recent in first.

```git
  git log

  git log --oneline
```

#### Unmodifying a Modified File

- How can
you easily unmodify it — revert it back to what it looked like when you last committed
- "git checkout -- filename..."

```git
    git checkout -- CONTRIBUTING.md
```

#### Unstaging a staged file
- git restore --staged move to untracked file with changes
- git restore file name restore to original state when it was before doing the changes. Any
local changes you made to that file are gone
```git
    git restore --staged CONTRIBUTING.md
    git restore CONTRIBUTING.md
```

- creating a new branch and swtiching to the branch 
- can be done in single command git checkout -b iss53
```git
    git branch iss53
    git checkout iss53
    
    git checkout -b iss53 
```

#### reverting a commit
- n is the number of commit
- soft will have chnages in the staging 
- hard will remove the commit and have it as how it looked before the nth commit

```git
    git reset --soft HEAD~n 
    git reset --hard HEAD~n
        
```
