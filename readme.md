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
