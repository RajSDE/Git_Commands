# 🚀 Git Commands Cheat Sheet

_A complete reference for essential Git commands_


## 🔧 Setup & Configuration
```bash
git config --global user.name "Your Name"          # Set global username
git config --global user.email "your@email.com"    # Set global email
git config --global core.editor "code --wait"      # Set VSCode as editor
git config --list                                 # Show all configurations
```

## 📂 Repository Management
```bash
git init                                        # Initialize new repo
git clone <repo_url>                            # Clone a repository
git clone -b <branch> <repo_url>                # Clone specific branch
git remote -v                                   # List remote connections
git remote add origin <repo_url>                # Add remote repository
```

## 🌿 Branching Workflow
```bash
git branch                                      # List local branches
git branch -a                                   # List all branches (local + remote)
git checkout -b <new_branch>                    # Create & switch to new branch
git switch <branch>                             # Switch branch (Git 2.23+)
git branch -d <branch>                          # Delete local branch
git push origin --delete <branch>               # Delete remote branch
git push -u origin <branch>                     # Push & set upstream
```

## 📝 Staging & Committing
```bash
git status                                      # Show working tree status
git add <file>                                  # Stage specific file
git add .                                       # Stage all changes
git add -p                                      # Stage changes interactively
git commit -m "message"                         # Commit with message
git commit --amend                              # Amend last commit
git reset HEAD <file>                           # Unstage file
git restore <file>                              # Discard changes in file
git restore --staged <file>                     # Unstage file
```

## 🔄 Remote Synchronization
```bash
git fetch                                       # Download objects/refs
git fetch --prune                               # Prune stale remote branches
git pull                                        # Fetch + merge
git pull --rebase                               # Fetch + rebase
git push                                        # Push to remote
git push -f                                     # Force push (use with caution)
```

## ⏪ Undoing Changes
```bash
git reset --soft HEAD~1                         # Undo commit (keep changes staged)
git reset --mixed HEAD~1                        # Undo commit (keep changes unstaged)
git reset --hard HEAD~1                         # Discard commit and changes
git revert <commit_hash>                        # Create undo commit
git clean -fd                                   # Remove untracked files/dirs
```

## 📦 Stashing
```bash
git stash                                       # Stash changes
git stash push -m "message"                     # Stash with message
git stash list                                  # List stashes
git stash pop                                   # Apply last stash
git stash apply stash@{n}                       # Apply specific stash
git stash drop                                  # Delete last stash
git stash clear                                 # Clear all stashes
```

## 🔍 Inspection & Comparison
```bash
git log                                         # Show commit history
git log --oneline --graph --all                 # Compact visual history
git show <commit_hash>                          # Show commit details
git diff                                        # Unstaged changes
git diff --staged                               # Staged changes
git diff <branch1>..<branch2>                   # Compare branches
git blame <file>                                # Show file line history
```

## 🔀 Merging & Rebasing
```bash
git merge <branch>                              # Merge into current branch
git merge --abort                               # Abort merge
git rebase <branch>                             # Rebase current branch
git rebase --abort                              # Abort rebase
git rebase -i HEAD~3                            # Interactive rebase
git cherry-pick <commit_hash>                   # Apply specific commit
```

## 🏷 Tagging
```bash
git tag                                         # List tags
git tag -a v1.0 -m "Version 1.0"               # Create annotated tag
git push origin v1.0                            # Push tag to remote
git tag -d v1.0                                 # Delete local tag
git push origin --delete v1.0                   # Delete remote tag
```

## 🛠 Advanced Commands
```bash
git bisect start                                # Binary search for bugs
git reflog                                      # Show reference logs
git worktree add ../new_dir branch              # Add worktree
git submodule add <repo_url>                    # Add submodule
git gc                                          # Cleanup unnecessary files
```

## 💡 Pro Tips
- Use `git fetch` + `git diff origin/main` before merging
- `git commit --fixup=<commit>` for quick fix commits
- `git rebase -i --autosquash` for automatic fixup squashing
- `git log -p <file>` to see changes to specific file
- `git grep "pattern"` to search codebase

## 🚨 Emergency Commands
```bash
git fsck --full                                 # Check repository integrity
git reflog expire --expire=now --all            # Clean reflog
git gc --prune=now --aggressive                 # Force cleanup
```


