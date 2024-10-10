# Git Tags

## Introduction

Git tags are a way to mark specific points in your Git repository history. They act like bookmarks or labels that you can assign to important commits. Here's a breakdown of their functionalities and usage:

### Types of Git Tags:

**Annotated Tags**: These are the most common type. They store not only the commit reference but also additional information like a tag message, tagger name, and email address. You create annotated tags using the -m flag with the git tag command.

**Lightweight Tags**: These are simpler tags that store only the commit SHA (hash) reference. They are useful for creating quick references to specific commits but lack the descriptive information of annotated tags.

<h3>Creating Tags:</h3>

Use the git tag command followed by the tag name and optionally the -m flag for an annotated tag with a message.
```
# Create an annotated tag named "v1.0" with a message
git tag -m "Release version 1.0" v1.0
```

## Create a lightweight tag named "v1.1"

```
git tag v1.1
```


### Listing Tags:

Use the `git tag` command without arguments to list all tags in your repository.

```
git tag
```

### Viewing Tag Information:

Use the git show command followed by the tag name to see information about a specific tag, including the commit SHA, tagger details (for annotated tags), and the tag message (if applicable).

```
git show v1.0
```

Using Tags:

You can use tags for various purposes:

**Releases**: Mark stable releases of your project.

**Version Control**: Easily reference specific versions of your codebase.
s
**Collaboration**: Share specific points in your history with collaborators.

**Detaching HEAD** (referencing a specific tag): You can use the git checkout command with a tag name to detach the HEAD pointer to that specific commit. This allows you to work on that specific version of your codebase without affecting the current branch.

### Deleting Tags:

Use the git tag -d command followed by the tag name to delete a tag.
```
git tag -d v1.1  # Delete the tag "v1.1"
```
<img src = "https://github.com/FreakyOne700/OpenSourceTraining/blob/main/assets/git%20tag.png" width = "500px">

<img src = "https://github.com/FreakyOne700/OpenSourceTraining/blob/main/assets/git%20tag%20checkout.png" width  = "500px">



## Using Git Desktop

### Creating a Tag:

**History Tab**:  Click on the "History" tab in the left sidebar of GitHub Desktop. This displays the commit history of your local repository.

**Right-Click on Commit**:  Locate the commit you want to tag in the history view. Right-click on that specific commit.

**Create Tag**:  From the context menu that appears, select the option "Create Tag...".

**Tag Name**:  In the "Create a Tag" dialog window that pops up, enter a desired name for your tag. This name should be descriptive and clear about what the tag represents.

**Create Tag**:  Once you've entered the tag name, click on the "Create Tag" button.

## Extras

You can also refer to the following pages:

[Official Page for Git Bash](https://git-scm.com/docs/git-tag)

[Official Page for Git Desktop](https://docs.github.com/en/desktop/managing-commits/managing-tags-in-github-desktop)
