# Continuous Delivery & DevOps (CDD) Lab

**Author**: Dev Tiwary ([@devtiwary181-ctrl](https://github.com/devtiwary181-ctrl))  
**Repository**: [CDD_LAB](https://github.com/devtiwary181-ctrl/CDD_LAB)  
**Reference Blueprint**: [Raavee-Singh/cdd_lab](https://github.com/Raavee-Singh/cdd_lab)

---

## 📌 Overview
This repository contains the complete practical curriculum for the **Continuous Delivery and DevOps (CDD) Lab**. It covers hands-on industry-standard practices in Version Control Systems (VCS) using Git and GitHub, ranging from core command-line fundamentals to multi-branch development, remote repository synchronization, conflict resolution strategies, and commit history linearization via rebasing.

---

## 📂 Repository Structure

```text
CDD_LAB/
├── devops lab1/                               # Exp 1: Git Basics & First Commit
│   ├── hello.txt
│   └── README.md
├── devops lab2/                               # Exp 2: Remote Repositories & Cloning
│   ├── code.cpp
│   ├── cloning folder/
│   │   ├── read.txt
│   │   └── cdd_lab/
│   │       ├── devops lab1/
│   │       │   └── hello.txt
│   │       └── devops lab2/
│   │           └── code.cpp
│   └── README.md
├── devops lab3/                               # Exp 3: Git Pull vs Fetch & Merge
│   ├── myfriend.txt
│   ├── new.txt
│   ├── pull.txt
│   ├── pull_fetch.txt
│   └── README.md
├── devops lab4/                               # Exp 4: Branching, Switching & Merging
│   ├── branch_file.cpp
│   ├── notes.txt
│   └── README.md
├── conflict_class/                            # Exp 5: Merge Conflict Resolution
│   ├── merge_conflict.txt
│   └── README.md
├── devops lab5/                               # Exp 6: Git Rebase & History Manipulation
│   ├── abc.txt
│   ├── bcd.txt
│   ├── edf.txt
│   ├── file1.txt
│   ├── file2.txt
│   ├── file3.txt
│   └── README.md
├── login.txt                                  # Feature branch change
├── PLAN.md                                    # Implementation tracking checklist
├── REFERENCE_ANALYSIS.md                      # Comprehensive blueprint analysis
└── README.md                                  # Repository documentation
```

---

## 🧪 Experiments Catalog

### Experiment 1: Git Basics, Local Repository Setup & First Commit (`devops lab1`)
- **Aim**: Initialize a Git repository, stage files, record initial snapshot, modify tracked files, and observe working tree states.
- **Key Commands**:
  ```bash
  git init
  git add hello.txt
  git commit -m "initial commit"
  git diff hello.txt
  git commit -am "made a modification"
  ```
- **Files**:
  - `devops lab1/hello.txt`
  - `devops lab1/README.md`

---

### Experiment 2: Remote Repositories, C++ Compilation & Cloning (`devops lab2`)
- **Aim**: Author and compile a C++ application, connect local repository to remote GitHub repository, push changes, and clone into a separate directory to simulate multi-developer collaboration.
- **Compilation & Execution**:
  ```bash
  clang++ "devops lab2/code.cpp" -o code
  ./code
  ```
  *Output*:
  ```text
  My name is Dev Tiwary.
  Pushing my code to Remote repository in Github!
  ```
- **Key Commands**:
  ```bash
  git remote add origin https://github.com/devtiwary181-ctrl/CDD_LAB.git
  git push -u origin main
  git clone https://github.com/devtiwary181-ctrl/CDD_LAB.git "cloning folder"
  ```
- **Files**:
  - `devops lab2/code.cpp`
  - `devops lab2/cloning folder/read.txt`
  - `devops lab2/cloning folder/cdd_lab/...`
  - `devops lab2/README.md`

---

### Experiment 3: Git Remote Synchronization - Pull vs Fetch & Merge (`devops lab3`)
- **Aim**: Understand how remote tracking branches operate and compare direct `git pull` against the safer two-step `git fetch` + `git merge` workflow for conflict mitigation.
- **Workflow**:
  ```bash
  # Step 1: Fetch remote changes without affecting local working tree
  git fetch origin

  # Step 2: Inspect incoming commits
  git log HEAD..origin/main --oneline

  # Step 3: Fast-forward / merge cleanly
  git merge origin/main
  ```
- **Files**:
  - `devops lab3/pull_fetch.txt`
  - `devops lab3/myfriend.txt`
  - `devops lab3/new.txt`
  - `devops lab3/pull.txt`
  - `devops lab3/README.md`

---

### Experiment 4: Git Branching, Switching, and Branch Merging (`devops lab4`)
- **Aim**: Implement isolated feature development via Git branches, switch contexts, publish feature branches to remote, and integrate changes back into `main`.
- **Compilation & Execution**:
  ```bash
  clang++ "devops lab4/branch_file.cpp" -o branch_file
  ./branch_file
  ```
  *Output*:
  ```text
  This is a feature branch file created by Dev Tiwary.
  Demonstrating Git branching and merging workflows!
  Changes successfully integrated into main.
  ```
- **Key Commands**:
  ```bash
  # Create and switch to new branch
  git switch -c feature-branch  # or git checkout -b feature-branch
  git push -u origin feature-branch

  # Return to main and merge
  git switch main
  git merge feature-branch
  git branch -d feature-branch
  ```
- **Files**:
  - `devops lab4/branch_file.cpp`
  - `devops lab4/notes.txt`
  - `devops lab4/README.md`

---

### Experiment 5: Merge Conflict Generation & Resolution (`conflict_class`)
- **Aim**: Simulate concurrent conflicting edits across different branches on identical lines of code, inspect conflict markers, manually resolve the conflict, and complete the merge.
- **Conflict Anatomy**:
  ```text
  <<<<<<< HEAD
  Changes in current branch
  =======
  Changes in incoming branch
  >>>>>>> feature-branch
  ```
- **Resolution Steps**:
  1. Detect conflict during `git merge`.
  2. Open file and resolve edits manually.
  3. Remove conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
  4. Stage with `git add` and commit with `git commit`.
- **Files**:
  - `conflict_class/merge_conflict.txt`
  - `conflict_class/README.md`

---

### Experiment 6: Git Rebase, Commit Squashing & History Linearization (`devops lab5`)
- **Aim**: Manage sequential multi-commit workflows, linearize project history, and use interactive rebasing (`git rebase -i`) to squash and reword commits.
- **Key Commands**:
  ```bash
  # Sequential feature commits
  git commit -m "commit 1"
  git commit -m "commit 2"
  ...
  # Rebase onto base branch
  git rebase main

  # Interactive rebase for history cleanup
  git rebase -i HEAD~5
  ```
- **Files**:
  - `devops lab5/file1.txt`, `file2.txt`, `file3.txt`
  - `devops lab5/abc.txt`, `bcd.txt`, `edf.txt`
  - `devops lab5/README.md`

---

## 🛠️ Environment & Prerequisites
- **Git**: 2.30+ (`git --version`)
- **C++ Compiler**: Clang (`clang++`) or GCC (`g++`) with C++17+ support
- **Platform**: macOS / Linux / Windows (Git Bash)

---

## 🚀 Cloning & Running Locally

```bash
# Clone the repository
git clone https://github.com/devtiwary181-ctrl/CDD_LAB.git
cd CDD_LAB

# Compile and test Experiment 2
clang++ "devops lab2/code.cpp" -o code2 && ./code2

# Compile and test Experiment 4
clang++ "devops lab4/branch_file.cpp" -o branch4 && ./branch4
```
