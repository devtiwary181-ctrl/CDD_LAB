# DevOps Lab 2: Remote Repositories & Cloning

## Aim
To link a local repository to a remote GitHub repository, push code files, and clone the remote repository into a secondary local directory to verify multi-environment setup.

## Concepts & Commands
1. **Writing C++ Source**:
   Creating a program (`code.cpp`) to test build, compilation, and execution.
   ```bash
   clang++ code.cpp -o code
   ./code
   ```
2. **Connecting Remote Repository**:
   ```bash
   git remote add origin https://github.com/devtiwary181-ctrl/CDD_LAB.git
   ```
3. **Pushing Code**:
   ```bash
   git add "devops lab2/code.cpp"
   git commit -m "Code Push in Remote Repo"
   git push -u origin main
   ```
4. **Cloning the Remote Repository**:
   Simulating team collaboration by cloning into a separate folder:
   ```bash
   mkdir "cloning folder" && cd "cloning folder"
   git clone https://github.com/devtiwary181-ctrl/CDD_LAB.git
   ```

## Files in this Experiment
- `code.cpp`: C++ source file printing developer name and push confirmation.
- `cloning folder/read.txt`: Verification note of repository cloning.
- `cloning folder/cdd_lab/`: Cloned repository instance verifying remote fetch and file integrity.

## Execution Output
```text
$ ./code
My name is Dev Tiwary.
Pushing my code to Remote repository in Github!
```

