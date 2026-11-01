# DevOps Lab 1: Git Basics & First Commit

## Aim
To understand the fundamentals of Version Control using Git, including repository initialization, file staging, initial commit creation, tracking modifications, and inspecting working tree status.

## Concepts & Commands
1. **Repository Setup**: Initializing or cloning a project directory.
   ```bash
   git init
   ```
2. **Checking Status**: Inspecting untracked and staged files.
   ```bash
   git status
   ```
3. **Staging Changes**: Moving changes to the index.
   ```bash
   git add hello.txt
   ```
4. **Committing Changes**: Capturing a snapshot with a descriptive message.
   ```bash
   git commit -m "initial commit"
   ```
5. **Modifying Tracked Files**: Editing `hello.txt` to include new lines and reviewing differences.
   ```bash
   git diff hello.txt
   git commit -am "made a modification"
   ```

## Files in this Experiment
- `hello.txt`: Introductory text file modified across commits to demonstrate git change tracking.

## Expected Output
```text
Hello world
this is dev tiwary
this is the first devops experiment!

i have made a modification!
```

