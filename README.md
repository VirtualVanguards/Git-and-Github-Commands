# Git & Github (What Matter's)

## Global Setup
    git config --global user.name "Manish Borikar"
    git config --global user.email "manishborikar92@gmail.com"
    git config --global core.editor "code --wait"
    git config --global core.autocrlf "input"

## Edit Global Setup
    git config --global -e

## Current Status of Saved Points
    git log --oneline
    git log --oneline --graph

## Current Status of Unstaged and Staged Files
    git status -s

## Going Back to Stage with Reset
    git reset --hard HEAD~1
        --hard Means Completely Vanish till Stage 
        --soft
        --mixed

        HEAD~(1,2,3,4.....) Determine How Many Stages Want to Reset

## Branching
### Create Branch
    git branch "branch name"
    e.g git branch feature/nav

### View Branches
    git branch
    git branch -a
    -a means All Branches

### Switch Branches
    git switch "branch name"
    e.g. git switch feature/nav

    Create and Switch Branch
    git switch -c "branch name"
    e.g. git switch -c feature/nav

### Merge Branches
    Can be done in main branch only
    git merge "branch name"
    e.g. git merge feature/nav

### Delete Branches
    git branch -d "branch name"
    e.g. git branch -d feature/nav

### Git Stash
    git stash (Save Changes) 
    git stash apply (Apply Changes)
    
## Github Contribution
### Github Setup
    git init (if you want to initialize the repository)
    git add . (if you want to add the changes to the staging area)
    git commit -m "message" (if you want to commit the changes)
    git branch -M main (if you want to rename the branch)
    git remote add origin https://github.com/VirtualVanguards/Git-and-Github-Commands.git (if you want to add the remote repository)
    git push -u origin main (if you want to push the changes to the remote repository)

    git pull (if you want to pull the changes from the remote repository, pull same as github)
    git pull origin main (if you want to pull the changes from main branch)
    git pull origin "branch name" (if you want to pull the changes from the specific branch)

    git clone https://github.com/VirtualVanguards/Git-and-Github-Commands.git (if you want to clone the remote repository)
    
    git remote -v (if you want to view the remote repository)
    git remote remove origin (if you want to remove the remote repository)
    git remote set-url origin "url" (if you want to change the url of the remote)
    git remote rename origin upstream (if you want to change the name of the remote)
    git remote rename origin origin (if you want to change the name of the remote)

    