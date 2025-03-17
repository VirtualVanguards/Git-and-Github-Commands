# Git & GitHub Guide

## Global Setup
```sh
git config --global user.name "Manish Borikar"
git config --global user.email "manishborikar92@gmail.com"
git config --global core.editor "code --wait"
git config --global core.autocrlf "input"
```

## Edit Global Config
```sh
git config --global -e
```

## Viewing Commit History
```sh
git log --oneline      # Compact commit history

git log --oneline --graph  # Visualize branch structure
```

## Checking File Status
```sh
git status -s  # Show unstaged and staged files
```

## Resetting Commits
```sh
git reset --hard HEAD~1  # Completely remove last commit

git reset --soft HEAD~1  # Keep changes staged

git reset --mixed HEAD~1  # Keep changes unstaged
```
- `HEAD~(1,2,3,...)` determines how many commits to reset.

## Branching
### Creating a New Branch
```sh
git branch <branch_name>
# Example: git branch feature/nav
```

### Viewing Branches
```sh
git branch         # List local branches
git branch -a      # List all branches (local & remote)
```

### Switching Branches
```sh
git switch <branch_name>
# Example: git switch feature/nav
```
- Create and switch to a new branch:
```sh
git switch -c <branch_name>
# Example: git switch -c feature/nav
```

### Merging Branches
- Merging can only be done in the main branch:
```sh
git merge <branch_name>
# Example: git merge feature/nav
```

### Deleting a Branch
```sh
git branch -d <branch_name>
# Example: git branch -d feature/nav
```

## Git Stash
```sh
git stash       # Save changes temporarily
git stash apply # Restore stashed changes
```

## Cloning a Repository
```sh
git clone <repo_url>
# Example: git clone https://github.com/user/repository.git
```
- Clone a specific branch:
```sh
git clone --branch <branch_name> --single-branch <repo_url>
# Example: git clone --branch main --single-branch https://github.com/user/repository.git
```

## GitHub Contributions
### Initializing a Repository
```sh
git init                     # Initialize a new Git repository
git add .                    # Stage all changes
git commit -m "commit message" # Commit changes
git branch -M main           # Rename branch to 'main'
```
- Add a remote repository:
```sh
git remote add origin <repo_url>
# Example: git remote add origin https://github.com/user/repository.git
```
- Push changes:
```sh
git push -u origin main
```

### Pulling & Fetching Changes
```sh
git pull              # Pull latest changes from the remote repository
git pull origin main  # Pull changes from the main branch
git pull origin <branch_name> # Pull changes from a specific branch
git fetch origin      # Fetch changes without merging
```
- Rebase changes:
```sh
git rebase origin/main
```
- Reset to remote state:
```sh
git reset --hard origin/main
```

### Force Push and Other Options
```sh
git push --force origin main       # Force push changes to main branch (overwrites remote branch)
git push --force-with-lease origin main  # Safer force push to main branch (checks if remote branch changed)
git push origin --delete <branch_name>  # Delete a remote branch
```

### Remote Repository Management
```sh
git remote -v            # View remote repositories
git remote remove origin # Remove a remote repository
git remote set-url origin <new_url> # Change remote URL
git remote rename origin upstream  # Rename a remote repository
```

This guide provides essential Git and GitHub commands for effective version control and collaboration. 🚀