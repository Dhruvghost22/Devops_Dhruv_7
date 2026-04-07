# Devops_Dhruv_7
This is for Practical
Author - Dhruv
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<p>
  # 🔹 STEP 1: Setup
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list

# 🔹 STEP 2: Create Local Repository
mkdir devops-lab
cd devops-lab
git init
git branch -m master main

# 🔹 STEP 3: Create Files
echo "Hello World" > newfile.txt
echo "Ignore this file" > ignore.txt

# 🔹 STEP 4: Ignore File
echo "ignore.txt" > .gitignore

# 🔹 STEP 5: Status + Commit
git status
git add .
git commit -m "Initial commit"
git log

# 🔹 STEP 6: Connect to GitHub
git remote add origin https://github.com/username/devops-lab.git
git remote -v
git pull origin main
git push -u origin main

# 🔹 STEP 7: Modify File
echo "New Line Added" >> newfile.txt
git diff
git add newfile.txt
git commit -m "Updated file"
git push origin main

# 🔹 STEP 8: Staging Control
git add newfile.txt
git reset newfile.txt
git reset

# 🔹 STEP 9: Clone Repo
cd ..
git clone https://github.com/username/devops-lab.git
cd devops-lab

# 🔹 STEP 10: Branching
git branch mergebranch
git branch rebasebranch
git branch -a

# 🔹 STEP 11: Work on mergebranch
git checkout mergebranch
echo "Merge branch work" > merge.txt
git add .
git commit -m "Work on merge branch"
git push origin mergebranch

# 🔹 STEP 12: Work on rebasebranch
git checkout rebasebranch
echo "Rebase branch work" > rebase.txt
git add .
git commit -m "Work on rebase branch"
git push origin rebasebranch

# 🔹 STEP 13: Merge Branch
git checkout main
git pull origin main
git branch --merged
git merge mergebranch
git push origin main

# 🔹 STEP 14: Rebase
git checkout main
echo "Main update" >> newfile.txt
git add .
git commit -m "Main update before rebase"
git rebase rebasebranch

# (If conflict occurs)
git add .
git rebase --continue

# 🔹 STEP 15: Push All Branches
git push --all origin

# 🔹 STEP 16: Delete Branch
git branch --merged
git branch -d mergebranch
git branch -a
git push origin --delete mergebranch

# 🔹 STEP 17: Undo Changes (before commit)
git checkout newfile.txt

# 🔹 STEP 18: Amend Commit
git commit --amend -m "Updated commit message"
echo "Extra change" >> newfile.txt
git add .
git commit --amend

# 🔹 STEP 19: Cherry Pick
git log
git checkout rebasebranch
git cherry-pick <commit-hash>

# 🔹 STEP 20: Reset Commands
git reset --soft HEAD~1
git reset HEAD~1
git reset --hard HEAD~1

# 🔹 STEP 21: Clean Untracked Files
git clean -df

# 🔹 STEP 22: Recover Lost Data
git reflog
git checkout <commit-hash>
git branch backup
git checkout backup

# 🔹 STEP 23: Revert Commit
git revert HEAD
git diff HEAD HEAD~1

# 🔹 STEP 24: Remove Remote
git remote remove origin

# 🔹 STEP 25: Remove Git Tracking
rm -rf .git
</p>
