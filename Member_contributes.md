## DO NOT  
**"Super important"**

- Don't Push directly to main 
- Donot use generic branch names like test1 or temp 
- Without understanding ctrl+c / ctrl+v 
    {make sure your confession is ready else we discard}

---

# POWERLINES PROJECT - CONTRIBUTION GUIDE 

We are following a strict CLI-first approach for working on this project. This guide walks through:

- Installing Git
- Setting up SSH keys
- Cloning the repository
- Creating branches for tasks
- Making changes and pushing them
- Submitting a Pull Request

---

## 1. INSTALLING GIT (FOR UBUNTU SYSTEMS with bash)

Make sure Git is installed before contributing.

sudo apt update && sudo apt install git 
git --version    # Verify Git installation

---

## 2. CONFIGURE GIT WITH YOUR GITHUB CREDENTIALS

Set your name and email (should match your GitHub account):

git config --global user.name "YourGitHubUsername" 
git config --global user.email "youremail@example.com"

To verify:

git config --global --list

---

## 3. GENERATE SSH KEY (RECOMMENDED METHOD FOR PUSHING CODE)

Instead of using HTTPS (which asks for username/password), we use SSH for secure and seamless interaction.

ssh-keygen -t ed25519 -C "youremail@example.com"

- Press Enter to accept the default file location: ~/.ssh/id_ed25519 
- Choose a passphrase (or leave it empty for simplicity) 

Then display the public key:

cat ~/.ssh/id_ed25519.pub

---

## 4. ADD SSH KEY TO YOUR GITHUB ACCOUNT

1. Copy the entire output from the above `cat` command 
2. Go to GitHub → Settings → SSH and GPG keys 
3. Click New SSH key 
4. Title:  Dev Machine 
5. Paste the public key 
6. Click Add SSH key

---

## 5. CLONE THE REPOSITORY

Clone the Powerlines repo using SSH:

git clone git@github.com:Mark-Phathomlezz/Powerlines.git 
cd Powerlines

---

## 6. CREATE A NEW BRANCH (ONE PER TASK / FEATURE)

Always create a new branch before starting a new feature or fix.

git checkout -b feature/your-name-taskname

Examples:

git checkout -b feature/xavier-auth-logic 
git checkout -b bugfix/john-dashboard-crash

---

## 7. MAKE CHANGES LOCALLY (USING CLI OR IDE)

Edit your files using your preferred editor (VSCode, Vim, etc.).

---

## 8. STAGE AND COMMIT CHANGES

Stage all changed files:

git add .

Then commit them with a meaningful message:

git commit -m "Add: login module for admin panel"

---

## 9. PUSH YOUR BRANCH TO GITHUB

git push origin feature/your-name-taskname

This creates a remote branch on GitHub.

---

## 10. CREATE A PULL REQUEST (PR)

1. Go to the Powerlines GitHub repository 
2. GitHub will detect your newly pushed branch and suggest a Pull Request 
3. Select: 
   - Base branch: main 
   - Compare: feature/your-name-taskname 
4. Add a clear title and description 
5. Click Create Pull Request

---

## 11. WAIT FOR REVIEW AND MERGE

A project maintainer will review your PR. 
- If approved: it gets merged into main 
- If feedback is given: make changes on the same branch and push again

---

## 12. SYNCING WITH MAIN BRANCH

Before starting any new feature, always make sure you're up-to-date:

git checkout main 
git pull origin main

Then create a new branch from main.

---

## SUMMARY CHECKLIST

- [ ] Git installed and configured 
- [ ] SSH key generated and added to GitHub 
- [ ] Repo cloned via SSH 
- [ ] Feature/task branch created 
- [ ] Local changes committed with clear message 
- [ ] Branch pushed to GitHub 
- [ ] Pull Request submitted and reviewed

---

This guideline will evolve with time. Please follow it strictly to maintain clean and collaborative workflows.
---


## 1. INSTALLING GIT FOR WINDOWS

1. Download Git from the official website: https://git-scm.com/download/win  
2. During installation:
   - Choose **"Git Bash Here"** for right-click context menu
   - Choose **"Use Git from Git Bash only"** (or the default recommended)
   - Keep SSH-related settings default

3. After installation, open **Git Bash**

To verify:
    git --version

---

## 2. CONFIGURE GIT WITH YOUR GITHUB CREDENTIALS

git config --global user.name "YourGitHubUsername"  
git config --global user.email "youremail@example.com"

To verify:

git config --global --list

---

## 3. GENERATE SSH KEY (FOR WINDOWS USERS)

Generate your SSH key:

ssh-keygen -t ed25519 -C "youremail@example.com"

- When prompted for a file to save the key, **press Enter** to accept the default:  
  `C:\Users\YourUsername\.ssh\id_ed25519`

- You can skip the passphrase (just press Enter twice)

Then copy the public key:

cat ~/.ssh/id_ed25519.pub

Copy the full output (you’ll paste this into GitHub in the next step)

---

## 4. ADD SSH KEY TO YOUR GITHUB ACCOUNT

1. Go to GitHub → Settings → SSH and GPG Keys  
2. Click **New SSH key**  
3. Title: `YourName Dev`  
4. Paste the SSH key you copied  
5. Click **Add SSH key**

---

## 5. TEST THE SSH CONNECTION TO GITHUB

ssh -T git@github.com

If successful, you will see:

> Hi your-username! You've successfully authenticated, but GitHub does not provide shell access.

---

## 6. CLONE THE REPOSITORY USING SSH

git clone git@github.com:Mark-Phathomlezz/Powerlines.git  
cd Powerlines

---

## 7. CREATE A NEW BRANCH FOR EACH TASK

git checkout -b feature/your-name-taskname

---

## 8. MAKE CHANGES LOCALLY

Use your favorite editor (e.g. VSCode or Notepad++) to make changes to files inside the cloned repo folder.

---

## 9. STAGE AND COMMIT CHANGES

git add .  
git commit -m "Add: your feature description"

---

## 10. PUSH CHANGES TO GITHUB

git push origin feature/your-name-taskname

---

## 11. CREATE A PULL REQUEST

1. Go to GitHub  
2. Open the repo  
3. GitHub will prompt you to create a Pull Request  
4. Choose base: `main`, compare: `feature/...`  
5. Submit the PR

---

## 12. KEEP YOUR MAIN BRANCH UPDATED

Before starting a new task:

git checkout main  
git pull origin main

---

## NOTES FOR WINDOWS USERS

- Git Bash emulates Unix paths — use `/c/Users/...` instead of `C:\Users\...`
- All git commands work the same as on Ubuntu
- File permissions and hidden folders (like `.ssh`) may be hidden in Windows Explorer
- Use **Git Bash only**, not CMD or PowerShell, for consistency with Linux users

---

## SUMMARY CHECKLIST

- [ ] Git installed from https://git-scm.com  
- [ ] Git Bash used for terminal commands  
- [ ] SSH key added to GitHub  
- [ ] Repo cloned using SSH  
- [ ] New branch created per task  
- [ ] Changes committed and pushed  
- [ ] Pull request submitted

---

## BRANCH NAMING EXAMPLES

| Type     | Example                     |
|----------|-----------------------------|
| Feature  | feature/alex-login-ui       |
| Bug Fix  | bugfix/jane-title-crash     |
| Docs     | docs/setup-instructions     |
| Hotfix   | hotfix/server-port-fix      |

---

Stick to Git Bash, one branch per task, and clear commit messages. This keeps collaboration smooth across systems.



