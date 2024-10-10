# Submodules

## Introduction

Submodules in GitHub are a way to incorporate other Git repositories as subdirectories within your main repository. This allows you to manage complex projects with modular components efficiently.

### Why Use Submodules:

This helps in breaking down large projects into smaller, reusable components managed in separate repositories and
Version Control to track changes and versions of each submodule independently. Also helps in integrating external libraries or tools as submodules without copying their code directly.

**Note**: Ensure you're using the specific version of a submodule required by your project.



## How Submodules Work:

### Adding a Submodule:

You reference an external Git repository URL within a file called `.gitmodules` in your main repository.

GitHub provides a convenient way to add submodules by using the URL with the `https://` or `git@` protocol when browsing the desired submodule repository.

### Initializing Submodules:

Run `git submodule update --init` to download and initialize the submodule repositories referenced in your `.gitmodules` file.

This creates a subdirectory for each submodule and checks out a specific commit from the submodule repository based on the configuration.

### Working with Submodules:

You can navigate into the submodule directory and work on it like a regular Git repository (clone, commit, push, etc.).

Changes made within the submodule won't directly affect your main repository.
Updating Submodules:

To update the submodule to a different commit from its repository, use `git submodule update`.

This will fetch changes from the submodule's remote repository and update the subdirectory to the specified commit.

### Committing Changes:

Commit changes made in the main repository and the submodule directory separately.
The main repository will track the submodule by reference (SHA) at the specific commit you've included.



## Extras

You can also refer to the following pages:


[Official Page for Git Bash](https://git-scm.com/docs/git-tag)