# Quick Start - Deploy Your Website in 15 Minutes

## ✅ What's Ready

Your website is complete and ready to deploy:

- ✅ **Landing page** (index.html) - Features, pricing, beautiful design
- ✅ **Privacy Policy** (privacy-policy.html) - Legal disclosure for AI services
- ✅ **Terms of Service** (terms-of-service.html) - Complete terms
- ✅ **Git repository** initialized with all files committed

## 🚀 3 Simple Steps to Go Live

### Step 1: Create GitHub Repo (2 minutes)

1. Go to https://github.com/ByteThreads
2. Click "New repository"
3. Name: `smart-inspection-website`
4. Make it **Public**
5. Do NOT initialize (we have files already)
6. Create repository

### Step 2: Push Your Code (30 seconds)

```bash
cd "/Users/elkyratliff/Documents/Professional Business/smart-inspection-website"

git remote add origin https://github.com/ByteThreads/smart-inspection-website.git
git push -u origin main
```

### Step 3: Enable GitHub Pages (1 minute)

1. On GitHub → Settings → Pages
2. Source: **main** branch, **/ (root)** folder
3. Click Save
4. Wait 2 minutes
5. Visit: https://bytethreads.github.io/smart-inspection-website/

**Done! Your site is live!**

---

## 🌐 Add Custom Domain (Optional - 10 minutes)

### On GitHub:
Settings → Pages → Custom domain: `smartinspectioncheck.com`

### On Your Domain Registrar:
Add these DNS records:

```
Type: A, Name: @, Value: 185.199.108.153
Type: A, Name: @, Value: 185.199.109.153
Type: A, Name: @, Value: 185.199.110.153
Type: A, Name: @, Value: 185.199.111.153
Type: CNAME, Name: www, Value: bytethreads.github.io
```

Wait 10-30 minutes for DNS, then your site will be at:
✅ https://smartinspectioncheck.com

---

## 📱 For App Store Connect

Use these URLs:

- **Support URL:** https://smartinspectioncheck.com
- **Privacy Policy:** https://smartinspectioncheck.com/privacy-policy.html

---

## 📄 Full Instructions

See `DEPLOYMENT_GUIDE.md` for complete step-by-step instructions.

---

**Questions?** contact@bytethreadsllc.com

© 2025 ByteThreads LLC
