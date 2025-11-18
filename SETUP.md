# Quick Setup Guide

## 🎯 Step-by-Step Instructions

### 1. Push Files to GitHub

```bash
git add .
git commit -m "Initial setup: GitHub Pages and repository protection"
git push origin main
```

### 2. Enable GitHub Pages

1. Go to: https://github.com/Satendra9984/privacy_policies/settings/pages
2. Under **Source**, select:
   - **Branch**: `main` (or `master` if that's your default branch)
   - **Folder**: `/ (root)`
3. Click **Save**
4. Wait 2-3 minutes for the site to deploy

Your site will be live at: **https://satendra9984.github.io/privacy_policies/**

### 3. Protect the Repository

#### A. Set Up Branch Protection

1. Go to: https://github.com/Satendra9984/privacy_policies/settings/branches
2. Click **Add rule**
3. Enter branch name: `main` (or `master`)
4. Enable these settings:
   - ✅ **Require a pull request before merging**
   - ✅ **Require status checks to pass before merging**
   - ✅ **Do not allow bypassing the above settings**
   - ✅ **Restrict who can push to matching branches** → Add yourself only
   - ✅ **Include administrators** (this protects you too!)

#### B. Disable External Contributions (Optional)

1. Go to: https://github.com/Satendra9984/privacy_policies/settings
2. Scroll to **Features** section
3. Uncheck:
   - ❌ **Issues**
   - ❌ **Pull requests**
   - ❌ **Discussions**

### 4. Verify Protection

- Try making a change directly on GitHub (should be blocked)
- Only you can push via command line or approved PRs
- Repository remains public for GitHub Pages

## ✅ Checklist

- [ ] Files pushed to GitHub
- [ ] GitHub Pages enabled
- [ ] Site accessible at GitHub Pages URL
- [ ] Branch protection rules configured
- [ ] External contributions disabled (optional)
- [ ] Tested: Can you still push changes? (You should be able to)

## 🎨 Adding Your First Privacy Policy

1. Copy the template:
   ```bash
   cp policies/template.html policies/my-app.html
   ```

2. Edit `policies/my-app.html` with your content

3. Add to `index.html`:
   ```html
   <div class="policy-card">
       <h3>My App</h3>
       <p class="description">Description of my app</p>
       <a href="policies/my-app.html" class="btn">View Policy</a>
   </div>
   ```

4. Commit and push:
   ```bash
   git add .
   git commit -m "Add privacy policy for My App"
   git push origin main
   ```

## 🔍 Troubleshooting

**Site not showing?**
- Wait 5-10 minutes
- Check repository is Public
- Verify Pages is enabled in Settings

**Can't push changes?**
- Check branch protection allows you
- Verify you're authenticated correctly
- Try: `git push origin main --force` (only if needed!)

---

**Need help?** Check the full README.md for detailed information.

