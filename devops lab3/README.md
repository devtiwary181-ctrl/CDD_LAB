# DevOps Lab 3: Git Pull vs Fetch & Merge

## Aim
To understand remote repository synchronization workflows, specifically analyzing the operational difference between direct `git pull` and the safer two-stage workflow of `git fetch` followed by `git merge`.

## Theory & Concepts
- **`git fetch`**: Downloads remote commits, branches, and tags from the remote repository (e.g. `origin`) into remote tracking branches (e.g. `origin/main`). It does **not** modify your current working directory or active branch.
- **`git merge`**: Integrates the fetched history into your active branch.
- **`git pull`**: Shorthand that immediately runs `git fetch` and attempts `git merge FETCH_HEAD`. If concurrent changes exist, it can trigger immediate merge conflicts.

## Workflow Comparison

| Action | Command | Working Tree Modified? | Conflict Risk |
|---|---|---|---|
| **Direct Pull** | `git pull origin main` | Yes, immediately | High (unreviewed incoming changes) |
| **Fetch & Inspect** | `git fetch origin` | No (updates `origin/main` only) | None |
| **Controlled Merge**| `git merge origin/main` | Yes, after review | Managed |

## Commands Used
```bash
# 1. Fetch changes without altering local work
git fetch origin

# 2. Inspect incoming commits
git log HEAD..origin/main --oneline

# 3. Merge verified remote changes
git merge origin/main
```

## Files in this Experiment
- `pull_fetch.txt`: Summary of synchronization goals.
- `myfriend.txt`: Step-by-step workflow guide for conflict avoidance via fetch + merge.
- `new.txt`: Test file tracking fetch and merge validation.
- `pull.txt`: Test file tracking direct pull execution.
