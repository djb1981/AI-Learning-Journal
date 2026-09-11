# Git Basics - Learning Notes

## Objective

Understand the basic Git workflow and connect a local repository with GitHub.

---

# Git Architecture

Git works in three stages:

```text
Working Directory
       ↓
Staging Area
       ↓
Repository (Commit History)
```

---

# Step 1 - Configure Git

Check existing configuration:

```bash
git config --global --list
```

Set username:

```bash
git config --global user.name "YourName"
```

Set email:

```bash
git config --global user.email "your-email@example.com"
```

Verify:

```bash
git config --global --list
```

---

# Step 2 - Create Local Repository

Navigate to project folder:

```bash
cd C:\Learning\AI-Learning-Journal
```

Initialize Git:

```bash
git init
```

Result:

```text
Initialized empty Git repository
```

---

# Step 3 - Create First File

Create:

```text
README.md
```

Add initial content.

---

# Step 4 - Check Status

```bash
git status
```

Purpose:

Shows files tracked and untracked by Git.

Example:

```text
Untracked files:
README.md
```

---

# Step 5 - Stage Changes

```bash
git add .
```

Purpose:

Move all current modifications into the staging area.

Think:

```text
Working Area → Staging Area
```

Verify:

```bash
git status
```

Expected:

```text
Changes to be committed
```

---

# Step 6 - Commit Changes

```bash
git commit -m "Initial learning journal"
```

Purpose:

Create a permanent snapshot.

Think:

```text
Staging Area → Commit History
```

Verify:

```bash
git log --oneline
```

Example:

```text
1e07ff0 Initial learning journal
```

---

# Step 7 - Modify Existing File

Edit README.md:

```markdown
## Day 1

Started learning Git.
```

Check differences:

```bash
git diff
```

Purpose:

Compare current file with last commit.

---

# Step 8 - Commit Additional Changes

```bash
git add .
git commit -m "Added Day 1 git learning notes"
```

Verify:

```bash
git log --oneline
```

Example:

```text
6065f8e Added Day 1 git learning notes
184831a Added Day 1 notes
1e07ff0 Initial learning journal
```

---

# Step 9 - Connect GitHub Repository

Add remote repository:

```bash
git remote add origin https://github.com/<username>/<repository>.git
```

Verify:

```bash
git remote -v
```

Example:

```text
origin fetch
origin push
```

---

# Step 10 - Authenticate GitHub

Configure Git Credential Manager:

```bash
git config --global credential.helper manager
```

Push repository:

```bash
git push -u origin master
```

GitHub opens authentication page.

Approve:

```text
Authorize Git Credential Manager
```

Result:

Repository synchronized with GitHub.

---

# Validation Commands

Check current status:

```bash
git status
```

Check commit history:

```bash
git log --oneline
```

Check configured remotes:

```bash
git remote -v
```

Check file differences:

```bash
git diff
```

---

# Daily Workflow

For regular learning activities:

```bash
git status
git add .
git commit -m "Meaningful message"
git push
```

Example:

```bash
git commit -m "Completed AI Fundamentals Module 1"
```

---

# Key Learnings

- Git tracks file changes over time.
- `git add` stages files.
- `git commit` creates a checkpoint.
- `git push` uploads commits to GitHub.
- GitHub stores repository history remotely.
- Git Credential Manager simplifies authentication.

---

# Practical Use Case

While learning:

- AI
- Azure
- System Design
- TOGAF
- AI Agents

Store notes as Markdown documents and commit regularly.

This repository becomes:

- Knowledge Base
- Learning Journal
- Portfolio
- Interview Preparation Material