# 📖 Complete Guide to Git and GitHub

## 📌 Introduction to Git & GitHub

Git is a powerful version control system that helps developers track changes, collaborate, and manage projects efficiently.  
This guide covers essential Git commands and concepts in an easy-to-understand manner.

### 🌐 What is GitHub?

GitHub is a cloud-based platform that provides a remote repository service for Git projects.  
It enables developers to store, manage, and collaborate on code in a centralized manner.  
GitHub enhances Git by adding features like pull requests, issue tracking, and CI/CD integration.

---

## 🔍 Difference Between Git and GitHub

| Feature       | Git                                                 | GitHub                                                           |
|--------------|-----------------------------------------------------|-----------------------------------------------------------------|
| **Definition** | A version control system for tracking code changes. | A cloud-based platform for hosting Git repositories.             |
| **Functionality** | Manages local and remote repositories.              | Provides additional tools for collaboration and automation.      |
| **Hosting**   | No hosting; operates locally.                       | Provides hosting for repositories.                               |
| **Collaboration** | Requires manual repository sharing.                 | Allows teams to work together with built-in collaboration tools. |
| **GUI Support** | Command-line-based (CLI).                           | Provides a web interface and desktop apps.                       |

---

## 🛠 1️⃣ Understanding Git Basics

### 📂 Git Folder Structure

```
.git  -> A hidden folder that keeps history of files and sub-folders.
commit -> Acts like a checkpoint in the version history.
```

### 🔄 Git Workflow

```
Working Directory --(git add)--> Staging Area --(git commit)--> Local Repository --(git push)--> Remote Repository (GitHub/GitLab)
```

### 📝 Basic Git Commands

| Command                        | Description                                             |
|--------------------------------|---------------------------------------------------------|
| `git --version`                | Checks the installed Git version.                      |
| `git status`                   | Shows the status of your working directory.            |
| `git init`                     | Initializes a Git repository (run once per project).   |
| `git add <file_name>`          | Adds a file to the staging area.                       |
| `git add .`                    | Adds all files to the staging area.                    |
| `git commit -m "message"`      | Commits changes with a message.                        |
| `git log`                      | Shows commit history with details.                     |
| `git log --oneline`            | Displays commit history in a simplified format.        |
| `git config --list`            | Lists all current Git configurations.                  |
| `touch .gitignore`             | Creates a `.gitignore` file to specify untracked files.|

---

## 🌿 2️⃣ Working with Branches

### 🔀 What is a Git Branch?

A Git branch is like a separate workspace where you can work on new features or fixes without affecting the main project.

### 📌 Branch Commands

| Command                      | Description                                |
|-----------------------------|--------------------------------------------|
| `git branch`                | Lists all branches.                        |
| `git branch <branch_name>`  | Creates a new branch.                      |
| `git checkout <branch_name>` | Switches to the specified branch.          |
| `git merge <branch_name>`    | Merges a branch into the current branch.   |
| `git branch -d <branch_name>` | Deletes a merged branch.                   |

---

## 🔄 3️⃣ Rebase and Merge

⚠️ **NEVER run `git rebase` on `main/master`! It is for side branches only when necessary!**

### 📖 Understanding Git Rebase

- **Before Rebase:** Your branch is outdated.
- **After Rebase:** Your branch gets updated with the latest `main` changes, making history cleaner.

### 📌 Real-Life Example: Writing a Group Project Report

Imagine you and your friend are working on a group project report. The main document is in a shared Google Doc, and you make a copy to work on separately.

#### ✏️ Before Rebase:
- You start writing your section.
- Meanwhile, the main document gets updated.
- Your copy is now outdated.

#### 🔄 What Happens When You Run `git rebase main`?
- Git temporarily removes your changes.
- Git updates your branch with the latest version from `main`.
- Git reapplies your changes on top of the updated document.

#### ⚠️ Conflict Example (Merge Conflict)
- If both you and your teammate edited the same paragraph, Google Docs will highlight the conflict.
- In Git, this happens with merge conflicts. You must manually edit the file, save it, and run:

```
git add <file_name>
git rebase --continue
```

### 🔍 Why Use Rebase Instead of Merge?

| Method  | Pros | Cons |
|---------|------|------|
| Merge  | Keeps history but creates extra commits | History becomes messy |
| Rebase | Makes history cleaner | Requires careful handling |

✅ **If conflicts arise, run:**

```
git rebase --continue
```

---

## 🌍 4️⃣ Remote Configuration in Git

| Command | Description |
|---------|-------------|
| `git remote -v` | Shows the remote repositories linked to your local repo. |
| `git remote add origin <repo_url>` | Connects local repo to a remote repository. |
| `git push -u origin main` | Pushes changes and sets `main` as upstream. |
| `git pull origin main` | Pulls latest changes from the remote repository. |

---

## 🚀 5️⃣ Important GitHub Commands

| Command | Description |
|---------|-------------|
| `git clone <repo_url>` | Clones a GitHub repository. |
| `git fork` | Creates a copy of a repository on your GitHub account. |
| `git pull-request` | Submits changes to the original repo via a pull request. |
| `git remote set-url origin <new_repo_url>` | Changes the remote repository URL. |

---

## 🎯 Conclusion

This guide covers the most important Git and GitHub commands to help you manage your projects efficiently.  
Follow these best practices to keep your workflow smooth and organized. 🚀

## 👨‍💻 About the Author

**Anit Paul**  
BTech Student @ Sister Nivedita University  
Passionate about Backend Development & Problem-Solving.

### 💡 Need More Help?

Feel free to reach out for any queries or clarifications! 🎯
