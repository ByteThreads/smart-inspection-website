# Smart Inspection Check Website - Deployment Guide

## 🚀 Step-by-Step Deployment to GitHub Pages

### Step 1: Create GitHub Repository (2 minutes)

1. Go to **https://github.com/ByteThreads**
2. Click **"New repository"** (green button)
3. Fill in:
   - **Repository name:** `smart-inspection-website`
   - **Description:** "Official website for Smart Inspection Check iOS app"
   - **Visibility:** ✅ **Public** (required for free GitHub Pages)
   - **Initialize:** ❌ Do NOT initialize with README (we already have files)
4. Click **"Create repository"**

### Step 2: Push Code to GitHub (1 minute)

GitHub will show you commands. Use these:

```bash
cd "/Users/elkyratliff/Documents/Professional Business/smart-inspection-website"

# Add remote
git remote add origin https://github.com/ByteThreads/smart-inspection-website.git

# Push to GitHub
git push -u origin main
```

### Step 3: Enable GitHub Pages (1 minute)

1. On GitHub, go to your repository
2. Click **"Settings"** tab
3. Scroll down to **"Pages"** in left sidebar
4. Under **"Source"**:
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **"Save"**

GitHub will show: **"Your site is ready to be published at..."**

Wait 1-2 minutes, refresh the page. You'll see:
✅ **"Your site is published at https://bytethreads.github.io/smart-inspection-website/"**

### Step 4: Test the Site (1 minute)

Visit these URLs to confirm everything works:

- **Home:** https://bytethreads.github.io/smart-inspection-website/
- **Privacy:** https://bytethreads.github.io/smart-inspection-website/privacy-policy.html
- **Terms:** https://bytethreads.github.io/smart-inspection-website/terms-of-service.html

All pages should load with proper styling and navigation.

### Step 5: Configure Custom Domain (5 minutes)

Now point your domain (smartinspectioncheck.com) to GitHub Pages:

#### On GitHub:

1. Still in **Settings → Pages**
2. Under **"Custom domain"**, enter: `smartinspectioncheck.com`
3. Click **"Save"**
4. GitHub will check DNS... (may show error at first, that's normal)

#### On Your Domain Registrar (where you bought smartinspectioncheck.com):

You need to add DNS records. The steps vary by registrar, but here's what to add:

**Option A: Using A Records (Recommended)**

Add these 4 A records pointing to GitHub Pages:

```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

**Also add CNAME for www:**

```
Type: CNAME
Name: www
Value: bytethreads.github.io
```

**Common Registrars:**

- **Namecheap:** Dashboard → Domain List → Manage → Advanced DNS → Add New Record
- **Google Domains:** My domains → DNS → Custom records → Add
- **GoDaddy:** My Products → Domains → Manage → DNS → Add

#### Wait for DNS Propagation (5-30 minutes)

DNS changes can take 5-30 minutes to propagate. You can check status:

```bash
# Check if DNS is working
dig smartinspectioncheck.com
```

Should show the GitHub Pages IP addresses.

#### Enable HTTPS (1 minute)

Once DNS is working:

1. Go back to GitHub: **Settings → Pages**
2. You should see: ✅ **"DNS check successful"**
3. Check the box: ✅ **"Enforce HTTPS"**
4. Wait 1-2 minutes for SSL certificate

### Step 6: Verify Final URLs (1 minute)

Test all URLs work:

- ✅ https://smartinspectioncheck.com
- ✅ https://www.smartinspectioncheck.com (redirects to main)
- ✅ https://smartinspectioncheck.com/privacy-policy.html
- ✅ https://smartinspectioncheck.com/terms-of-service.html

---

## 📧 Update App Store Connect

Once your site is live, update App Store Connect:

### App Information:
- **Support URL:** https://smartinspectioncheck.com
- **Privacy Policy URL:** https://smartinspectioncheck.com/privacy-policy.html
- **Marketing URL:** https://smartinspectioncheck.com (optional)

---

## 🔄 Making Updates to the Website

Whenever you need to update the site:

```bash
cd "/Users/elkyratliff/Documents/Professional Business/smart-inspection-website"

# Edit your HTML files
# Then commit and push:

git add .
git commit -m "Update website content"
git push origin main
```

Changes go live in 1-2 minutes automatically!

---

## 🎨 Customizing the Site

### Update App Store Link (After Approval)

Once your app is approved, update `index.html`:

**Find this line:**
```html
<a href="#" class="cta-button">📱 Coming Soon to App Store</a>
```

**Replace with:**
```html
<a href="https://apps.apple.com/app/idYOUR_APP_ID" class="cta-button">📱 Download on App Store</a>
```

Get your App Store link from App Store Connect after approval.

### Add Screenshots (Optional)

Create an `images/` folder and add screenshots:

```bash
mkdir images
# Add your screenshots to images/ folder
git add images/
git commit -m "Add app screenshots"
git push origin main
```

Then update `index.html` to include images.

---

## 📊 Analytics (Optional - v1.1)

To track website visitors, you can add:

- **Google Analytics** (free)
- **Plausible** (privacy-friendly, paid)
- **Simple Analytics** (privacy-friendly, paid)

Just add their tracking code to `<head>` section of all HTML files.

---

## 🐛 Troubleshooting

### "404 Page Not Found"
- Wait 1-2 minutes for GitHub Pages to deploy
- Check Settings → Pages shows "Your site is live"
- Clear browser cache

### "DNS_PROBE_FINISHED_NXDOMAIN" (Custom Domain)
- DNS not propagated yet, wait 30 minutes
- Check DNS records are correct
- Use `dig smartinspectioncheck.com` to verify

### "Not Secure" Warning
- Wait for HTTPS certificate (can take 30 minutes)
- Ensure "Enforce HTTPS" is checked in Settings → Pages
- DNS must be working first

### CSS Not Loading
- Check file paths in HTML (should be relative: `./style.css` not `/style.css`)
- Clear browser cache
- Check all files committed to GitHub

---

## ✅ Deployment Checklist

- [ ] Create GitHub repository (public)
- [ ] Push code to GitHub
- [ ] Enable GitHub Pages
- [ ] Test bytethreads.github.io URL works
- [ ] Add DNS records for custom domain
- [ ] Wait for DNS propagation (5-30 min)
- [ ] Enable HTTPS
- [ ] Test smartinspectioncheck.com works
- [ ] Test all pages load (home, privacy, terms)
- [ ] Update App Store Connect URLs
- [ ] Bookmark for future updates

---

## 📞 Need Help?

**GitHub Pages Docs:** https://docs.github.com/en/pages
**DNS Help:** Contact your domain registrar support

**Questions?** contact@bytethreadsllc.com

---

**Total Time:** 15-45 minutes (most is waiting for DNS)

© 2025 ByteThreads LLC. All rights reserved.
