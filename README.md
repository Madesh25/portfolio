# 🚀 Madeshwaran's DevOps Portfolio

A modern, terminal-themed portfolio website built with pure HTML, CSS, and JavaScript. Features an admin panel for content management and is deployed on Cloudflare Pages.

![Portfolio Preview](images/og-image.png)

## 🌐 Live Demo

- **Website:** [https://madesh.online](https://madesh.online)
- **Admin Panel:** `/aman/` (password protected)

## ✨ Features

- 🎨 **Terminal-style Design** - Unique developer aesthetic with green terminal theme
- 📱 **Fully Responsive** - Works on all devices
- 🔐 **Password Protected Admin Panel** - Manage content securely
- 📝 **Dynamic Content** - Projects, Blogs, and Experience loaded from JSON
- 📧 **Working Contact Form** - Sends emails via Web3Forms
- 📄 **Resume Download** - PDF resume available for visitors
- ⚡ **Fast Loading** - Pure HTML/CSS/JS, no heavy frameworks

## 📁 Project Structure

```
clifolio-port/
├── index.html          # Home page
├── about.html          # About page with skills & resume
├── projects.html       # Projects showcase
├── blog.html           # Blog posts
├── experience.html     # Work experience timeline
├── contact.html        # Contact form (Web3Forms)
├── aman/               # Admin panel (password protected)
│   └── index.html
├── content/            # JSON data files
│   ├── projects.json
│   ├── blogs.json
│   └── experience.json
├── resume/             # Resume PDF folder
│   └── Madeshwaran_Resume.pdf
├── images/             # All images
├── fonts/              # Custom fonts
└── docs/               # Documentation
```

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure |
| CSS3 | Styling (custom terminal theme) |
| JavaScript | Interactivity & dynamic content |
| Web3Forms | Contact form email service |
| Cloudflare Pages | Free hosting |
| GitHub | Version control |

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/Madesh25/portfolio.git
cd portfolio
```

### 2. Run Locally
```bash
# Using Python (simplest)
python3 -m http.server 8080

# Then open http://localhost:8080 in your browser
```

### 3. Customize Content
Edit the JSON files in `/content/` folder:
- `projects.json` - Your projects
- `blogs.json` - Your blog posts
- `experience.json` - Your work experience

## 📖 Documentation

See the [docs/](docs/) folder for detailed guides:
- [Project Setup Guide](docs/SETUP.md)
- [Deployment Guide](docs/DEPLOYMENT.md)
- [Admin Panel Guide](docs/ADMIN.md)
- [Customization Guide](docs/CUSTOMIZATION.md)

## 🔐 Security Features

- ✅ Admin password is **SHA-256 hashed** (not stored in plaintext)
- ✅ Session-based authentication
- ✅ Spam protection on contact form

## 📬 Contact Form Setup

The contact form uses [Web3Forms](https://web3forms.com/) (free service):
1. Get an access key from web3forms.com
2. Replace `YOUR_ACCESS_KEY` in `contact.html`
3. Messages will be sent to your email!

## 📄 License

This project is open source. Feel free to use it as a template for your own portfolio!

## 👨‍💻 Author

**Madeshwaran M**
- Website: [madesh.online](https://madesh.online)
- LinkedIn: [Madeshwaran M](https://linkedin.com/in/madeshwaranm)
- GitHub: [@Madesh25](https://github.com/Madesh25)

---

Made with 💚 by Madeshwaran M
