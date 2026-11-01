# Reference Repository Analysis

## 1. Overview
- **Reference Repository**: [Raavee-Singh/cdd_lab](https://github.com/Raavee-Singh/cdd_lab)
- **Target Repository**: [devtiwary181-ctrl/CDD_LAB](https://github.com/devtiwary181-ctrl/CDD_LAB)
- **Domain**: Continuous Delivery and DevOps (CDD) Lab Experiments
- **Primary Focus**: Practical Git workflows, version control fundamentals, remote repository management, branching strategies, conflict resolution, and history management (rebase).

---

## 2. Inventory & Directory Structure

```text
cdd_lab/
├── devops lab1/
│   └── hello.txt
├── devops lab2/
│   ├── code.cpp
│   └── cloning folder/
│       ├── read.txt
│       └── cdd_lab/
│           ├── devops lab1/
│           │   └── hello.txt
│           └── devops lab2/
│               └── code.cpp
├── devops lab3/
│   ├── myfriend.txt
│   ├── new.txt
│   ├── pull.txt
│   └── pull_fetch.txt
├── devops lab4/
│   ├── branch_file.cpp
│   └── notes.txt
├── conflict_class/
│   └── merge_conflict.txt
└── devops lab5/
    ├── abc.txt
    ├── bcd.txt
    ├── edf.txt
    ├── file1.txt
    ├── file2.txt
    └── file3.txt
```

---

## 3. Detailed Experiment Analysis

| # | Experiment / Item | Files Involved | Description | Status in Target Repo |
|---|---|---|---|---|
| 1 | **devops lab1** (Git Basics & First Commit) | `devops lab1/hello.txt` | Basics of initializing local repository, tracking files, staging (`git add`), initial commit, and modifying tracked files. | Missing |
| 2 | **devops lab2** (Remote Repositories & Cloning) | `devops lab2/code.cpp`<br>`devops lab2/cloning folder/read.txt`<br>`devops lab2/cloning folder/cdd_lab/...` | Writing and compiling a C++ program, linking to GitHub remote (`git remote add origin`), pushing code (`git push`), and cloning repository into a separate folder (`git clone`). | Missing |
| 3 | **devops lab3** (Git Pull vs Fetch & Merge) | `devops lab3/pull_fetch.txt`<br>`devops lab3/myfriend.txt`<br>`devops lab3/new.txt`<br>`devops lab3/pull.txt` | Exploring Git synchronization workflows: comparing direct `git pull` against two-stage `git fetch origin` + `git merge origin/main` to inspect and avoid merge conflicts. | Missing |
| 4 | **devops lab4** (Branching, Switching & Merging) | `devops lab4/branch_file.cpp`<br>`devops lab4/notes.txt` | Creating branches (`git branch`), switching branches (`git checkout` / `git switch`), shorthand branch creation (`git checkout -b` / `git switch -c`), feature branch commits, remote branch pushing, and branch merging. | Missing |
| 5 | **conflict_class** (Merge Conflict Resolution) | `conflict_class/merge_conflict.txt` | Simulating merge conflict via concurrent edits across branches on identical lines, inspecting conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`), manual conflict resolution, and completing the merge. | Missing |
| 6 | **devops lab5** (Git Rebase & Multi-Commit Sequences) | `devops lab5/file1.txt`<br>`devops lab5/file2.txt`<br>`devops lab5/file3.txt`<br>`devops lab5/abc.txt`<br>`devops lab5/bcd.txt`<br>`devops lab5/edf.txt` | Demonstrating sequential commit management (`commit 1` through `commit 5`), linear history rebasing (`git rebase`), and organizing multiple project files cleanly. | Missing |

---

## 4. Technical Stack & Environment
- **Languages**: C++ (compiled with `clang++` / `g++`), Markdown, Text / Shell
- **Version Control System**: Git version 2.x+
- **Host / Platform**: macOS Darwin (arm64) / GitHub
- **Dependencies**: Standard C++ Library (`<iostream>`), standard Git tools
- **Pre-existing files in target repo**:
  - `README.md` (0 bytes / empty) - Needs full project documentation
  - `login.txt` (Existing work from PR: "These changes had been done by Devyani..!!") - Preserved
