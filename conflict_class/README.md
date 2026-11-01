# DevOps Lab: Merge Conflict Simulation & Resolution

## Aim
To understand how Git identifies conflicting changes across branches, interpret Git conflict markers, manually resolve conflicts, and commit the reconciled state.

## Why Merge Conflicts Occur
A merge conflict occurs when two branches make competing edits to the exact same line of a file, or if a file is deleted in one branch and modified in another. Git pauses the merge and inserts conflict markers to require manual developer intervention.

## Conflict Markers Structure
```text
<<<<<<< HEAD
(Changes present in the current active branch)
=======
(Changes incoming from the branch being merged)
>>>>>>> feature-branch
```

## Step-by-Step Resolution Workflow
1. **Triggering Conflict**:
   - On branch `main`: Modify line 2 and commit.
   - On branch `feature`: Modify line 2 with differing content and commit.
   - Switch to `main` and execute `git merge feature`.
   - Git reports: `CONFLICT (content): Merge conflict in conflict_class/merge_conflict.txt`.
2. **Inspecting Conflict**:
   - Run `git status` to see unmerged paths.
   - Open the conflicting file to view the markers.
3. **Resolving**:
   - Edit the file to preserve the desired final logic and remove all markers (`<<<<<<<`, `=======`, `>>>>>>>`).
4. **Finalizing**:
   ```bash
   git add conflict_class/merge_conflict.txt
   git commit -m "Resolve merge conflict between main and feature branch"
   ```

## Files in this Experiment
- `merge_conflict.txt`: Text file illustrating resolved state after reconciling competing commits across branches.

