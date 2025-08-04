# GitHub CLI Login Instructions from Terminal (Linux - Ubuntu/Debian)

Run the following commands step by step in your terminal to install and log in to GitHub using the GitHub CLI (`gh`):


## ✅ Install GitHub CLI (gh) on Ubuntu/Debian
## 🛠️ Step 1: Add GitHub CLI package repository
## Run these commands one by one in your terminal:
```bash
type -p curl >/dev/null || sudo apt install curl -y

curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | \
  sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg

sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) \
signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] \
https://cli.github.com/packages stable main" | \
sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null

sudo apt update
sudo apt install gh -y
```
## Step 2: Authenticate with GitHub
```
gh auth login
```
Follow the prompts:
```
- Select: GitHub.com
- Protocol: HTTPS
- Authenticate in browser
```
## Step 3: Verify authentication
```
gh auth status
```
# -----------------------------

