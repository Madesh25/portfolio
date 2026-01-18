# 🎨 Customization Guide

This guide explains how to customize the portfolio to make it your own.

## Quick Customization Checklist

- [ ] Update personal information in HTML files
- [ ] Replace profile image
- [ ] Update resume PDF
- [ ] Modify color scheme
- [ ] Update social links
- [ ] Update contact form email
- [ ] Change admin password

---

## 1. Personal Information

### Update Your Name & Title
Edit each HTML file and find the header section:
```html
<!-- In index.html, about.html, etc. -->
<title>Your Name - Your Title</title>
```

### Update Bio Text
Edit `about.html` to change your bio and skills.

### Update Social Links
Find the social links section and update:
```html
<a href="https://linkedin.com/in/YOUR_USERNAME">LinkedIn</a>
<a href="https://github.com/YOUR_USERNAME">GitHub</a>
```

---

## 2. Images

### Profile Image
1. Add your image to `/images/` folder
2. Update the path in HTML files:
```html
<img src="images/your-image.jpg" alt="Your Name">
```

### Favicon
Replace `images/DcZrecPWYZKbhOIPYCEMLzuVvF4.png` with your icon.

---

## 3. Resume

### Update Resume PDF
1. Add your resume to `/resume/` folder
2. Name it `Madeshwaran_Resume.pdf` (or update the path in `about.html`)

---

## 4. Color Scheme

The CSS uses CSS variables for easy theming. Edit the `:root` section in any HTML file:

```css
:root {
    --color-bg: #09090b;        /* Background color */
    --color-green: #00ff6a;     /* Primary accent (green) */
    --color-cyan: #00ffff;      /* Secondary accent (cyan) */
    --color-text: #a8d7e7;      /* Text color */
    --color-border: #1d2025;    /* Border color */
    --color-purple: #c084fc;    /* Purple accent */
}
```

### Example: Change to Blue Theme
```css
:root {
    --color-green: #00b4ff;     /* Change green to blue */
    --color-cyan: #60efff;      /* Lighter blue */
}
```

---

## 5. Contact Form

### Update Email
1. Go to [web3forms.com](https://web3forms.com/)
2. Create a new access key with YOUR email
3. Update `contact.html`:
```html
<input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
```

---

## 6. Content Data

### Projects (`content/projects.json`)
```json
{
  "projects": [
    {
      "id": 1,
      "title": "Your Project Name",
      "status": "Operational",
      "description": "What this project does...",
      "responsibilities": [
        "Built the backend using Node.js",
        "Deployed to AWS"
      ],
      "tags": ["Node.js", "AWS", "Docker"],
      "image": "images/project1.png"
    }
  ]
}
```

### Blogs (`content/blogs.json`)
```json
{
  "blogs": [
    {
      "id": 1,
      "title": "Your Blog Title",
      "slug": "your-blog-title",
      "category": "Tutorial",
      "excerpt": "A short preview of your blog...",
      "readTime": "5 min read",
      "status": "Published"
    }
  ]
}
```

### Experience (`content/experience.json`)
```json
{
  "experience": [
    {
      "id": 1,
      "title": "Your Job Title",
      "company": "Company Name",
      "startDate": "Jan 2023",
      "endDate": "Present",
      "responsibilities": [
        "What you did...",
        "Your achievements..."
      ]
    }
  ]
}
```

---

## 7. Admin Password

### Change the Password
1. Generate new SHA-256 hash:
```bash
echo -n 'your-new-password' | sha256sum | cut -d' ' -f1
```

2. Update `aman/index.html`:
```javascript
const correctHash = 'YOUR_NEW_HASH_HERE';
```

---

## 8. Fonts

Custom fonts are in `/fonts/` folder. To change:
1. Download new fonts from [Google Fonts](https://fonts.google.com/)
2. Update the font-family in CSS:
```css
body {
    font-family: 'Your Font Name', monospace;
}
```

---

## Tips

1. **Test locally** before pushing changes
2. **Backup files** before major edits
3. **Use Git branches** for experimental changes
4. **Validate JSON** using [jsonlint.com](https://jsonlint.com/)

---

**← Previous:** [Admin Panel Guide](ADMIN.md)
