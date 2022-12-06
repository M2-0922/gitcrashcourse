# Git Crash Course Part 2

Lifecyle of the status of files in a git repository, from untracked to committed.

### Additional Git Commands

Skip to staging area and commit

```bash
git commit -a -m "Commit message"
```

-a option will add all the files to staging area and commit them

<hr>

###### gitignore

Create a .gitignore file in the root directory of your project. Add the files you want to ignore to this file.

```bash
# .gitignore
node_modules
.DS_Store
```

<hr>
###### rm - mv

rm - Remove files from working tree and from the index

```bash
git rm <file>
```

mv - Move or rename a file, a directory, or a symlink

```bash
git mv <file>
```
<hr>

###### setting alias

```bash
git config --global alias.<alias-name> <command>
```

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.st status
```

<hr>

###### Non-linear development

Branching is a way to work on different versions of a repository at one time.

```bash
git branch <branch-name>
```

```bash
git checkout <branch-name>
```

```bash
git checkout -b <branch-name>
# -b option will create a new branch and switch to it
```
<hr>

###### HEAD

HEAD is a pointer to the last commit in the current branch.

<hr>

###### New Branch

```bash
git branch <branch-name>
```
<hr>

###### Merge

A standard merge will take each commit in the branch being merged and add them to the history of the base branch based on the timestamp of when they were created.

It will also create a merge commit, a special type of “empty” commit that indicates when the merge occurred

![Alt text](https://lukemerrett.com/content/images/2021/08/906613c7-94fb-41a8-9c74-77895dec7f53.png)

Advantages:

- Most descriptive and verbose history, tells us exactly when things happened, helps give the best context about code changes
- Allows us to see a graph of when branches were made using git log --oneline --graph which can help understanding why changes were made and when
- Allows us to see each commit that made up the eventual merged changes, no loss of granularity

Disadvantages:

- Merge commits are often seen as messy as they are empty and only really there for historical reasons. Can be especially confusing if you are trying to revert a set of changes.
- Can end up having a complex graph of previous branches that’s more difficult to read

###### Fast Forward Merge

If we change our example so no new commits were made to the base branch since our branch was created, Git can do something called a “Fast Forward Merge”. This is the same as a Merge but does not create a merge commit.

This is as if you made the commits directly on the base branch. The idea is because no changes were made to the base branch there’s no need to capture a branch had occurred.

Fast-forward is a way to move the current branch pointer forward to the latest commit.

![Alt text](https://lukemerrett.com/content/images/2021/08/6fbbe0c4-e8fe-4663-bbf8-19fa6c593bae.png)

Advantages:

- Keeps a very clean commit history
- Allows us to see each commit that made up the eventual merged changes, no loss of granularity

Disadvantages:

- Can only be done when the base branch hasn’t had any new commits, a rarity in a shared repository
- Can be seen as a inaccurate view of history as it hasn’t captured that a branch was created, or when it was merged

```bash
git merge <branch-name>
```
<hr>

###### Three-way merge

Three-way merge is a way to combine the changes from two branches.

Example of a three-way merge


```bash
git merge <branch-name>
```