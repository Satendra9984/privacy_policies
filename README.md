# Privacy Policies Repository

This repository hosts privacy policies for all applications in one centralized location. The policies are publicly accessible via GitHub Pages.

🌐 **Live Site**: [https://satendra9984.github.io/privacy_policies/](https://satendra9984.github.io/privacy_policies/)

## 📋 Table of Contents

- [Repository Setup](#repository-setup)
- [Adding Privacy Policies](#adding-privacy-policies)
- [Protecting the Repository](#protecting-the-repository)
- [GitHub Pages Configuration](#github-pages-configuration)
- [File Structure](#file-structure)

## 🚀 Repository Setup

### Initial Setup

1. **Clone the repository** (if you haven't already):
   ```bash
   git clone https://github.com/Satendra9984/privacy_policies.git
   cd privacy_policies
   ```

2. **Push the initial files**:
   ```bash
   git add .
   git commit -m "Initial commit: GitHub Pages setup"
   git push origin main
   ```

## 📄 Adding Privacy Policies

1. Copy the template file:
   ```bash
   cp policies/template.html policies/your-app-name.html
   ```

2. Edit `policies/your-app-name.html` with your app's privacy policy content.

3. Add a card to `index.html` in the `.policies-grid` section:
   ```html
   <div class="policy-card">
       <h3>Your App Name</h3>
       <p class="description">Brief description of your app</p>
       <a href="policies/your-app-name.html" class="btn">View Policy</a>
   </div>
   ```

4. Commit and push:
   ```bash
   git add .
   git commit -m "Add privacy policy for [App Name]"
   git push origin main
   ```

## 🔒 Protecting the Repository

To ensure only you can make changes while keeping the repository public:

### 1. Branch Protection Rules

1. Go to your repository on GitHub
2. Click **Settings** → **Branches**
3. Under **Branch protection rules**, click **Add rule**
4. Set **Branch name pattern** to `main` (or `master`)
5. Enable the following:
   - ✅ **Require a pull request before merging**
     - Set **Required number of approvals**: `0` (since you're the only one)
     - ✅ **Require approvals** (if available)
   - ✅ **Do not allow bypassing the above settings**
   - ✅ **Include administrators** (this protects you too!)
   - ✅ **Require linear history** (optional, recommended)

**Note**: If "Restrict who can push to matching branches" is not available, the PR requirement combined with disabled PRs feature (see below) will effectively protect your repository.

### 2. Disable Issues and Pull Requests (RECOMMENDED)

This is the key step to prevent external contributions:

1. Go to **Settings** → **General**
2. Scroll to **Features**
3. Uncheck:
   - ❌ **Issues**
   - ❌ **Pull requests** ← **This is critical!** Prevents others from creating PRs
   - ❌ **Discussions**
   - ❌ **Wiki**

**Why this works**: By disabling Pull Requests, external users cannot create PRs. Since you're the owner, you can still push directly via command line (`git push origin main`), but the branch protection will prevent direct edits on GitHub.

### 3. Repository Visibility and Access

- Keep the repository **Public** (required for free GitHub Pages)
- **Do NOT add any collaborators** - keep it owner-only
- Only you will be able to push changes via command line
- Direct edits on GitHub will be blocked by branch protection

### 4. Additional Security

1. **Two-Factor Authentication**: Enable 2FA on your GitHub account
2. **Deploy Keys**: If using CI/CD, use deploy keys instead of personal access tokens
3. **Repository Settings**: Regularly review who has access in **Settings** → **Collaborators**

## 🌐 GitHub Pages Configuration

### Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under **Source**, select:
   - **Branch**: `main` (or `master`)
   - **Folder**: `/ (root)`
4. Click **Save**

### Custom Domain (Optional)

If you have a custom domain:

1. Add a `CNAME` file in the root directory:
   ```
   yourdomain.com
   ```
2. Configure DNS records with your domain provider
3. Enable **Enforce HTTPS** in GitHub Pages settings

### Access Your Site

Your site will be available at:
- `https://satendra9984.github.io/privacy_policies/`
- Or your custom domain if configured

**Note**: It may take a few minutes for changes to appear after pushing.

## 📁 File Structure

```
privacy_policies/
├── index.html              # Main landing page
├── styles.css              # Styling for all pages
├── README.md               # This file
├── .gitignore              # Git ignore rules
└── policies/
    ├── template.html       # Template for new privacy policies
    └── [app-name].html     # Individual privacy policy files
```

## 🔧 Troubleshooting

### GitHub Pages Not Updating

1. Check that the repository is **Public**
2. Verify GitHub Pages is enabled in Settings → Pages
3. Ensure `index.html` is in the root directory
4. Wait 5-10 minutes for changes to propagate
5. Clear your browser cache

### Branch Protection Issues

- If you can't push, check branch protection rules
- Ensure you're pushing to the correct branch (`main` or `master`)
- Verify you're authenticated with the correct GitHub account

## 📝 Notes

- This repository is public so GitHub Pages can serve it for free
- Branch protection ensures only you can make changes
- All privacy policies are static HTML files for easy maintenance
- The site is mobile-responsive and works on all devices

## 📧 Contact

For questions or issues, please contact the repository owner.

---

**Last Updated**: January 2025

