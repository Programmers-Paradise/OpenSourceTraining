# Merging

Merging branches in Git is a way to combine the changes made on separate branches into a single branch. It's a fundamental concept in Git workflows, allowing you to integrate different lines of development and keep your project history organized.

## How its done
**Switching Branches**:  Before merging, you typically switch to the branch where you want to integrate the changes from another branch. This is often the main branch (like master) that holds the core codebase.

**Merging the Branch:**  Use the git merge command followed by the name of the branch you want to integrate.
For example, to merge a branch named feature into the current branch, you would run:

```sh
git merge <feature>
```

**Git's Analysis**:  Git analyzes the history of both branches to determine how to integrate them. There are two main scenarios:

**Fast-forward Merge** (Simple Scenario):  If the branch you're merging from was created from the current branch and hasn't diverged (no new commits in the current branch since the feature branch was created), Git can perform a fast-forward merge. It simply moves the pointer of the current branch to the commit tip of the branch being merged, effectively incorporating its changes.

i.e After creations of a new branch B from Branch A ,There has been no commits in Branch A since the creation of Branch B. *Just like adding a new node at the last of a linked list*

**Three-way Merge** (Common Scenario):  If the branches have diverged (meaning there have been new commits in the current branch since the feature branch was created), Git performs a more complex three-way merge. It analyzes the common ancestor commit (the last commit both branches share) and identifies the changes introduced in each branch since then. It attempts to combine these changes automatically.

**Merge Conflict Resolution** (Potential):  In the case of conflicting changes (where both branches modify the same part of a file), Git cannot automatically resolve the conflict. It will mark the conflicting sections in the file and leave them for you to manually resolve. You'll need to edit the file to decide how you want to integrate the changes from both branches.

**Committing the Merge**:  Once you've resolved any conflicts or reviewed the changes, you can commit the merge. This creates a new commit on the current branch that reflects the integration of the merged branch.

## Some additional points to consider:

**Visual Merge Tools**:  Some Git tools offer visual merge tools that can help you see the differences between conflicting sections and make it easier to resolve them.

**Branch Deletion** (Optional):  Once you've successfully merged a branch and are confident the changes are integrated, you can optionally delete the branch using git branch -d <branch_name>. However, it's sometimes recommended to keep feature branches for future reference.

**Merge Strategies** (Advanced):  Git offers various merge strategies that control how conflicts are handled during a merge.  These are typically used in more advanced scenarios.

### Challenges
Try to demonstrate `fast-forward` and `three-way` merge!
### Fast-Forward Merge (Example)
1. Initialize a repository and create a file
```
git init fast-forward-example
cd fast-forward-example
echo "Hello World" > file.txt
git add file.txt
git commit -m "Initial commit on main branch"
```
2. Create a new branch
```
git checkout -b feature-branch
```
3. Make changes on the feature branch
```
echo "Feature work in progress" > feature.txt
git add feature.txt
git commit -m "Added feature.txt on feature-branch"
```
4. Switch back to the main branch

```bash
git checkout main
```
5. Merge the feature-branch into main (fast-forward merge)
```
git merge feature-branch
```
6. Check the commit history
```
git log --oneline
```

### Three-Way Merge
1. Initialize a repository and create a file
```
git init three-way-merge-example
cd three-way-merge-example
echo "Hello World" > file.txt
git add file.txt
git commit -m "Initial commit on main branch"
```
2. Create a new branch
```
git checkout -b feature-branch
```
3. Make changes on the feature-branch
```
echo "Feature branch content" > feature.txt
git add feature.txt
git commit -m "Added feature.txt on feature-branch"
```
4. Switch back to the main branch and make changes
```
git checkout main
echo "Main branch updated" >> file.txt
git add file.txt
git commit -m "Updated file.txt on main branch"
```

5. Merge the feature-branch into main (three-way merge)
```
git merge feature-branch
```
6. Check the commit history
```
git log --oneline
```