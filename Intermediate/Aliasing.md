# Aliasing

## Introduction

Git aliases allow you to create shortcuts for frequently used Git commands. This can significantly improve your workflow by saving you time and keystrokes.

## Steps
Creating Git Aliases:

There are two main ways to create Git aliases:

**Global Configuration**:

Use the `git config` command to define aliases that apply to all your Git repositories. These settings are stored in your global Git configuration file (`~/.gitconfig` on Unix-based systems).

```sh
git config --global alias.st status
git config --global alias.co checkout
```

In this example, `st` becomes an alias for `git status` and `co` becomes an alias for `git checkout`. You can define aliases for any Git command.

**Repository-Specific Configuration**:

You can also define aliases specific to a particular Git repository. These settings are stored in the `.git/config` file within your repository.

```
git config alias.br branch
git config alias.logshow log -p -n 5  # More detailed log view
```

Here, `br` becomes an alias for `git branch` and `logshow` is an alias for a more detailed `git log` command showing the last 5 commits with patches.

### Using Aliases:

Once you've defined aliases, you can use them just like regular Git commands:

```
git st   # This executes git status
git co master  # This executes git checkout master
```

### Advanced Aliases:

You can create even more powerful aliases by combining multiple commands or using shell scripting within the alias definition. This allows you to automate repetitive tasks.

Example:

```
git config --global alias.pushall 'git push origin --all && git push --tags'
```

This alias, `pushall`, executes both `git push origin --all` (push all branches) and `git push --tags` (push all tags) in a single command.

## Challenge
Try `Aliase` a command and show screenshot of sucessfull aliasing

## Extras

You can refer to the following pages for more information:

[Official Page(Bash)](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
