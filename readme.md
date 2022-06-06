# Managing git commands and Github

First, register the username and the email for the global user using

username

```git
git config --global user.name "FrankRight"
```

email

```git
git config --global user.email "frankbosire2017@gmail.com"
```

Initialize git.

```git
git init
```

Use the add command to stage files in the current directory

```git
git add <FILENAME>
git add .
```

Then commit the changes

```git
git commit -m "COMMIT MESSAGE..."
```

Keep track of what git is doing, show all commit made to document.

```git
git log
```

To show git log in a single line

```git
git log --oneline
```

## Understanding Environments

By the default the branch that we are working on will be set to master or main

3 work environments

- Working
- Staging
- Commit

Before a commit files can be in one of these 2 states:-

- Tracked - previous commit
- Untracked - any other files not commited

Tracked files can also exist in different states:

- Unmodified - Files have not changed since the last commit
- Modified - Files have changed since the last commit
- Staged - The changes have been staged

### command git status

Tracks down changes made to a file to show the stage currently they are in. It also shows you what options you have to perform an action.

### restore command

Redo some changes.

#### With filename

```git
git restore readme.md
```

#### Restore current directory

```git
git restore .
```

#### Restore from the staged part

```git
git restore --staged <FILENAME>
```

## ignore some files

use a file called .gitignore in the root of the project to ignore files.

Can be patterns or just file names

```git
.DS_Store
.vscode/
node_modules
**/*-todo.md
```

### Global ignoring of files

```git
git config --global core.excludesfile [file]
```

### Clearing the git cache

If git ignore does not working try clearing the cache first.

```git
git rm -r --cached .
```

## File deletion

```git
git rm <file to be removed>
```

## File renaming

```git
git mv <name of file to be renamed> <name to be renamed>
```

File renaming and deletion using the above git commands places the files in staging state instead of normal modified this helps us skip an addition staging command step.

## difference between changes

```git
git diff
```

To exit if a colon appear press q on the keyboard. For a lot of it diff tracking try using gitlens extension from the extensions marketplace.

## Amending

```git
git commit --amend
```

## A reset

Going back to a previous commit. Unstages some changes of the specified commit.

```git
git reset <COMMIT ID>
```

To delete all commit before the specified commit.

```git
git reset --hard <COMMIT ID>
```

## Rebasing

Commits from one branch to another.

```git
git rebase <branch>/<commit>
```

Using it with an iteractive editor is the best way to use rebase.

```git
git rebase --interactive <branch>/<commit>

or

git rebase --i HEAD~<no of commits>

or

git rebase -i --root
```

## Branches

### List all braches

```git
git branch
```

### Copying a branch

```git
git switch -c <new branch name>

# Switch to master or a specific branch
git switch <name of the branch>

or older version
git checkout -b <new branch name>
```

### Merging branch with main

navigate first to main branch before running the below command.

```git
git merge <branchname>
```

### Deleting a branch

After merging with the main if the branch is no longer in need you can delete it.

```git
git branch --delete <branchname>

or

git branch -d <branchname>

or

git branch -D <branchname>
```

## Working with Github

### remotes

Link a remote link to a github rep

```git
git remote add <name> <url>
```

Remove a remote rep

```git
git remote remove <name>
```

Renaming a remote rep

```git
git rename <oldname> <newname>
```

List all the remotes available

```git
git remote -v
```

Pushing a remote online

```git
git push <remote branch>
```

Pushing for the first time

```git
git push -u origin-main
```

Subsequent pushes - after the first one

```git
git push
```

All local braches to github

```git
git push --all
```
