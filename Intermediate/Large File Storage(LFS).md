# Git Large File Storage

## Introduction
Git LFS (Large File Storage) is a Git extension that helps manage large files efficiently within a Git repository.
## How it works
How Git LFS Works:

**Marking Large Files**: You configure Git LFS to track specific file types or extensions (e.g., .mp4, .jpg) as large files.

**Pointer Files**: When a large file is added to the repository, Git LFS replaces it with a small text file called a pointer file. This pointer file contains a reference (like a hash) to the actual file content stored elsewhere.

**Remote Storage**: The actual content of the large file is stored on a remote server supported by Git LFS, such as a Git hosting service or a dedicated server you manage.

## How to Use/Configure Git LFS
### Configure

There are two main configuration approaches:

**Global Configuration (Optional):**

Use the git lfs config command to define global settings that apply to all your Git repositories. For example:

```Bash
git lfs config track "*.iso"  # Track all files with .iso extension
```

You can specify multiple file extensions to track and even set the remote storage location if you're not using a Git hosting service with built-in Git LFS support.

### Repository-Specific Configuration (**Recommended**):

This approach is generally recommended. It allows you to define specific settings for each repository. Here's the workflow:

Create a .gitattributes file: In the root directory of your Git repository, create a new file named .gitattributes.

Define tracking patterns: Inside the .gitattributes file, add lines specifying the file patterns Git LFS should track. For example:
```Bash
*.psd filter=lfs diff=lfs merge=lfs -text
*.mp4 filter=lfs diff=lfs merge=lfs -text
```
This configures Git LFS to track files with .psd and .mp4 extensions.

 The additional options (diff and merge) define how Git LFS handles diffs and merges for these large files (often set to lfs for server-side handling).

Commit the .gitattributes file: Add and commit the .gitattributes file to your repository.

### Use
When you add a large file to your repository that matches a configured tracking pattern (e.g., .psd), Git LFS will automatically replace it with a pointer file containing a reference to the actual file content.

You can commit and push changes to your repository as usual. Git LFS manages the pointer files and interacts with the remote storage for the large file content behind the scenes.

## Note
Downloading large files during operations like cloning might require an internet connection. If you have limited bandwidth, this could impact performance.
## Extras
You can also refer to the [Official Page](https://docs.github.com/en/repositories/working-with-files/managing-large-files/configuring-git-large-file-storage) for Large File Storage for more info.