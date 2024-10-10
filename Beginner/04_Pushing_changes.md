# Pushing Changes
## How to push changes?
### Using Git Bash

1. **Open Git Bash:**
   - Find and open Git Bash on your computer. It's a terminal application where you can type commands.

2. **Navigate to Your Local Repository:**
   - Use the `cd` (change directory) command to navigate to the directory of your local Git repository.
     ```sh
     cd path/to/your/repository
     ```
     Replace `path/to/your/repository` with the actual path to your repository

3. **Check the Status:**
   - Check the status of your working directory to see which files have been modified or are untracked:
     ```sh
     git status
     ```
      **Note:** 
      - If any files are untracked and you want to track them, [add](./Staging_and_Commiting.md) them.

4. **Push Your Changes to the Remote Repository:**
   - Push your committed changes to the remote repository.
     ```sh
     git push origin main
     ```
     Replace `main` with the name of your branch if it’s different

### Using GitHub Desktop

1. **Open GitHub Desktop:**
   - Open GitHub Desktop from your applications menu.

2. **Open Your Repository:**
   - If your repository isn't already open, go to `File > Open repository` and select your repository.

3. **Make Changes and Add Files:**
   - Make changes to your files using your preferred text editor or directly through GitHub Desktop.
   - You can add new files to the repository folder directly.

4. **Review Changes:**
   - In GitHub Desktop, you will see a list of changed files in the left panel under the `Changes` tab.
   - Review the changes by clicking on each file to see what has been modified.

5. **Commit Your Changes:**
   - At the bottom of the left panel, you will see fields for a commit summary and description.
   - Enter a summary of your changes in the `Summary` box (e.g., "Add new feature and update documentation").
   - Optionally, you can provide a more detailed description in the `Description` box.
   - Click the `Commit to main` button (or the button for your current branch) to commit the changes.

6. **Push Changes to Remote:**
   - After committing your changes, you will see a `Push origin` button at the top of the GitHub Desktop window.
   - Click the `Push origin` button to push your committed changes to the remote repository.
