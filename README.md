# Changes-and-Commit


# Staging and Committing Changes
# 1. Stage all changes:
git add .
# 2. Commit with a meaningful commit message:
git commit -m "Your meaningful commit message here"


# Moving Commits to the Correct Branch
# 1. Switch to the correct branch (create it if it doesn't exist):
git checkout correct-branch
# If the branch doesn't exist:
git checkout -b correct-branch
# 2. Cherry-pick the commits from the wrong branch:
git cherry-pick <commit-hash1> <commit-hash2> ...
# 3. Switch back to the wrong branch and reset to the previous state:
git checkout wrong-branch
git reset --hard HEAD~n  # n is the number of commits to undo


# Creating and Pushing a New Branch
# 1. Create and switch to a new branch:
git checkout -b new-branch
# 2. Make changes and commit them:
# Make your changes
git add .
git commit -m "Commit message for new branch"
# 3. Push the new branch to the remote repository:
git push origin new-branch


# Contributing to an Open-Source Project on GitHub
# 1. Fork the repository on GitHub.
# 2. Clone your forked repository:
git clone https://github.com/your-username/repo-name.git
cd repo-name
# 3. Add the original repository as an upstream remote:
git remote add upstream https://github.com/original-username/repo-name.git
# 4. Create a new branch for your changes:
git checkout -b feature-branch
# 5. Make changes and commit them:
git add .
git commit -m "Description of changes"
# 6. Push the changes to your fork:
git push origin feature-branch
# 7. Create a pull request from your branch on GitHub.


# Resolving Merge Conflicts
# 1. Fetch and merge changes from the main branch:
git fetch origin
git checkout main
git pull
git checkout your-branch
git merge main
# 2. Resolve conflicts manually in the files.
# 3. Stage the resolved files:
git add resolved-file1 resolved-file2
# 4. Continue the merge process:
git commit


# Creating a Feature Branch Based on the Latest Main Branch
# 1. Fetch the latest changes:
git fetch origin
# 2. Switch to the main branch and pull the latest changes:
git checkout main
git pull origin main
# 3. Create and switch to the new feature branch:
git checkout -b feature-branch
# Reverting to a Specific Commit
# 1. Revert to a specific commit:
git reset --hard <commit-hash>
# 2. Force push to the remote repository (if necessary):
git push origin main --force


# Restoring a Deleted File
# 1. Find the commit where the file existed:
git log -- <file-path>
# 2. Checkout the file from the specific commit:
git checkout <commit-hash> -- <file-path>
# 3. Commit the restored file:
git add <file-path>
git commit -m "Restore deleted file"
