# Managing git commands

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

Keep track of what git is doing

```git
git log
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
