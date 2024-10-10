# Commit history
## Why to view commit history?
   To see who made the changes and at what time .
   To see the changes made in the file.
## How to view commit history?

- ### Using Git Bash

   **Step 1: Open Git Bash:**
     - Go to your file location.
     - Right click there and select option `Open git bash here`.
     - Your git bash interface will open.
 
   **Step 2: View Commit History:**
     - To view the commit history, use the `git log` command:
       ```sh
       git log
       ```
       - This command will display a list of commits with details such as the commit hash, author, date, and commit message.

   **Step 3: Additional Options:**
     - For a more concise view, you can use:
       ```sh
       git log --oneline
       ```
       - This will display each commit on a single line.
     - To see a graphical representation of the commit history, you can use:
       ```sh
       git log --graph --oneline --all
       ```

- ### Using GitHub Desktop

  **Step 1: Open GitHub Desktop:**
     - Open GitHub Desktop from your applications menu.
      
   **Step 2: Open Your Repository:**
     - If your repository isn't already open, go to `File > Open repository` and select your repository.
      
   **Step 3: View Commit History:**
     - In GitHub Desktop, switch to the `History` tab located at the top of the left sidebar.
     - This tab will display a list of all commits in the repository. Each commit entry shows the commit message, author, and date.
      
   **Step 4: View Commit Details:**
     - Click on any commit in the history list to see detailed information about the changes made in that commit.
     - The details pane will show the files that were changed, added, or deleted in that commit, along with the specific changes (diff) for each file.
