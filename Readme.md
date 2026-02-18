## This is my README File

---

Before starting any Git commands, make sure you have a working repository created under your GitHub account (either empty or existing).

## 1. Initialize Git

```bash
git init
git branch
```

> Use `git branch` to verify the current branch (usually master or main).

---

## 2. Set up username and email (one-time setup)

```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

---

## 3. Check commit status

```bash
git status
```

---

## 4. Add files

Add a single file:

```bash
git add <file_name>
git status
```

Add all files:

```bash
git add .
git status
```

---

## 5. Commit changes

```bash
git commit -m "commit message"
git status
```

---

## 6. Rename master to main

```bash
git branch -M main
git branch
```

---

## 7. Add remote repository

```bash
git remote add origin https://github.com/username/repository.git
git remote -v
```

This defines where your commits will be pushed.

---

## 8. Push to GitHub

```bash
git push -u origin main
```

---

## 9. Modify and push changes

If you modify files locally:

```bash
git add .
git status
git commit -m "new commit message"
git push origin main
```

To restore a file:

```bash
git restore README.md
```

---

# Cloning a Repository

## 1. Clone repository

```bash
git clone <repository_url>
```

## 2. Make changes after cloning

```bash
cd <repository_folder>
git status
git add .
git commit -m "commit message"
git push origin main
```

---

# Branching and Merging

## Create and switch branch

```bash
git branch <branch_name>
git checkout <branch_name>
```

Or in one step:

```bash
git checkout -b <branch_name>
```

## Merge branch to main

```bash
git checkout main
git merge <branch_name>
git push origin main
```

---

# Viewing Logs

```bash
git log
git log -p -3
```

---

# Resolving Merge Conflicts

After a merge conflict:

```bash
git pull
```

Open the conflicted file and remove conflict markers:

```
<<<<<<< HEAD
Your code
=======
Incoming code
>>>>>>> branch_name
```

Manually resolve, then:

```bash
git add .
git commit -m "resolved conflict"
git push origin main
```
