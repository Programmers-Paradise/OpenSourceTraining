# Staging files and commiting changes
## Why to stage file?

## How to stage a file and commit changes
- ### Using Git Bash
    **Step 1: Open Git Bash**
    - Open Git Bash on your computer.
    
    **Step 2: Navigate to Your Local Repository**
    - Use the cd command to navigate to the directory of your local repository. For example:
    
      ```sh
      cd path/to/your/repository
      ```
    
    **Step 3: Check the Status**
    - You can see the current status of your working directory and check which files are untracked or have been modified(added, deleted or     updated), using:
    
      ```sh
      git status
      ```
    **Step 4: Add Files to Staging Area**
    - You can add a specific file to the staging area, using:
    
      ```sh
      git add < filename >
      ```
       - To add all modified and untracked files, use:
    
       ```sh
       git add .
       ```
    **Step 5: Commit the Changes**
    - Commit the changes with a descriptive commit message:
    
      ```sh
      git commit -m "Your commit message"
      ```
    **Step 6: Verify**
    - You can verify if all the required files are staged, using:
    
      ```sh
      git status
      ```
    
    **Note:** 
              
     - To unstage a file, use:
              
       ```sh
       git restore --staged < filename >
       ```

- ### Using GitHub Desktop
    **Step 1: Open GitHub Desktop**
     - Open GitHub Desktop on your computer.
    
    **Step 2: Open Your Repository**
     - If your repository is not already open, go to File > Open repository and select your repository.
    
    **Step 3: Make Changes and Add Files**
     - Make changes to your files using your preferred text editor or IDE. You can also add new files to the repository folder directly.
    
    **Step 4: Review Changes**
     - In GitHub Desktop, you will see a list of changed files in the left panel under the Changes tab. You can review the changes by clicking  on  each file.
    
    **Step 5: Stage Changes**
     - By default, all changes will be staged for commit. You can uncheck any files you don't want to commit.
    
    **Step 6: Commit the Changes**
     - At the bottom of the left panel, you will see fields for a commit summary and description. Enter a summary of your changes and an       optional description.
    
    **Step 7: Commit to Branch**
     - Click the Commit to main (or the current branch name) button to commit the changes.