# 🚀 Git Collaboration Demo

This is my first GitHub repository where I demonstrate **Git & GitHub basics** along with a **starter project using HTML, CSS, and JavaScript**.  

The goal of this repo is:  
✅ Show my understanding of Git concepts (init, commits, branches, merges, stashing).  
✅ Practice standard workflows for collaboration.  
✅ Provide a simple frontend template that others can contribute to.  

---

## 📂 Project Structure
```bash
git-collaboration-demo/
│
├── index.html # Main HTML file
├── style.css # Basic styling
├── script.js # JavaScript starter file
└── README.md # Git notes + project details
```
---

## 🌐 Project Overview
- **index.html** → A simple webpage with a heading and linked CSS/JS.  
- **style.css** → Adds basic styles for layout & readability.  
- **script.js** → Contains starter JavaScript code (console log + simple function).  

👉 This acts as a **starter template** for anyone learning Git + frontend basics.  

---

## 🔑 Git Basics (Quick Notes)

### 1️⃣ Why `git init`?
When you create a folder, Git doesn’t know it.  
`git init` initializes Git so it can track file changes and save history.

### 2️⃣ File States
- **Untracked** → New file (Git doesn’t know it).  
- **Tracked** → Git monitors this file.  
- **Modified** → Changed but not staged.  
- **Staged** → Marked for commit.  
- **Committed** → Saved checkpoint in Git history.  

### 3️⃣ Useful Commands
- `git status -s` → Shows file states (`??`, `M`, `A`).  
- `git log --oneline --graph` → Shows history in short form + graph.  

### 4️⃣ Simple Example
```bash
# Initialize Git
git init

# Create file
echo "Hello Git" > file.txt

# Stage & Commit
git add file.txt
git commit -m "First commit: added file.txt"

# Check history
git log --oneline --graph
```
---
## 🔄 Merging Techniques

### 🔹 Fast Forward Merge

- Used when the target branch has no new commits.

- Git just moves the pointer forward (no merge commit).

### 🔹 Three-Way Merge

- Used when both branches have commits.

- Git creates a new merge commit to combine work.
---
## ⚔️ Handling Merge Conflicts

When two branches change the same line, Git asks you to resolve manually.

Steps:
1. Open conflicted file.

2. Edit & keep correct changes.

3. git add + git commit → Conflict resolved.
   
---

## 🌿 Branching

- Create → git switch -C feature

- Switch → git switch main

- Delete → git branch -d feature
  
---

## 📦 Stashing

Temporarily save work without committing:
``` bash
git stash
git switch main
git stash apply
git stash clear
```
---
## 👥 Collaboration Workflow

#### 🔹 Step 1: Clone the Repository (Collaborator / Owner first setup)
```bash
git clone https://github.com/PranavAdhau/git-essentials-demo.git
cd git-essentials-demo
```
---
#### 🔹 Step 2: Work on a Feature Branch
```bash
git switch -C feature/adding-marque-effect
git add .
git commit -m "Added marquee feature"
git push -u origin feature/adding-marque-effect
```

---
#### 🔹 Step 3: Merge Feature into Main
```bash
git fetch
git switch feature/adding-marque-effect
git switch main
git merge feature/adding-marque-effect
git push origin main
```
---

#### 🔹 Common Steps for Teams

- The main branch owner creates the repo and initial files, then pushes to GitHub.

- Owner adds collaborators on GitHub.

- Each collaborator clones the repo.

- Everyone must create their own branch, do coding there, commit & push.

- After work is done, notify teammates.

- A teammate (or owner) fetches and merges into main.


---

👨‍💻 Author: Pranav Adhau
📅 Created On: September 2025