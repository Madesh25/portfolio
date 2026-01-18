# 🚀 Deployment Guide

This guide explains how to deploy your portfolio to Cloudflare Pages for **FREE hosting**.

## Why Cloudflare Pages?

- ✅ **Free forever** - No credit card required
- ✅ **Fast global CDN** - Your site loads fast worldwide
- ✅ **Automatic HTTPS** - Secure by default
- ✅ **Custom domains** - Use your own domain
- ✅ **Auto-deploy** - Updates when you push to GitHub

## Prerequisites

1. A GitHub account ([Sign up](https://github.com/))
2. A Cloudflare account ([Sign up](https://dash.cloudflare.com/sign-up))
3. Your portfolio code pushed to GitHub

---

## Step 1: Push Code to GitHub

### Initialize Git (if not already done)
```bash
cd portfolio
git init
git add .
git commit -m "Initial commit"
```

### Create GitHub Repository
1. Go to [github.com/new](https://github.com/new)
2. Name your repository (e.g., `portfolio`)
3. Keep it **Public** or **Private** (both work with Cloudflare)
4. Click "Create repository"

### Push to GitHub
```bash
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
git branch -M main
git push -u origin main
```

---

## Step 2: Connect to Cloudflare Pages

1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. Click **"Workers & Pages"** in the left sidebar
3. Click **"Create application"**
4. Click **"Pages"** tab
5. Click **"Connect to Git"**

### Configure Build Settings

| Setting | Value |
|---------|-------|
| Framework preset | **None** |
| Build command | *(leave empty)* |
| Build output directory | *(leave empty)* |
| Root directory | `/` |

6. Click **"Save and Deploy"**

Wait 1-2 minutes for deployment...

🎉 **Your site is now live!**

---

## Step 3: Get Your Live URL

After deployment, you'll get a URL like:
```
https://your-project.pages.dev
```

## Step 4: Add Custom Domain (Optional)

### If you own a domain (e.g., madesh.online):

1. In Cloudflare Pages, go to your project
2. Click **"Custom domains"** tab
3. Click **"Set up a custom domain"**
4. Enter your domain (e.g., `madesh.online`)
5. Follow the DNS setup instructions

### DNS Configuration
Add these records at your domain registrar:

| Type | Name | Value |
|------|------|-------|
| CNAME | @ | your-project.pages.dev |
| CNAME | www | your-project.pages.dev |

---

## Automatic Deployments

Every time you push to GitHub, Cloudflare will automatically redeploy:

```bash
# Make changes to your code
git add .
git commit -m "Updated projects"
git push origin main

# Wait ~1 minute, your live site is updated!
```

---

## Troubleshooting

### "Build failed"
- Make sure you selected "None" as framework preset
- Leave build command empty (it's a static site)

### "Domain not working"
- DNS propagation takes 5-48 hours
- Check DNS settings are correct

### "Old version still showing"
- Clear your browser cache (Ctrl+Shift+R)
- Wait a few minutes for Cloudflare to update

---

**← Previous:** [Setup Guide](SETUP.md) | **Next:** [Admin Panel Guide](ADMIN.md) →
