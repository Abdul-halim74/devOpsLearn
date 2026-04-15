#### 🔹 Task 1: Repository Initialization

git init
echo "# Project" > README.md
git add .
git commit -m "Initial commit"

git checkout -b develop
git checkout -b feature/login
git checkout main


### 🔹 Task 2: Branching Workflow
git checkout develop
git checkout -b feature/payment
git checkout develop
git checkout -b feature/profile
git checkout develop
git checkout -b bugfix/login-error

git checkout develop
git merge feature/payment

git checkout feature/profile
git rebase develop

git checkout develop
git merge feature/profile


### 🔹 Task 3: Commit History Management

git checkout -b feature/profile

git add .
git commit -m "Add profile UI"

git commit -am "Add profile controller"

git commit -am "Fix validation issue"

git commit -am "Update profile API"

git commit -am "Minor UI fix"

git rebase -i HEAD~5

pick a1b2c3 Add profile UI
pick b2c3d4 Add profile controller
pick c3d4e5 Fix validation issue
pick d4e5f6 Update profile API
pick e5f6g7 Minor UI fix

reword a1b2c3 Add profile UI
squash b2c3d4 Add profile controller
squash c3d4e5 Fix validation issue
squash d4e5f6 Update profile API
squash e5f6g7 Minor UI fix



 Explanation of:

   Merge vs Rebase

   | Feature | Merge              | Rebase          |
| ------- | ------------------ | --------------- |
| History | Preserve           | Rewrite         |
| Commit  | Extra merge commit | No merge commit |
| Safety  | Safe for teams     | Careful needed  |
| Style   | Tree-like          | Linear          |


Squash & Reword
| Feature     | Squash               | Reword                    |
| ----------- | -------------------- | ------------------------- |
| Purpose     | Multiple commits → 1 | Change commit message     |
| Code change | Yes (combined)       | No                        |
| History     | Simplified           | Same commits, new message |
