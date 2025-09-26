# Save the Git Workflow Notes into a .txt file for the user

content = """# 📘 Git Workflow Notes (EC2 + GitHub)

This document summarizes the Git commands and workflows I practiced on **EC2** with my repositories.

---

## 1️⃣ System Setup

# Update packages
sudo yum update -y

# Install Git
sudo yum install git

# Verify installation
git --version

# Configure Git user
git config --global user.name "Khushal Bhavsar"
git config --global user.email "khushalbhavsar41@gmail.com"

# Check config
git config --list

---

## 2️⃣ Work with First Repo (`Demorepo`)

# Clone repo
git clone https://github.com/Khushal41/Demorepo.git
cd Demorepo

# Create a file
nano hello.py

# Check status
git status

# Add & commit file
git add hello.py
git commit -m "Initial Commit"

# Push to main branch
git push origin main

### 🔄 Updating Repo

# Pull latest changes
git pull

# Delete files
rm *.py

# Stage deletions
git add -u
git commit -m "Deleted unnecessary Python files"
git push origin main

---

## 3️⃣ Branch Management

# Create new branches
git branch staging
git branch prod

# List branches
git branch

# Switch to branch
git checkout prod

# Add commits to prod
git add .
git commit -m "Commit on prod"
git push origin prod

# Push to staging
git push origin staging

---

## 4️⃣ Work with Second Repo (`myrepo`)

# Clone another repo
git clone https://github.com/atulkamble/myrepo.git
cd myrepo

# Create new branch
git branch khushal
git checkout khushal

# Add files
touch khushal.txt
nano khushal.txt

# Stage & commit
git add khushal.txt
git commit -m "Khushal Commit"

# Push to remote branch
git push origin khushal

---

## 5️⃣ Useful Commands

# Check status
git status

# Check commit history
git log

# Show remote branches
git branch -a

# Show remote URLs
git remote -v

---

## ⚡ Common Mistakes to Avoid

- git staus ❌ → ✅ git status
- git cheakout prod ❌ → ✅ git checkout prod
- git logn / git logs ❌ → ✅ git log
- git origin prod ❌ → ✅ git push origin prod

---

✅ With this workflow, I managed multiple branches (`main`, `staging`, `prod`, `khushal`) and pushed commits successfully from EC2.
"""
