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

### Switch Branches
    git switch "branch name"
    e.g. git switch feature/nav