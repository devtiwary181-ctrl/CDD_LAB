# DevOps Lab 5: Git Rebase & Multi-Commit Sequences

## Aim
To master Git rebasing techniques, understand how to maintain a clean linear commit history, manage sequential commits, and perform interactive rebasing (`git rebase -i`).

## Concepts & Theory
- **Rebasing vs Merging**:
  - `git merge`: Combines two branches with an explicit merge commit, preserving branching history.
  - `git rebase`: Re-applies commits from the current branch onto another base branch, producing a straight, clean linear commit log.
- **Interactive Rebase (`git rebase -i`)**:
  Allows modifying commit history:
  - `pick`: keep the commit as is
  - `reword`: modify the commit message
  - `edit`: pause to amend files in the commit
  - `squash`: combine commit with the previous commit
  - `fixup`: combine commit and discard its log message
  - `drop`: delete the commit

## Commands Used
```bash
# Sequential commit workflow
git add devops\ lab5/file1.txt && git commit -m "commit 1"
git add devops\ lab5/file2.txt && git commit -m "commit 2"
git add devops\ lab5/abc.txt devops\ lab5/bcd.txt && git commit -m "commit 3"
git add devops\ lab5/edf.txt && git commit -m "commit 4"
git add devops\ lab5/file3.txt && git commit -m "commit 5"

# Rebase current branch onto main
git rebase main

# Interactive rebase for the last 5 commits
git rebase -i HEAD~5
```

## Files in this Experiment
- `file1.txt`: Initial rebase marker file ("starting rebase").
- `file2.txt`: Secondary commit file ("new file").
- `abc.txt`, `bcd.txt`, `edf.txt`, `file3.txt`: Empty tracking files representing sequential feature commits in the rebase pipeline.

