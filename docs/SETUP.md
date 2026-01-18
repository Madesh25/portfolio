# 📋 Project Setup Guide

This guide explains how to set up and run this portfolio website locally.

## Prerequisites

Before you begin, make sure you have:
- A computer with Windows, Mac, or Linux
- A web browser (Chrome, Firefox, Edge, etc.)
- A text editor (VS Code recommended)
- Git installed ([Download Git](https://git-scm.com/))
- Python 3 installed (for local server)

## Step 1: Download the Project

### Option A: Clone from GitHub
```bash
git clone https://github.com/Madesh25/portfolio.git
cd portfolio
```

### Option B: Download ZIP
1. Go to the GitHub repository
2. Click the green "Code" button
3. Click "Download ZIP"
4. Extract the ZIP file

## Step 2: Understand the File Structure

```
portfolio/
├── index.html          # 🏠 Home page (entry point)
├── about.html          # 👤 About me page
├── projects.html       # 💼 Projects showcase
├── blog.html           # 📝 Blog posts
├── experience.html     # 📅 Work experience
├── contact.html        # 📧 Contact form
│
├── aman/               # 🔐 Admin panel
│   └── index.html      #    (password protected)
│
├── content/            # 📄 JSON data files
│   ├── projects.json   #    Project data
│   ├── blogs.json      #    Blog data
│   └── experience.json #    Experience data
│
├── resume/             # 📄 Resume PDF
├── images/             # 🖼️ All images
├── fonts/              # 🔤 Custom fonts
└── docs/               # 📖 Documentation
```

## Step 3: Run Locally

### Using Python (Recommended)
```bash
# Navigate to project folder
cd portfolio

# Start a local server
python3 -m http.server 8080
```

Then open your browser and go to: **http://localhost:8080**

### Using VS Code Live Server
1. Open the project in VS Code
2. Install "Live Server" extension
3. Right-click on `index.html`
4. Select "Open with Live Server"

## Step 4: Test the Website

1. **Home Page** - http://localhost:8080/
2. **About** - http://localhost:8080/about.html
3. **Projects** - http://localhost:8080/projects.html
4. **Admin Panel** - http://localhost:8080/aman/
   - Password: `madesh@aman2025`

## Common Issues

### "Port already in use"
```bash
# Kill the process using the port
pkill -f "python3 -m http.server"

# Try again
python3 -m http.server 8080
```

### "Page not found"
Make sure you're in the correct directory (the one with `index.html`)

### "Styles not loading"
Make sure all files are in the correct locations

---

**Next:** [Deployment Guide](DEPLOYMENT.md) →
