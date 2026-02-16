
# Git Assignment

## Question 1

### Step 1: Create a new Git repository

```bash
git init
```

### Step 2: Create a file and commit changes

```bash
echo "Hello Git" > file.txt
git add file.txt
git commit -m "Initial commit"
```

### Step 3: View the commit history

```bash
git log
```

### Step 4: Modify the file

Edit the file using any editor and add some content.

### Step 5: Check file status

```bash
git status
```

The file will be shown as **modified and unstaged**.

### Step 6: Stage and commit the changes

```bash
git add file.txt
git commit -m "Updated file"
```

### Step 7: Clone the GitHub repository

```bash
git clone <repository-url>
```

### Step 8: Fetch changes

```bash
cd <repository-folder>
git fetch
```

### Step 9: Pull changes

```bash
git pull
```

---

## Question 2

### Step 1: Clone the repository

```bash
git clone <repository-url>
```

### Step 2: Create a new branch

```bash
git branch new-branch
```

### Step 3: Switch to the new branch

```bash
git checkout new-branch
```

### Step 4: Modify code

Make some changes in the project files.

### Step 5: Commit changes

```bash
git add .
git commit -m "Changes in new branch"
```

### Step 6: Switch back to original branch

```bash
git checkout main
```

### Step 7: Merge the new branch

```bash
git merge new-branch
```

### Step 8: Push changes

```bash
git push origin main
```

---

## Question 3

### Step 1: Create a feature branch

```bash
git branch feature-branch
```

### Step 2: Switch to feature branch

```bash
git checkout feature-branch
```

### Step 3: Modify the file

Make changes in the file.

### Step 4: Add and commit

```bash
git add .
git commit -m "Feature changes"
```

### Step 5: Push feature branch

```bash
git push origin feature-branch
```

### Step 6: Create a Pull Request

Create a PR from the feature branch to the main branch in GitHub.

### Step 7: Simulate another user

Switch to main branch and make changes to the same file.

```bash
git checkout main
```

### Step 8: Commit and push

```bash
git add .
git commit -m "Main branch changes"
git push origin main
```

### Conflict Resolution using Rebase

```bash
git checkout feature-branch
git rebase main
```

Resolve conflicts manually in the file, then:

```bash
git add .
git rebase --continue
git push --force
```

---

## Question 4

### Step 1: Create a feature branch

```bash
git checkout -b feature-branch
```

### Step 2: Make multiple commits

```bash
# First change
git add .
git commit -m "First change"

# Second change
git add .
git commit -m "Second change"

# Third change
git add .
git commit -m "Third change"
```

### Step 3: Identify commits

```bash
git log
```

### Step 4: Switch to target branch

```bash
git checkout main
```

### Step 5: Cherry-pick commits

```bash
git cherry-pick <commit-hash>
```

---

## Question 5

### Step 1: Create a feature branch

```bash
git checkout -b feature-branch
```

### Step 2: Make multiple commits

```bash
git add .
git commit -m "Commit 1"

git add .
git commit -m "Commit 2"

git add .
git commit -m "Commit 3"
```

### Step 3: View commit history

```bash
git log
```

### Step 4: Reset to a specific commit

```bash
git reset --hard <commit-hash>
```

### Step 5: Verify reset

```bash
git log
```

### Step 6: Identify commit to revert

```bash
git log
```

### Step 7: Revert a commit

```bash
git revert <commit-hash>
```

### Step 8: Verify revert

```bash
git log
```

---

## Difference Between Git Reset and Git Revert

| Git Reset                               | Git Revert                           |
| --------------------------------------- | ------------------------------------ |
| Removes commits from history            | Creates a new commit to undo changes |
| Rewrites commit history                 | Keeps history intact                 |
| Used for local changes                  | Safe for shared repositories         |
| Can cause data loss if used incorrectly | Safe and recommended in teams        |

---

## Conclusion

This assignment demonstrates core Git operations such as repository creation, branching, merging, rebasing, cherry-picking, resetting, and reverting. These concepts are essential for version control and collaborative software development.

