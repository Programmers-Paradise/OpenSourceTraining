# Stash

## Introduction

Git stash is a valuable feature that allows you to temporarily save your uncommitted changes in a stack, essentially putting them on hold. This enables you to switch to a different branch, work on something else, and then come back to your previous work later.

## Steps

### Stashing Changes:

Use the git stash command to save your current uncommitted work. By default, it creates a new stash entry with a generic name like "stash@{0}".

```
git stash
```

You can optionally provide a descriptive message along with the stash using the `-m` flag:

```
git stash -m "Fix bug in login functionality"
```

### Viewing Stashed Changes:

Use git stash list to see a list of your stashed changes, including the stash SHA and the provided message (if any).

```
git stash list
```

### Applying a Stash:

To re-apply the most recent stash (stash@{0}) and incorporate the changes back into your working directory, use `git stash pop`.

```
git stash pop
```

This will apply the changes from the stash and remove it from the stash list.

### Applying a Specific Stash:

If you have multiple stashes and want to apply a specific one (e.g., stash@{2}), use its SHA with git stash pop:
```
git stash pop stash@{2}
```
### Dropping a Stash:

To permanently remove a stash from the list without applying it, use `git stash drop`.
```
git stash drop stash@{1}  # Drops the stash with SHA "stash@{1}"
```
### Viewing the Contents of a Stash:

To see the changes in a specific stash without applying it, use `git stash show`:
```sh
git stash show stash@{2}  # Shows the contents of stash "stash@{2}"
```

## Using Git Stash in GitHub Desktop:

While GitHub Desktop doesn't have a built-in terminal for running Git commands, it offers a user-friendly interface to manage stashes:

Click on the Stash tab in the left sidebar.
This displays a list of your stashed changes. You can see the message (if provided) and the date/time of the stash.

Click on a specific stash to view its details.
You can choose to **Apply**, **Drop**, or **View** Changes of the selected stash.


## Extras

You can refer to the following pages for more information:

[Official Page(Bash)](https://git-scm.com/docs/git-stash)

