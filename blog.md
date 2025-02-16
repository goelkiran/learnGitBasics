# Git Basics Notes

## 1. Initialize a New Repository
- `git init` – Initializes a new Git repository in the current directory.

## 2. Configure User Information (One-Time Setup)
- `git config --global user.name "Your Name"` – Sets your global username.
- `git config --global user.email "your-email@example.com"` – Sets your global email.

## 3. Add and Check Remote Repository
- `git remote add origin <repo_url>` – Adds a remote repository (usually GitHub) and names it `origin`.
- `git remote -v` – Lists the currently configured remote repositories.
- `git remote set-url origin <new_repo_url>` – Updates the URL of an existing remote repository.

## 4. Create and Switch Branches
- `git branch <branch_name>` – Creates a new branch.
- `git checkout <branch_name>` – Switches to the specified branch.
- `git checkout -b <branch_name>` – Creates and switches to a new branch.
- `git branch` – Lists all local branches.

## 5. Track Changes and Commit
- `git status` – Displays the state of the working directory and staging area.
- `git add <file>` – Stages a specific file for commit.
- `git add .` – Stages all changes in the current directory.
- `git commit -m "Commit message"` – Commits the staged changes with a message.

## 6. Merge Branches
- `git merge <branch_name>` – Merges the specified branch into the current branch.
- **(Resolve conflicts if prompted, then run `git add` and `git commit` to finalize the merge.)**

## 7. Push Changes to Remote Repository
- `git push -u origin main` – Pushes the `main` branch to the remote repository and tracks it.
- `git push origin <branch_name>` – Pushes a specific branch to the remote repository.

## 8. Pull Latest Changes from Remote
- `git pull origin main` – Pulls the latest changes from the `main` branch.
- `git pull` – Pulls changes from the remote repository linked to the current branch.

## 9. Check SSH Connection and Set Up Authentication
- `ls ~/.ssh` – Lists existing SSH keys.
- `ssh-keygen -t ed25519 -C "your-email@example.com"` – Generates a new SSH key.
- `cat ~/.ssh/id_ed25519.pub` – Displays the public key (to add it to GitHub).
- `ssh -T git@github.com` – Tests the SSH connection.
- `git remote set-url origin git@github.com:your-username/your-repo.git` – Switches the remote URL to use SSH instead of HTTPS.

## 10. Check Branch and Repository Status
- `git branch` – Lists all branches.
- `git status` – Shows the current state of the working directory.
- `git log --oneline` – Shows a compact history of commits.

This guide organizes essential Git commands in a logical order for easy reference.
