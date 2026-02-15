# Layer 8 Service Website

Professional IT support website for Layer 8 Service LLC - "Making Your Tech Work For You"

## 🚀 Quick Start - Hosting on GitHub Pages

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in (or create an account)
2. Click the **+** icon in the top right and select "New repository"
3. Name your repository: `layer8service` (or `yourusername.github.io` for a personal site)
4. Set it to **Public**
5. **Do NOT** check "Initialize with README"
6. Click **Create repository**

### Step 2: Upload Your Files

You have two options:

#### Option A: Upload via Web Interface (Easiest)
1. On your new repository page, click **uploading an existing file**
2. Drag and drop these files:
   - `index.html`
   - `layer8.png`
   - `layer8vert.png`
   - `README.md`
3. Scroll down and click **Commit changes**

#### Option B: Use Git (Recommended for future updates)
See the **Basic Git Workflow** section below

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top navigation)
3. Click **Pages** in the left sidebar
4. Under "Source":
   - Select **Deploy from a branch**
   - Choose **main** branch
   - Select **/ (root)** folder
5. Click **Save**
6. Wait 1-2 minutes for deployment

### Step 4: Access Your Site

Your website will be live at:
- `https://yourusername.github.io/layer8service/`
- Or `https://yourusername.github.io/` if you named the repo `yourusername.github.io`

---

## 🌐 Custom Domain Setup (layer8service.com)

### In GitHub:
1. Go to repository **Settings** → **Pages**
2. Under "Custom domain", enter: `layer8service.com`
3. Check **Enforce HTTPS** (wait a few minutes after DNS propagation)
4. Click **Save**

### In Your Domain Registrar:
Add these DNS records where you purchased your domain:

**A Records** (for apex domain):
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

**CNAME Record** (for www):
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

**Note:** DNS changes can take up to 48 hours to propagate, but usually happen within a few hours.

---

## 💻 Basic Git Workflow

### First Time Setup

1. **Install Git**
   - Windows: Download from [git-scm.com](https://git-scm.com)
   - Mac: `brew install git` or install Xcode Command Line Tools
   - Linux: `sudo apt-get install git` or `sudo yum install git`

2. **Configure Git** (first time only)
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "hello@layer8service.com"
   ```

3. **Navigate to your website folder**
   ```bash
   cd path/to/your/website/folder
   ```

4. **Initialize and push to GitHub**
   ```bash
   # Initialize Git repository
   git init
   
   # Add all files
   git add .
   
   # Create first commit
   git commit -m "Initial commit - Layer 8 Service website"
   
   # Add GitHub as remote (replace 'yourusername' with your GitHub username)
   git remote add origin https://github.com/yourusername/layer8service.git
   
   # Push to GitHub
   git branch -M main
   git push -u origin main
   ```

### Making Updates (After Initial Setup)

Every time you make changes to your website:

```bash
# 1. Check what files changed
git status

# 2. Add the changes
git add .
# Or add specific files: git add index.html

# 3. Commit with a descriptive message
git commit -m "Updated contact information"

# 4. Push to GitHub (and deploy)
git push
```

**Your changes will be live within 1-2 minutes!**

### Useful Git Commands

```bash
# See recent commits
git log --oneline

# Undo changes to a file (before committing)
git checkout -- filename.html

# Pull latest changes (if editing from multiple places)
git pull

# Create a new branch for experiments
git checkout -b new-feature

# Switch back to main branch
git checkout main
```

---

## 📁 File Structure

```
layer8service/
├── index.html          # Main website file
├── layer8.png          # Horizontal logo (for header)
├── layer8vert.png      # Vertical logo (for future use)
└── README.md           # This file
```

---

## 🎮 Future Enhancements

As mentioned, this site is ready to expand with:
- Hidden game sections (can create separate HTML pages)
- Additional service pages
- Blog or news section
- Client portal
- Photo gallery

To add new pages, simply create new `.html` files and link to them from `index.html`.

---

## 🛠️ Making Changes

### Updating Contact Info
Edit `index.html` and search for the contact section around line 640.

### Changing Colors
Colors are defined in CSS variables at the top of `index.html` (around line 14):
```css
:root {
    --primary: #2f4a7c;
    --primary-dark: #1d3461;
    --accent: #4a7ba7;
    /* etc... */
}
```

### Adding New Services
Find the services grid section (around line 580) and duplicate a service card, then modify the content.

---

## 📞 Support

For questions about the website or Git workflow:
- GitHub Docs: [docs.github.com](https://docs.github.com)
- Git Basics: [git-scm.com/book](https://git-scm.com/book/en/v2)

---

## 📄 License

© 2026 Layer 8 Service LLC. All rights reserved.

---

**Built with:** HTML5, CSS3, JavaScript  
**Hosted on:** GitHub Pages  
**Domain:** layer8service.com

