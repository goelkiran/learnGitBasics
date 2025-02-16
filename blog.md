# 📌 Git Basics - Commands & Descriptions

## 🔹 Git Commands for Repository Setup & Branch Management

| Command | Description |
|---------|------------|
| `git init` | Initializes a new Git repository in the current directory. |
| `git clone <repo_url>` | Clones a remote repository to your local machine. |
| `git status` | Shows the current state of the working directory and staging area. |
| `git branch` | Lists all local branches in the repository. |
| `git branch user-kiran` | Creates a new branch called `user-kiran`. |
| `git checkout user-kiran` | Switches to the `user-kiran` branch. |
| `git checkout -b user-kiran` | Creates and switches to the `user-kiran` branch in one step. |
| `git add <file>` | Stages a specific file for commit. |
| `git add .` | Stages all changes (new, modified, deleted files) for commit. |
| `git commit -m "Message"` | Commits the staged changes with a descriptive message. |
| `git log --oneline --graph --all` | Shows a compact history of commits across all branches. |
| `git remote -v` | Displays the remote repository URL(s) linked to your local repo. |
| `git push origin user-kiran` | Pushes the `user-kiran` branch to the remote repository. |
| `git pull origin user-kiran` | Fetches and merges the latest changes from `user-kiran` branch on remote. |
| `git merge user-kiran` | Merges `user-kiran` branch into the current branch. |
| `git merge --abort` | Cancels a merge if conflicts arise and need to be undone. |
| `git push origin main` | Pushes the `main` branch to the remote repository. |
| `git checkout main` | Switches back to the `main` branch. |
| `git fetch` | Downloads changes from the remote repository without merging them. |
| `git diff` | Shows changes between the working directory and the last commit. |
| `git reset --hard HEAD` | Resets all uncommitted changes to the last commit. |
| `git stash` | Temporarily saves changes without committing them. |
| `git stash pop` | Restores the stashed changes. |

## 🔹 Notes
- If you need to track a branch for future pushes, use:  
  ```bash
  git push -u origin user-kiran
  ```
- To resolve merge conflicts, manually edit the conflicting files, then run:
  ```bash
  git add <file>
  git commit -m "Resolved merge conflict"
  ```

This serves as a handy reference for learning Git basics. 🚀
