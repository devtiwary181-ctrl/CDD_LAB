# DevOps Lab 4: Git Branching & Merging

## Aim
To master branch creation, switching contexts, developing isolated features on a branch, pushing branches to remote, merging changes into the `main` branch, and cleaning up merged branches.

## Concepts & Commands
Git branching provides an isolated workspace to build features or fix bugs without affecting the stable `main` branch.

```bash
# Check current branches
git branch

# Create a new feature branch and switch to it
git checkout -b feature-branch
# Alternatively:
git switch -c feature-branch

# Develop feature and commit
git add devops\ lab4/branch_file.cpp
git commit -m "Add feature code on branch"

# Push branch to remote
git push -u origin feature-branch

# Switch back to main and merge
git switch main
git merge feature-branch

# Delete local feature branch
git branch -d feature-branch
```

## Files in this Experiment
- `branch_file.cpp`: C++ source file implementing a sample program developed on a feature branch.
- `notes.txt`: Detailed command cheatsheet for Git branching operations.

## Execution Output
```text
$ clang++ branch_file.cpp -o branch_file
$ ./branch_file
This is a feature branch file created by Dev Tiwary.
Demonstrating Git branching and merging workflows!
Changes successfully integrated into main.
```
