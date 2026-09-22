# MJB Logistics - Complete Deployment Guide

This guide will walk you through setting up GitHub version control and deploying your website to Vercel.

## Table of Contents
1. [GitHub Setup](#github-setup)
2. [Making Commits](#making-commits)
3. [Vercel Deployment](#vercel-deployment)
4. [Custom Domain Setup](#custom-domain-setup)
5. [Troubleshooting](#troubleshooting)

---

## GitHub Setup

### Step 1: Create a GitHub Account
If you don't have a GitHub account:
1. Go to [github.com](https://github.com)
2. Click "Sign up"
3. Follow the registration process
4. Verify your email

### Step 2: Create a New Repository

#### Via Web Interface:
1. Go to [github.com/new](https://github.com/new)
2. **Repository name**: `mjb-logistics` (or your preferred name)
3. **Description**: "Global Logistics Website - Professional Frontend"
4. Choose **Public** (to deploy on Vercel free tier)
5. Check "Add a README file" (optional, we already have one)
6. Click "Create repository"

#### Via Command Line:
```bash
# Navigate to your project folder
cd mjb-logistics

# Initialize Git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: MJB Logistics website setup"

# Add remote repository (replace USERNAME with your GitHub username)
git remote add origin https://github.com/USERNAME/mjb-logistics.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Install Git (If Not Already Installed)

**Windows:**
1. Download from [git-scm.com](https://git-scm.com/download/win)
2. Run installer and follow setup wizard
3. Choose default options

**Mac:**
```bash
# Using Homebrew
brew install git

# Or download from https://git-scm.com/download/mac
```

**Linux:**
```bash
# Ubuntu/Debian
sudo apt-get install git

# Fedora/Red Hat
sudo dnf install git
```

### Step 4: Configure Git

```bash
# Set your name and email
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Verify configuration
git config --global --list
```

---

## Making Commits

### Understanding Git Workflow

```
Working Directory → Staging Area → Repository (History)
   (Your Files)    (git add)      (git commit)
                                      ↓
                              (git push to GitHub)
```

### Best Practices for Commits

**Commit Often**: Make commits for logical chunks of work
**Meaningful Messages**: Use clear, descriptive commit messages
**One Issue Per Commit**: Each commit should address one task

### Commit Message Format

```
[TYPE] Brief description (50 chars max)

Optional detailed explanation (72 chars per line)
- Bullet points if needed
- Explain the "why" not the "what"
```

**Types:**
- `feat` - New feature
- `fix` - Bug fix
- `style` - CSS/styling changes
- `docs` - Documentation updates
- `refactor` - Code refactoring
- `test` - Test additions
- `chore` - Maintenance tasks

### Example Workflow

#### 1. Create Feature Branch
```bash
# Create and switch to new branch
git checkout -b feature/new-section

# Or using newer Git syntax
git switch -c feature/new-section
```

#### 2. Make Changes
```bash
# Edit your files in VS Code or your editor
# Example: Add new service section to services.html
```

#### 3. Stage Changes
```bash
# Stage specific file
git add services.html

# Or stage all changes
git add .

# View staged changes
git status
```

#### 4. Commit Changes
```bash
# Commit with message
git commit -m "feat: Add new premium logistics service"

# Or for longer commit messages
git commit -m "feat: Add premium logistics service

- Added new service card to services.html
- Updated service comparison table
- Added pricing information
- Responsive design included"
```

#### 5. Push to GitHub
```bash
# Push branch to GitHub
git push origin feature/new-section

# Or push to main branch (after merging locally)
git push origin main
```

### Common Git Commands

```bash
# Check status
git status

# View commit history
git log
git log --oneline
git log --graph --all --decorate

# View changes
git diff                    # Unstaged changes
git diff --staged          # Staged changes

# Undo changes
git checkout -- filename   # Discard changes in working directory
git reset HEAD filename    # Unstage file
git reset --soft HEAD~1    # Undo last commit, keep changes

# Switch branches
git checkout main          # Or: git switch main
git checkout -b new-branch # Create and switch

# Merge branches
git merge feature-branch

# Remove branch
git branch -d feature-branch
git push origin --delete feature-branch
```

### Branching Strategy

**Main Branch**: Production-ready code
**Development Branch**: Integration branch for features
**Feature Branches**: Individual feature development

```bash
# Example workflow
git checkout -b feature/contact-form  # Create feature branch
# ... make changes ...
git add .
git commit -m "feat: Improve contact form validation"
git push origin feature/contact-form

# Then create Pull Request on GitHub to merge into main
```

---

## Vercel Deployment

### Step 1: Create Vercel Account

1. Go to [vercel.com](https://vercel.com)
2. Click "Sign Up"
3. **Recommended**: Sign up with GitHub account (easier integration)
4. Authorize Vercel to access your GitHub account

### Step 2: Deploy from GitHub

#### Option A: Automatic Import
1. In Vercel dashboard, click "New Project"
2. Click "Import Git Repository"
3. Paste your GitHub repository URL:
   ```
   https://github.com/USERNAME/mjb-logistics
   ```
4. Click "Import"

#### Option B: Connect Account
1. Click "Continue with GitHub"
2. Select your repository from the list
3. Click "Import"

### Step 3: Configure Project

**Project Settings Screen:**
- **Framework Preset**: Select "Other" (for static HTML/CSS/JS)
- **Root Directory**: Leave as `.` (current directory)
- **Build Command**: Leave empty (not needed for static sites)
- **Output Directory**: Leave empty
- **Environment Variables**: Not needed for this project

Click "Deploy"

### Step 4: Wait for Deployment

Vercel will:
1. Build your project (usually < 1 minute)
2. Deploy to production
3. Provide you with a URL

**Your Live URL**: `https://mjb-logistics.vercel.app` (or custom)

### Step 5: Update Repository

Once deployed, update your files to reflect the live URLs:

**Update README.md:**
```markdown
## 🌐 Live Demo

**Website**: https://mjb-logistics.vercel.app

**GitHub Repository**: https://github.com/USERNAME/mjb-logistics
```

**Commit and push:**
```bash
git add README.md
git commit -m "docs: Add live deployment URLs"
git push origin main
```

---

## Custom Domain Setup

### Step 1: Purchase Domain

Purchase a domain from:
- GoDaddy
- Namecheap
- Google Domains
- Any DNS provider

### Step 2: Connect Domain to Vercel

**In Vercel Dashboard:**

1. Go to your project settings
2. Click "Domains"
3. Click "Add Domain"
4. Enter your domain (e.g., `mjblogistics.com`)
5. Click "Add"

### Step 3: Configure DNS

Vercel will provide DNS records:

**For Nameserver approach (easiest):**
1. Copy Vercel's nameservers
2. Go to your domain registrar
3. Update nameservers to Vercel's nameservers
4. Wait 24-48 hours for DNS propagation

**For CNAME/A Record approach:**
1. Copy the CNAME record provided by Vercel
2. In your registrar's DNS settings:
   - Create CNAME record pointing to Vercel
   - Create A records for IPv4 addresses
3. Wait for DNS propagation

### Step 4: Verify Domain

Once DNS is configured:
1. Vercel will automatically verify
2. Your custom domain is now live
3. HTTPS certificate is automatically provided

---

## Updating After Deployment

### Process

1. **Make Changes Locally**
   ```bash
   # Edit files in your editor
   git status  # View changes
   ```

2. **Stage and Commit**
   ```bash
   git add .
   git commit -m "feat: Update service descriptions"
   ```

3. **Push to GitHub**
   ```bash
   git push origin main
   ```

4. **Vercel Auto-Deploys**
   - Vercel automatically rebuilds
   - New version is live within seconds
   - Check deployment status in Vercel dashboard

---

## Troubleshooting

### Website Not Live
```
Problem: Vercel shows error after deployment
Solution:
1. Check project root contains index.html
2. Verify all file names and links are correct
3. Check Vercel build logs for errors
4. Ensure no circular redirects in links
```

### Git Push Issues
```
Problem: "fatal: Could not read from remote repository"
Solution:
1. Check SSH key is configured: ssh -T git@github.com
2. Or use HTTPS: git remote set-url origin https://github.com/USERNAME/repo.git
3. Verify credentials are saved
4. Check internet connection
```

### DNS Not Resolving
```
Problem: Custom domain shows "This site can't be reached"
Solution:
1. Wait 24-48 hours for DNS propagation
2. Clear browser cache and DNS cache
   - Windows: ipconfig /flushdns
   - Mac: sudo dscacheutil -flushcache
   - Linux: sudo systemd-resolve --flush-caches
3. Use https://www.whatsmydns.net to check propagation
4. Verify DNS records in domain registrar
5. Re-check nameservers in Vercel settings
```

### Performance Issues
```
Problem: Website loads slowly
Solution:
1. Optimize images (compress with TinyPNG)
2. Minify CSS and JavaScript
3. Enable Vercel Analytics
4. Check browser dev tools (Network tab)
5. Use lighthouse for audit
```

### Changes Not Appearing
```
Problem: Made changes but old content still shows
Solution:
1. Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
2. Clear browser cache
3. Wait for Vercel deployment to complete
4. Check deployment status in Vercel dashboard
5. Verify git push was successful: git log
```

---

## Advanced Topics

### Environment-Specific Deploys

**Preview Deployments:**
- Create feature branches
- Each PR gets a preview URL
- Test before merging to main

**Production:**
- Merge to main branch
- Automatic production deployment
- Revert by rolling back commits

### Monitoring and Analytics

**In Vercel Dashboard:**
1. **Analytics**: Real-time visitor stats
2. **Speed Insights**: Performance metrics
3. **Edge Network**: CDN status
4. **Environment Variables**: For future backend

### Collaboration

**For Team Projects:**
```bash
# Clone existing repository
git clone https://github.com/USERNAME/mjb-logistics.git
cd mjb-logistics

# Create your feature branch
git checkout -b feature/your-feature

# Make changes and push
git add .
git commit -m "feat: Your feature description"
git push origin feature/your-feature

# Create Pull Request on GitHub for review
```

---

## Deployment Checklist

- [ ] GitHub account created
- [ ] Repository created and initialized
- [ ] All project files committed with meaningful messages
- [ ] README.md completed
- [ ] .gitignore file added
- [ ] Repository pushed to GitHub
- [ ] Vercel account created
- [ ] Project imported to Vercel
- [ ] Build successfully deployed
- [ ] Live URL verified working
- [ ] Custom domain configured (optional)
- [ ] README updated with live URLs
- [ ] DNS propagation verified
- [ ] Final push to GitHub

---

## Quick Reference

### Essential Git Commands
```bash
git clone <url>           # Clone repository
git add .                 # Stage all changes
git commit -m "message"   # Create commit
git push origin main      # Push to GitHub
git pull origin main      # Pull latest changes
git status                # Check status
git log                   # View history
```

### Essential Vercel Commands
```bash
# Install Vercel CLI (optional)
npm install -g vercel

# Deploy from command line
vercel

# Check deployment status
vercel projects list
```

---

## Support Resources

- **GitHub Docs**: https://docs.github.com
- **Vercel Docs**: https://vercel.com/docs
- **Git Tutorial**: https://git-scm.com/book/en/v2
- **GitHub Learning Lab**: https://lab.github.com

---

**Last Updated**: December 2024  
**Version**: 1.0.0
