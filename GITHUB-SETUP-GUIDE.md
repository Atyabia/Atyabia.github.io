# GitHub Portfolio Website Setup Guide

## 📁 Recommended Folder Structure

```
your-portfolio/
├── index.html                          # Main homepage (rename index_improved.html)
├── README.md                           # Repository description
├── projects/
│   ├── alkaline-electrolyzer.html     # Project detail page
│   ├── pem-fuel-cell.html             # Another project (you can create more)
│   └── cfd-optimization.html          # Another project
├── assets/
│   ├── css/
│   │   └── style.css                  # Optional: Extract CSS to separate file
│   ├── images/
│   │   ├── profile.jpg                # Your profile photo
│   │   ├── projects/
│   │   │   ├── project1-hero.jpg
│   │   │   └── project1-results.png
│   │   └── publications/
│   │       └── paper-figures/
│   └── files/
│       ├── cv.pdf                     # Your CV/Resume
│       └── publications/
│           └── paper-pdfs/
└── .gitignore                         # Git ignore file
```

## 🚀 Step-by-Step GitHub Setup

### Step 1: Create Repository

1. Go to GitHub.com and sign in
2. Click the "+" icon → "New repository"
3. Repository name: `your-username.github.io` (for personal site) or `portfolio`
4. Description: "Professional Portfolio - Mechanical Engineering Researcher"
5. Make it Public
6. Check "Add a README file"
7. Click "Create repository"

### Step 2: Organize Your Files Locally

```bash
# Create the folder structure
mkdir your-portfolio
cd your-portfolio
mkdir projects assets
mkdir assets/css assets/images assets/files
mkdir assets/images/projects assets/images/publications
```

### Step 3: Rename and Place Files

1. **Rename** `index_improved.html` → `index.html`
2. **Move** `project-alkaline-electrolyzer.html` → `projects/alkaline-electrolyzer.html`
3. Place any images in `assets/images/`
4. Place your CV in `assets/files/cv.pdf`

### Step 4: Update File Links

In your `index.html`, update project links to:

```html
<!-- In the Projects Section -->
<a href="projects/alkaline-electrolyzer.html" class="btn btn-primary">
    <i class="fas fa-info-circle"></i> View Details
</a>
```

In your project files (`projects/alkaline-electrolyzer.html`), update the back link:

```html
<!-- In navigation -->
<a href="../index.html">
    <i class="fas fa-arrow-left"></i> Back to Portfolio
</a>

<!-- Update all links to index.html -->
<a href="../index.html">Home</a>
<a href="../index.html#projects">Projects</a>
```

### Step 5: Upload to GitHub

**Option A: Using GitHub Web Interface (Easiest)**

1. Go to your repository on GitHub
2. Click "uploading an existing file" or "Add file" → "Upload files"
3. Drag and drop all your files maintaining folder structure
4. Write a commit message: "Initial portfolio upload"
5. Click "Commit changes"

**Option B: Using Git Command Line**

```bash
# Navigate to your portfolio folder
cd your-portfolio

# Initialize git
git init

# Add remote repository
git remote add origin https://github.com/your-username/your-repo-name.git

# Add all files
git add .

# Commit
git commit -m "Initial portfolio upload"

# Push to GitHub
git branch -M main
git push -u origin main
```

**Option C: Using GitHub Desktop (User-Friendly)**

1. Download GitHub Desktop
2. File → Add Local Repository → Choose your portfolio folder
3. Publish repository to GitHub
4. Make changes and commit whenever you update

### Step 6: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings"
3. Scroll to "Pages" in left sidebar
4. Under "Source", select "main" branch
5. Choose "/ (root)" folder
6. Click "Save"
7. Wait 1-2 minutes for deployment
8. Your site will be live at: `https://your-username.github.io/repo-name/`

## 🔗 Linking Project Pages in index.html

Add this code to each project card in your Projects section:

```html
<div class="project-card">
    <h3><i class="fas fa-flask"></i> Alkaline Electrolyzer Optimization</h3>
    <p><strong>Duration:</strong> 2022 – Present</p>
    <p><strong>Institution:</strong> KU Leuven, Belgium</p>
    <p style="margin: 1rem 0;">
        Advanced 3D multiphysics modeling of alkaline water electrolysis systems...
    </p>
    <p><strong><i class="fas fa-tools"></i> Tools:</strong> COMSOL Multiphysics, MATLAB</p>
    <p><strong><i class="fas fa-chart-line"></i> Impact:</strong> 2 Q1 publications</p>
    
    <!-- ADD THIS BUTTON -->
    <div class="btn-group" style="margin-top: 1rem;">
        <a href="projects/alkaline-electrolyzer.html" class="btn btn-primary">
            <i class="fas fa-info-circle"></i> View Details
        </a>
        <a href="https://doi.org/10.1016/j.est.2023.109838" target="_blank" class="btn btn-success">
            <i class="fas fa-file-alt"></i> Read Paper
        </a>
    </div>
</div>
```

## 📝 Creating .gitignore File

Create a file named `.gitignore` in your root folder:

```
# macOS
.DS_Store

# Windows
Thumbs.db

# Editor files
.vscode/
.idea/
*.swp
*.swo

# Backup files
*~
*.backup

# Large files (if any)
*.psd
*.ai
```

## 📄 Creating README.md

Create a file named `README.md`:

```markdown
# Ali Atyabi - Professional Portfolio

Personal portfolio website showcasing my research in computational fluid dynamics, 
electrochemical systems, and sustainable energy technologies.

## 🌐 Live Website
Visit: [https://your-username.github.io/portfolio](https://your-username.github.io/portfolio)

## 🔬 Research Focus
- CFD Modeling
- PEM Fuel Cells
- Alkaline Electrolyzers
- Green Hydrogen Production

## 📚 Publications
594+ citations | h-index: 11 | 17+ peer-reviewed papers

## 🛠️ Built With
- HTML5
- CSS3
- JavaScript
- Font Awesome Icons

## 📫 Contact
- Email: atyabi902@gmail.com
- LinkedIn: [s-ali-atyabi](https://linkedin.com/in/s-ali-atyabi)
- Google Scholar: [Profile](https://scholar.google.com/citations?user=MytiTgsAAAAJ)

---
© 2024 Ali Atyabi. All rights reserved.
```

## 🎨 Optional: Extract CSS to Separate File

For better organization, you can move CSS from HTML to `assets/css/style.css`:

1. Copy all content from `<style>` tags
2. Create `assets/css/style.css`
3. Paste CSS content there
4. In your HTML files, replace the `<style>` section with:

```html
<link rel="stylesheet" href="assets/css/style.css">
<!-- For project pages: -->
<link rel="stylesheet" href="../assets/css/style.css">
```

## 🖼️ Adding Images

To add images to your pages:

1. Place images in `assets/images/`
2. In HTML, reference them:

```html
<!-- In index.html -->
<img src="assets/images/profile.jpg" alt="Ali Atyabi">

<!-- In project pages -->
<img src="../assets/images/projects/electrolyzer-model.png" alt="3D Model">
```

## 🔄 Updating Your Website

After making changes:

**Using Git Command Line:**
```bash
git add .
git commit -m "Description of changes"
git push
```

**Using GitHub Web:**
1. Navigate to the file
2. Click the pencil icon to edit
3. Make changes
4. Commit directly to main branch

**Using GitHub Desktop:**
1. Review changes
2. Write commit message
3. Click "Commit to main"
4. Click "Push origin"

## ✅ Testing Before Upload

1. Open `index.html` in your browser
2. Click all navigation links
3. Test project detail page links
4. Check all external links (LinkedIn, Google Scholar, etc.)
5. Test on mobile by resizing browser window
6. Check that all buttons and hover effects work

## 🌍 Custom Domain (Optional)

If you want to use your own domain (e.g., ali-atyabi.com):

1. Buy domain from registrar (Namecheap, GoDaddy, etc.)
2. In your repository, create file: `CNAME`
3. Add your domain: `www.ali-atyabi.com`
4. Configure DNS settings in your domain registrar
5. Wait for DNS propagation (24-48 hours)

## 🚨 Common Issues

**Issue:** Links don't work after upload
**Solution:** Make sure you're using relative paths (`projects/page.html` not `/projects/page.html`)

**Issue:** CSS not loading
**Solution:** Check that Font Awesome CDN link is present in `<head>`

**Issue:** Images not showing
**Solution:** Verify image paths are correct and files are uploaded

**Issue:** Page not updating on GitHub Pages
**Solution:** Wait a few minutes, clear browser cache, or do a hard refresh (Ctrl+F5)

## 📱 Mobile Optimization

Your website is already mobile-responsive! Test on:
- Phone (portrait & landscape)
- Tablet
- Desktop

## 🔍 SEO Optimization

Already included in your HTML:
- Meta descriptions
- Keywords
- Proper heading hierarchy
- Semantic HTML

To improve further, add to `index.html`:
```html
<meta property="og:title" content="Ali Atyabi - Mechanical Engineer">
<meta property="og:description" content="CFD Expert | Electrochemical Systems">
<meta property="og:image" content="assets/images/profile.jpg">
<meta property="og:url" content="https://your-username.github.io">
```

## 🎯 Final Checklist

- [ ] Files organized in folders
- [ ] index.html renamed from index_improved.html
- [ ] All links updated to reflect folder structure
- [ ] Images added to assets/images/
- [ ] README.md created
- [ ] .gitignore created
- [ ] Tested locally in browser
- [ ] Uploaded to GitHub
- [ ] GitHub Pages enabled
- [ ] Website is live and working

## 📞 Need Help?

If you encounter issues:
1. Check GitHub Pages documentation
2. Review the repository settings
3. Test links in local browser first
4. Verify file paths are correct

---

Good luck with your portfolio! 🚀
```
