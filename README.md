# 🛠️ Git & GitHub: Master Command Reference

A systematic guide for version control workflows, from basic setup to advanced history management.

---

## 🏗️ 1. Setup & Repository Initialization
Commands for starting a new project or configuring your environment.

* **Check Version:** `git --version`
* **Initialize Repo:** `git init` (Creates a hidden `.git` folder)
* **Clone Project:** `git clone <url>`
* **View Hidden Files:** `ls -a` (To see the `.git` directory)
* **Navigation:** * `mkdir local-repo` (Create a folder)
    * `cd ..` (Move to parent directory)

---

## 🔄 2. The Core Workflow
Git moves files through four categories: **Untracked**, **Tracked**, **Added (Staged)**, and **Committed**.

### **The Standard Cycle**
1. **Check Status:** `git status`
2. **Add Files:** * `git add <filename>` (Single file)
    * `git add .` (All files)
3. **Commit:** `git commit -m "Your descriptive message"`
4. **Push:** `git push origin main`

---

## 🌐 3. Remote Management
Connecting your local work to GitHub.

* **Add Remote:** `git remote add origin <url>`
* **Verify Remote:** `git remote -v`
* **First Push:** `git push -u origin main` (Sets default upstream)
* **Pull Updates:** `git pull origin main` (Sync local with remote)

---

## 🌿 4. Branching & Merging
Used for "Feature-based" development to keep the main code stable.

| Command | Action |
| :--- | :--- |
| `git branch` | List all local branches |
| `git branch -m main` | Rename current branch to "main" |
| `git checkout -b <name>` | Create and switch to new branch |
| `git checkout <name>` | Switch to an existing branch |
| `git diff main` | Compare current branch changes with main |
| `git merge main` | Merge main into your current feature branch |
| `git branch -d <name>` | Delete a completed branch |
| `git push origin <name>` | Push a specific feature branch to remote |

---

## ⏪ 5. Inspecting History & Undoing Changes
Commands for viewing the past and fixing mistakes.

* **View History:** `git log` (Shows commit hashes/IDs)
* **Unstage Files:** * `git reset <filename>` (Removes from "Added" state)
    * `git reset` (Unstages everything)
* **Undo Last Commit:** `git reset head~1` (Keeps your code but removes the commit)
* **Hard Reset:** `git reset --hard <commit-hash>`  
  > **⚠️ Warning:** This permanently deletes uncommitted changes and reverts your code to the specified commit.

---

### 🚀 Summary Workflow
**Clone** $\rightarrow$ **Checkout Branch** $\rightarrow$ **Add** $\rightarrow$ **Commit** $\rightarrow$ **Push**