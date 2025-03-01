---
title: "Basics of Version Control with GitHub (2025/03/01)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no17-github-version-control )](https://github.com/takehika0129/no17-github-version-control )


# **Concept**
GitHub provide a structured way to track changes, collaborate, and release updates. This guide walks you through a step-by-step Git Flow, ensuring a clean and organized workflow.


# **Step-by-Step Guide to GitHub Version Control**
1️⃣ **Setup the Repository**
Before we start, we need to initialize a Git repository and connect it to GitHub.
```sh
mkdir test_repo
git init  # Initialize a new Git repository
git remote add origin https://github.com/<your-username>/<your-repo-name>.git  # Connect local repo to GitHub
```


2️⃣ **Create Main and Develop Branches**
To maintain a clean workflow, we separate stable and development code.
```sh
git checkout -b main  # Create and switch to the main branch
git commit --allow-empty -m "Initial commit on main"  # Create an empty commit for the main branch
git push -u origin main  # Push the main branch to GitHub

git checkout -b develop  # Create and switch to the develop branch
git commit --allow-empty -m "Initialize develop branch"  # Create an empty commit for the develop branch
git push -u origin develop  # Push the develop branch to GitHub
```
- `main` contains stable, production-ready code.
- `develop` is where new features and changes are tested before being released.


3️⃣ **Work on a New Feature**
Every new functionality is developed in its own `feature` branch.
```sh
git checkout -b feature/new-feature develop  # Create and switch to a feature branch from develop
echo "This is a test." > README.md  # Sample file
git add .  # Stage all modified files
git commit -m "Implement new feature"  # Commit with a meaningful message
git push -u origin feature/new-feature  # Push the feature branch to GitHub
```
- Keeping each feature in its own branch prevents conflicts with other changes.
- You can work independently without affecting the main development branch.


4️⃣ **Merge the Feature into Develop**
Once the `feature` is complete, it needs to be merged into `develop`.
```sh
git checkout develop  # Switch to the develop branch
git merge feature/new-feature  # Merge the completed feature into develop
git push origin develop  # Push the updated develop branch to GitHub
git branch -d feature/new-feature  # Delete the local feature branch.
git push origin --delete feature/new-feature  # Delete the remote feature branch.
```
- This keeps `develop` updated with the latest features.
- Cleaning up branches prevents unnecessary clutter in the repository.


5️⃣ **Prepare for a Release**
Once the project is stable, we create a `release` branch to finalize the update.
```sh
git checkout -b release/1.0.0 develop  # Create a release branch from develop
# Finalize the release (fix minor issues, update documentation, etc.)
git add .  # Stage all changes
git commit -m "Final tweaks for release v1.0.0"  # Commit final updates
git push -u origin release/1.0.0  # Push the release branch to GitHub
```
- `release` branch locks the version so no new features are added.
- This branch is used for testing and last-minute fixes before deployment.


6️⃣ **Merge Release into Main and Develop**
Once everything is ready, the `release` is merged into `main` and `develop`.
```sh
git checkout main  # Switch to main
git merge release/1.0.0  # Merge the release into main
git push origin main  # Push the updated main branch
git checkout develop  # Switch back to develop
git merge release/1.0.0  # Merge the release back into develop
git push origin develop  # Push the updated develop branch
git branch -d release/1.0.0  # Delete the local release branch
git push origin --delete release/1.0.0  # Delete the remote release branch
```
- `main` is now updated with the stable release.
- Merging back into `develop` ensures all bug fixes stay in future versions.


7️⃣ **Apply a Hotfix (Urgent Bug Fix in Main)**
If a critical issue is found in production, we need to fix it immediately.
```sh
git checkout -b hotfix/urgent-bug-fix main  # Create a hotfix branch from main
# Apply the fix, then commit and push
git add .  # Stage changes
git commit -m "Fix urgent bug in production"  # Commit the fix
git push -u origin hotfix/urgent-bug-fix  # Push the hotfix branch to GitHub
```
Hotfixes skip `develop` and are applied directly to `main` to fix the issue quickly.


8️⃣ **Merge Hotfix into Main and Develop**
Once `hotfix` is verified, it should be merged into both `main` and `develop`.
```sh
git checkout main  # Switch to main
git merge hotfix/urgent-bug-fix  # Merge the hotfix into main
git push origin main  # Push the updated main branch
git checkout develop  # Switch to develop
git merge hotfix/urgent-bug-fix  # Merge the hotfix into develop
git push origin develop  # Push the updated develop branch
git branch -d hotfix/urgent-bug-fix  # Delete the local hotfix branch
git push origin --delete hotfix/urgent-bug-fix  # Delete the remote hotfix branch
```
- `main` gets fixed immediately to prevent further issues.
- `hotfix` is also merged into develop to prevent regression in future updates.


# **Future Improvements**
- **Small Project Practice**: Apply this Git Flow to a simple project to get hands-on experience with version control.
- **Enforce Workflow Rules**: Set up branch protection rules on GitHub to maintain a clean and structured development process.


---
[Back to All Prototypes](../index.md)
