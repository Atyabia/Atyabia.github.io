# 📸 IMAGE FOLDER STRUCTURE FOR GITHUB

## 📁 Complete Folder Organization

```
your-portfolio/
│
├── index.html
├── projects/
│   ├── heraqcles.html
│   ├── h2-mhytic.html
│   ├── bioreco2ver.html
│   └── ...
│
└── assets/
    └── images/
        ├── profile.jpg                          # Your profile photo (for hero section)
        │
        ├── publications/                        # Publication thumbnails/figures
        │   ├── paper1-thumbnail.jpg             # Journal Energy Storage paper
        │   ├── paper2-thumbnail.jpg             # Journal Power Sources paper
        │   ├── paper3-thumbnail.jpg             # Energy Conversion Management paper
        │   ├── paper4-thumbnail.jpg             # Energy journal paper
        │   └── paper5-thumbnail.jpg             # Fuel Cell Science paper
        │
        ├── book-chapters/                       # Book chapter covers/figures
        │   └── chapter1-thumbnail.jpg           # Your book chapter image
        │
        ├── conferences/                         # Conference presentation images
        │   ├── conference1-thumbnail.jpg        # First conference
        │   └── conference2-thumbnail.jpg        # Second conference
        │
        └── projects/                            # Project images/diagrams
            ├── heraqcles-thumbnail.jpg          # HERAQCLES project
            ├── h2-mhytic-thumbnail.jpg          # H2-MHYTIC project
            ├── bioreco2ver-thumbnail.jpg        # BioRECO2VER project
            ├── columbus-thumbnail.jpg           # COLUMBUS project
            ├── electrodialysis-thumbnail.jpg    # Electrodialysis project
            └── industrial-optimization-thumbnail.jpg  # Industrial project
```

---

## 🖼️ WHERE IMAGES ARE USED IN INDEX.HTML

### 1. Publications Section

Each publication has an image placeholder:

```html
<div class="image-placeholder">
    <img src="assets/images/publications/paper1-thumbnail.jpg" alt="Publication Figure">
</div>
```

**Image Paths in index.html:**
- `assets/images/publications/paper1-thumbnail.jpg`
- `assets/images/publications/paper2-thumbnail.jpg`
- `assets/images/publications/paper3-thumbnail.jpg`
- `assets/images/publications/paper4-thumbnail.jpg`
- `assets/images/publications/paper5-thumbnail.jpg`

### 2. Book Chapters Section

```html
<div class="image-placeholder">
    <img src="assets/images/book-chapters/chapter1-thumbnail.jpg" alt="Book Chapter">
</div>
```

**Image Path:**
- `assets/images/book-chapters/chapter1-thumbnail.jpg`

### 3. Conference Presentations Section

```html
<div class="image-placeholder">
    <img src="assets/images/conferences/conference1-thumbnail.jpg" alt="Conference">
</div>
```

**Image Paths:**
- `assets/images/conferences/conference1-thumbnail.jpg`
- `assets/images/conferences/conference2-thumbnail.jpg`

### 4. Projects Section

```html
<div class="image-placeholder">
    <img src="assets/images/projects/heraqcles-thumbnail.jpg" alt="HERAQCLES">
</div>
```

**Image Paths:**
- `assets/images/projects/heraqcles-thumbnail.jpg`
- `assets/images/projects/h2-mhytic-thumbnail.jpg`
- `assets/images/projects/bioreco2ver-thumbnail.jpg`
- `assets/images/projects/columbus-thumbnail.jpg`
- `assets/images/projects/electrodialysis-thumbnail.jpg`
- `assets/images/projects/industrial-optimization-thumbnail.jpg`

---

## 📋 HOW THE IMAGE SYSTEM WORKS

### Smart Fallback System

The HTML includes an **automatic fallback** system. If an image doesn't exist:
- The broken image is hidden
- A placeholder icon appears instead
- The page still looks professional

```html
<img src="assets/images/publications/paper1-thumbnail.jpg" 
     onerror="this.style.display='none'; this.nextElementSibling.style.display='block';">
<div style="display: none;">
    <i class="fas fa-image"></i>
    <p>Graphical Abstract / Figure</p>
</div>
```

**This means:**
✅ You don't need to add all images immediately
✅ The site works perfectly without images
✅ You can add images one by one over time
✅ No broken image icons will appear

---

## 🎨 RECOMMENDED IMAGE SPECIFICATIONS

### Publications, Book Chapters, Conferences:
- **Format:** JPG or PNG
- **Size:** 800 x 600 pixels (4:3 ratio) or 1200 x 675 pixels (16:9 ratio)
- **File Size:** Under 500 KB (optimize for web)
- **Content:** 
  - Graphical abstracts from papers
  - Key figures from publications
  - Conference presentation slides
  - Book chapter covers

### Projects:
- **Format:** JPG or PNG
- **Size:** 800 x 600 pixels or 1200 x 675 pixels
- **File Size:** Under 500 KB
- **Content:**
  - Project diagrams
  - Simulation results
  - System schematics
  - Team photos
  - Lab equipment

### Profile Photo:
- **Format:** JPG or PNG
- **Size:** 400 x 400 pixels (square)
- **File Size:** Under 200 KB
- **Content:** Professional headshot

---

## 📤 HOW TO UPLOAD IMAGES TO GITHUB

### Method 1: GitHub Web Interface (Easy)

1. Go to your repository on GitHub
2. Navigate to `assets/images/publications/`
3. Click "Add file" → "Upload files"
4. Drag your images
5. Commit changes

### Method 2: Git Command Line

```bash
# Navigate to your repository
cd your-portfolio

# Create directories
mkdir -p assets/images/publications
mkdir -p assets/images/book-chapters
mkdir -p assets/images/conferences
mkdir -p assets/images/projects

# Copy your images to the folders
cp ~/Downloads/paper1.jpg assets/images/publications/paper1-thumbnail.jpg
cp ~/Downloads/paper2.jpg assets/images/publications/paper2-thumbnail.jpg

# Add and commit
git add assets/images/
git commit -m "Add publication images"
git push
```

---

## 🔧 ADDING IMAGES STEP BY STEP

### Step 1: Prepare Your Images

1. **Find** graphical abstracts from your papers (usually in the PDF)
2. **Export** to JPG format
3. **Resize** to recommended dimensions (800x600 or 1200x675)
4. **Optimize** file size (use tools like TinyJPG.com)
5. **Rename** according to the naming scheme:
   - `paper1-thumbnail.jpg`
   - `paper2-thumbnail.jpg`
   - etc.

### Step 2: Create Folder Structure Locally

```bash
your-portfolio/
└── assets/
    └── images/
        ├── publications/
        ├── book-chapters/
        ├── conferences/
        └── projects/
```

### Step 3: Add Images

- Place images in their respective folders
- Use the exact filenames from the HTML

### Step 4: Upload to GitHub

- Upload the entire `assets/` folder
- GitHub will preserve the folder structure
- Images will automatically display on your site

---

## 🎯 QUICK START (Minimum Required)

### You don't need all images immediately!

**Start with these essentials:**

1. **Profile photo** (if you want to replace the icon)
   - `assets/images/profile.jpg`

2. **Top 2-3 publication figures**
   - `assets/images/publications/paper1-thumbnail.jpg`
   - `assets/images/publications/paper2-thumbnail.jpg`

3. **Main project image**
   - `assets/images/projects/heraqcles-thumbnail.jpg`

**Everything else can be added later!** The site works perfectly with placeholder icons.

---

## 💡 PRO TIPS

### Where to Find Good Images:

1. **Publications:**
   - Graphical abstracts from journal articles
   - Key figures showing results
   - Methodology diagrams
   - Extract from PDF using screenshot or image export

2. **Projects:**
   - Official project logos
   - Screenshots from simulations
   - COMSOL/ANSYS visualization results
   - System diagrams

3. **Conferences:**
   - Title slide from presentation
   - Key results slide
   - Conference poster (reduced size)

### Image Optimization Tools:

- **TinyJPG** - https://tinyjpg.com (compress images)
- **Squoosh** - https://squoosh.app (Google's image optimizer)
- **ImageOptim** - Free desktop app (Mac)
- **GIMP/Photoshop** - Resize and edit images

### Batch Renaming:

If you have many images to rename:

**Mac/Linux:**
```bash
# Rename multiple files at once
mv image1.jpg paper1-thumbnail.jpg
mv image2.jpg paper2-thumbnail.jpg
```

**Windows PowerShell:**
```powershell
Rename-Item image1.jpg paper1-thumbnail.jpg
Rename-Item image2.jpg paper2-thumbnail.jpg
```

---

## ✅ CHECKLIST

Before uploading:

- [ ] Images are in JPG or PNG format
- [ ] Images are optimized (under 500 KB each)
- [ ] Images are named correctly (e.g., `paper1-thumbnail.jpg`)
- [ ] Folder structure matches: `assets/images/[category]/filename.jpg`
- [ ] Images are placed in correct folders
- [ ] Tested locally (if possible)

After uploading:

- [ ] Visit your GitHub Pages site
- [ ] Check if images load
- [ ] Verify no broken image icons
- [ ] Test on mobile device
- [ ] Check loading speed

---

## 🚫 COMMON MISTAKES TO AVOID

❌ **Wrong folder path:**
```
images/publications/paper1.jpg  ← Missing "assets/"
```

✅ **Correct:**
```
assets/images/publications/paper1-thumbnail.jpg
```

❌ **Wrong filename:**
```
paper-1-thumb.jpg  ← Doesn't match HTML
```

✅ **Correct:**
```
paper1-thumbnail.jpg
```

❌ **Case sensitivity:**
```
Paper1-Thumbnail.JPG  ← Wrong case
```

✅ **Correct:**
```
paper1-thumbnail.jpg  ← All lowercase
```

❌ **Spaces in filename:**
```
paper 1 thumbnail.jpg  ← Has spaces
```

✅ **Correct:**
```
paper1-thumbnail.jpg  ← Use hyphens
```

---

## 📝 EXAMPLE: Adding Your First Image

Let's add an image for your first publication:

1. **Find the image:**
   - Open your paper PDF
   - Find the graphical abstract or a key figure
   - Take a screenshot or export the image

2. **Prepare the image:**
   - Save as JPG
   - Resize to 800 x 600 pixels
   - Rename to `paper1-thumbnail.jpg`

3. **Upload to GitHub:**
   - Go to your repository
   - Navigate to `assets/images/publications/`
   - Click "Upload files"
   - Drag `paper1-thumbnail.jpg`
   - Commit: "Add first publication image"

4. **Check your site:**
   - Wait 1-2 minutes
   - Refresh your GitHub Pages site
   - The image should now appear!

---

## 🎉 YOU'RE READY!

Remember:
- ✅ Images are optional - the site works without them
- ✅ Add images gradually over time
- ✅ Use the smart fallback system
- ✅ Follow the folder structure
- ✅ Optimize images for web

**Your portfolio will look professional with or without images!**

---

*Last Updated: November 2024*
