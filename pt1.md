### Git Crash Course Pt-1

Git is a version control system. It is used to track changes in files and directories. It is used to track changes in files and directories. It is used to track changes in files and directories.

```bash
git config --list

git config --global user.name "Your Name"
git config --global user.email "Your Email Address"
```

##### Git Commands

```
git init: Initialize a local git repository
git add: Add files to staging area
git commit: Commit changes to repository
git status: Check status of working tree
git log: Show commit logs
git diff: Show changes between commits, commit and working tree, etc
git checkout: Switch branches or restore working tree files
git tag: Create, list, delete or verify a tag object signed with GPG
```

##### Git Tags

```
git tag: Create, list, delete or verify a tag object signed with GPG
git tag -a v1.4 -m "my version 1.4"
git tag -a v1.2 9fceb02
git tag -d v1.4
git push origin v1.5
git push origin --tags
```


git init - Create a new git repository in the current directory

```bash
git init
```

git add - Add files to staging area

```bash
git add <file>
git add .
```

git commit - Commit changes to repository

```bash
git commit -m "Commit message"

options: -a, --all
         -m, --message

git commit -a -m "Commit message"
-a option will add all the files to staging area and commit them
```

git status - Check status of working tree

```bash
git status

options: -s, --short
         -b, --branch
         -u, --untracked-files[=all|normal|no]
```

git log - Show commit logs

```bash
git log
```

git diff - Show changes between commits, commit and working tree, etc

```bash
git diff

options: --staged
         --color-words
         --word-diff=color
         --histogram
         --minimal
         


```

git checkout - Switch branches or restore working tree files

```bash
git checkout <branch>
git checkout -b <new-branch-name>
```

git branch - List, create, or delete branches

```bash
git branch
options: -d, -D
-d - Delete a branch
-D - Force delete a branch
```

git merge - Join two or more development histories together

```bash
git merge <branch>
```

git remote - Manage set of tracked repositories

```bash
git remote add origin <remote-url>
```

git push - Update remote refs along with associated objects

```bash
git push origin master
-u: Set the upstream branch for the current branch
-f: Force push
--all: Push all branches
```


