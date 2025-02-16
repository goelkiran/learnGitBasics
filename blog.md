# Git Basics Notes

# From the Linux Command Line
## 1. Initialize a New Repository
- `git init` – Initializes a new Git repository in the current directory.

## 2. Configure User Information (One-Time Setup)
- `git config --global user.name "Your Name"` – Sets your global username.
- `git config --global user.email "your-email@example.com"` – Sets your global email.
- `git config --list` – Displays the current Git configuration settings.

## 3. Add and Check Remote Repository
- `git remote -v` – Lists the currently configured remote repositories.
- `git remote add origin <repo_url>` – Adds a remote repository (usually GitHub) and names it `origin`.
- `git remote set-url origin <new_repo_url>` – Updates the URL of an existing remote repository.

## 4. Check SSH Connection and Set Up Authentication
- `ls ~/.ssh` – Lists existing SSH keys.
- `ssh-keygen -t ed25519 -C "your-email@example.com"` – Generates a new SSH key.
- `cat ~/.ssh/id_ed25519.pub` – Displays the public key (to add it to GitHub).
- `ssh -T git@github.com` – Tests the SSH connection.
- `git remote set-url origin git@github.com:your-username/your-repo.git` – Switches the remote URL to use SSH instead of HTTPS.

## 5. Create and Switch Branches
- `git branch` – Lists all local branches.
- `git branch <branch_name>` – Creates a new branch.
- `git checkout <branch_name>` – Switches to the specified branch.
- `git checkout -b <branch_name>` – Creates and switches to a new branch.

## 6. Track Changes and Commit
- `git status` – Displays the state of the working directory and staging area.
- `git add <file>` – Stages a specific file for commit.
- `git add .` – Stages all changes in the current directory.
- `git commit -m "Commit message"` – Commits the staged changes with a message.

## 7. Merge Branches
- `git status` – Check for any uncommitted changes before merging.
- `git merge <branch_name>` – Merges the specified branch into the current branch.
- **(Resolve conflicts if prompted, then run `git add` and `git commit` to finalize the merge.)**

## 8. Push Changes to Remote Repository
- `git status` – Ensure all changes are committed before pushing.
- `git push -u origin main` – Pushes the `main` branch to the remote repository and tracks it.
- `git push origin <branch_name>` – Pushes a specific branch to the remote repository.

## 9. Pull Latest Changes from Remote
- `git pull origin main` – Pulls the latest changes from the `main` branch.
- `git pull` – Pulls changes from the remote repository linked to the current branch.

## 10. Check Branch and Repository Status
- `git branch` – Lists all branches.
- `git status` – Shows the current state of the working directory.
- `git log --oneline` – Shows a compact history of commits.
- `git log --oneline main..user-goel` – Shows commits in `user-goel` that are not in `main`. It also tells how much your branch is ahead or behind `main`.
- `git log --oneline origin/main..user-goel` – Shows commits in `user-goel` that are not in `origin/main`, i.e., what is yet to be pushed.

## 11. Creating and Merging a Pull Request

### From the Command Line
- `git checkout user-goel` – Switch to the feature branch.
- `git push origin user-goel` – Push the branch to GitHub.
- `git log --oneline main..user-goel` – Verify unmerged changes.
- `git log --oneline origin/main..user-goel` – Verify what changes have not been pushed to the remote repository.

### From the Browser
#### Creating a Pull Request from the `user-goel` Branch
1. Go to **GitHub → Your Repository**.
2. Click on **Pull Requests** → **New Pull Request**.
3. In the **base branch**, select `main`.
4. In the **compare branch**, select `user-goel`.
5. Review changes and click **Create Pull Request**.

#### Merging the Pull Request
1. Open the newly created pull request.
2. Review the changes, checking for conflicts.
3. Click **Merge Pull Request** to integrate changes into `main`.
4. Optionally, delete the `user-goel` branch after merging.
