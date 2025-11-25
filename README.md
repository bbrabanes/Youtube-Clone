
## 📎 Appendix — Quick Command Cheat Sheet
```bash
# Init & first commit
git init
git add .
git commit -m "feat: initial commit"

# Connect to remote
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main

# Daily flow
git switch -c feature/awesome-thing   # create/switch
git add . && git commit -m "feat: awesome thing"
git push origin feature/awesome-thing
git pull origin main                  # keep up to date
git merge main                        # merge new changes into your branch

# Review & merge on GitHub → update local
git switch main && git pull origin main

# Ignore secrets
echo "JWT_SECRET=..." > .env
echo -e ".env\n.env.*\n*.env\n*.local\n*.key" >> .gitignore
git rm --cached .env                  # if accidentally committed
```
---

**Pro tip:** Keep `.env` out of Git, share a `.env.example`, and rotate secrets immediately if they leak.
