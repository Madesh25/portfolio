# 🔐 Admin Panel Guide

This guide explains how to use the admin panel to manage your portfolio content.

## Accessing the Admin Panel

**URL:** `https://yoursite.com/aman/`

**Default Password:** `madesh@aman2025`

> ⚠️ **Security Note:** The password is encrypted with SHA-256 hash in the code. Only the hash is visible, not the actual password.

---

## Admin Panel Features

### 1. Projects Management

Add, edit, or delete your projects:

| Field | Description | Example |
|-------|-------------|---------|
| Title | Project name | "CI/CD Pipeline" |
| Status | Current status | "Operational" or "In Progress" |
| Description | Brief description | "Automated deployment pipeline..." |
| Responsibilities | Key achievements (one per line) | "Reduced deployment time by 50%" |
| Tags | Technologies used | "Docker, Kubernetes, Jenkins" |
| Image URL | Project image | "images/project1.png" |

### 2. Blogs Management

Add, edit, or delete blog posts:

| Field | Description | Example |
|-------|-------------|---------|
| Title | Blog title | "How to Deploy with Docker" |
| Category | Topic category | "DevOps" or "Tutorial" |
| Excerpt | Short preview | "Learn the basics of..." |
| Read Time | Estimated time | "5 min read" |
| Status | Draft or Published | "Published" |

### 3. Experience Management

Add, edit, or delete work experience:

| Field | Description | Example |
|-------|-------------|---------|
| Job Title | Your role | "DevOps Engineer" |
| Company | Company name | "Tech Corp" |
| Start Date | When you started | "Jan 2023" |
| End Date | When you left/Present | "Present" |
| Responsibilities | What you did (one per line) | "Managed CI/CD pipelines" |

---

## How Data is Stored

### localStorage (Browser Storage)
- When you add/edit/delete items in admin, changes are saved to **localStorage**
- This means changes are **browser-specific**
- If you use a different browser or clear cache, changes are lost

### JSON Files (Permanent Storage)
- Original data is in `/content/` folder:
  - `projects.json`
  - `blogs.json`
  - `experience.json`
- These serve as **fallback** if localStorage is empty

### Making Changes Permanent

To permanently save changes:
1. Make changes in admin panel
2. Update the corresponding JSON file manually
3. Push to GitHub

---

## Security Features

### Password Hashing
The password is stored as a SHA-256 hash:
```javascript
// Only the hash is in the code, not the password
const correctHash = '911b8831f3ccaba1c2e6615ea5f2cfc443a3e8b43d7da5b96aa38e8445bbc65d';
```

### Session Storage
- Login state is stored in `sessionStorage`
- Automatically logs out when browser tab is closed

### Changing the Password

1. Generate a new SHA-256 hash:
```bash
echo -n 'your-new-password' | sha256sum | cut -d' ' -f1
```

2. Replace the hash in `aman/index.html`:
```javascript
const correctHash = 'YOUR_NEW_HASH_HERE';
```

3. Push to GitHub

---

## Tips

1. **Use the same browser** - localStorage is browser-specific
2. **Backup your JSON files** - Before making major changes
3. **Test locally first** - Before pushing to production
4. **Keep admin URL private** - Don't share `/aman/` publicly

---

**← Previous:** [Deployment Guide](DEPLOYMENT.md) | **Next:** [Customization Guide](CUSTOMIZATION.md) →
