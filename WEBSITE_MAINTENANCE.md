# BRAIN Lab Website Maintenance Guide

This guide provides step-by-step instructions for updating and maintaining the BRAIN Lab @ UTA website.

## 🌐 Website Overview

The BRAIN Lab website is a **static website** built with HTML, CSS, and minimal JavaScript. It's hosted on **GitHub Pages**, which means:
- No login credentials are required for the website itself
- Updates are made by editing files and pushing to GitHub
- Changes deploy automatically when pushed to the main branch

## 📁 Website Structure

```
Website/
├── index.html              # Home page
├── about.html              # About page
├── team.html               # Team overview page
├── publications.html       # Publications page
├── projects.html           # Projects overview page
├── grants.html             # Grants page
├── contact.html            # Contact page
├── lab_manual.html         # Lab manual page
├── _config.yml             # Site configuration
├── css/
│   └── styles.css          # Website styling
├── images/                 # Site images (banner, logos, etc.)
├── team members/           # Team member photos and docs
├── team_members/           # Individual team member HTML pages
├── projects/               # Individual project pages
├── publications/           # Publication documents
└── lab grants/             # Grant documents
```

## 👥 Adding/Updating Team Members

### Step 1: Add Team Member Photo
1. Save the photo in the `team members/` folder
2. Use a clear, professional headshot
3. Recommended format: JPG or PNG
4. Recommended size: 200x200 pixels or larger (square ratio preferred)

### Step 2: Update Main Team Page
1. Open `team.html` in a text editor
2. Find the `<div class="team-grid">` section
3. Add a new team member block following this template:

```html
<div class="team-member">
    <div class="member-photo">
        <img src="team members/[PHOTO_FILENAME]" alt="[MEMBER_NAME]">
    </div>
    <div class="member-info">
        <h3>[MEMBER_NAME], [DEGREE]</h3>
        <p class="member-title">[POSITION_TITLE]</p>
        <p class="member-bio">[SHORT_BIO_PARAGRAPH]</p>
        <div class="member-links">
            <a href="mailto:[EMAIL]"><i class="fas fa-envelope"></i> Email</a>
            <a href="team_members/[member_filename].html" class="read-more">
                <i class="fas fa-user"></i> Full Profile
            </a>
        </div>
    </div>
</div>
```

### Step 3: Create Individual Profile Page
1. Create a new HTML file in `team_members/` folder (e.g., `john_doe.html`)
2. Copy the structure from an existing profile (e.g., `fatima_rizwan.html`)
3. Update the following sections:
   - Page title in `<title>` tag
   - Member name, position, and email
   - Photo path (should be `../team members/[PHOTO_FILENAME]`)
   - Full biography in the `member-bio` section

### Step 4: Remove Team Members
1. Delete their photo from `team members/` folder
2. Remove their section from `team.html`
3. Delete their individual profile page from `team_members/` folder

## 📝 Updating Publications

1. Open `publications.html`
2. Add new publications to the list following the existing format
3. For publication documents, add PDFs to the `publications/` folder
4. Link to PDFs using: `href="publications/[FILENAME].pdf"`

## 🔬 Managing Projects

### Adding a New Project
1. Create a new HTML file in the `projects/` folder (e.g., `new-study.html`)
2. Copy the structure from an existing project page
3. Update the content with project details
4. Add the project to the main projects page (`projects.html`)

### Updating Project Information
1. Edit the corresponding HTML file in the `projects/` folder
2. Update project descriptions, timelines, or status

## 💰 Updating Grants Information

1. **Current Grants**: Edit `grants.html`
2. **Past Grants**: Edit `past_grants.html`
3. **Pending Grants**: Edit `pending_grants.html`
4. Add grant documents to the `lab grants/` folder

## 🛠️ Common Website Updates

### Changing Contact Information
1. Open `contact.html`
2. Update email addresses, phone numbers, or office locations
3. Also update footer information in each HTML file if needed

### Updating Navigation Menu
1. The navigation menu appears in every HTML file
2. To add a new page, add a menu item in each file's `<nav>` section:
```html
<li><a href="newpage.html">New Page</a></li>
```

### Changing Banner Image
1. Replace `images/banner.png` with your new image
2. Keep the same filename, or update all references in the HTML files

### Modifying Site-wide Settings
1. Edit `_config.yml` for:
   - Site title and description
   - Author information
   - Social media links

## 🚀 Publishing Changes

### Step 1: Test Locally (Recommended)
1. Open the HTML files in your web browser to preview changes
2. Check that all links work and images display correctly

### Step 2: Commit and Push to GitHub
1. Open Terminal/Command Prompt
2. Navigate to the website folder:
```bash
cd "/Users/zhulab/Desktop/Brain Lab/Website"
```

3. Add your changes:
```bash
git add .
```

4. Commit with a descriptive message:
```bash
git commit -m "Add new team member John Doe" 
```

5. Push to GitHub:
```bash
git push origin main
```

### Step 3: Verify Deployment
- Changes will automatically deploy to GitHub Pages within a few minutes
- Check the live website to confirm your updates appear correctly

## ⚠️ Important Notes

### File Naming Conventions
- Use lowercase letters and hyphens for file names (e.g., `john-doe.html`)
- No spaces in file names
- Keep file names descriptive but concise

### Image Guidelines
- Optimize images for web (keep file sizes under 1MB when possible)
- Use descriptive alt text for accessibility
- Maintain consistent photo styles for team members

### Backup Procedures
- The Git repository serves as your backup
- Keep local copies of important documents
- Test changes thoroughly before pushing to the live site

## 🆘 Troubleshooting

### Changes Not Appearing on Live Site
1. Check that you pushed changes to the `main` branch
2. Wait 5-10 minutes for GitHub Pages to rebuild
3. Clear your browser cache and refresh

### Broken Images
1. Check file paths are correct (case-sensitive)
2. Ensure images are in the correct folder
3. Verify image files aren't corrupted

### Layout Issues
1. Validate HTML syntax using online validators
2. Check CSS for syntax errors
3. Test on different browsers and devices

## 📞 Getting Help

For technical issues beyond this guide:
1. Contact the lab's designated web administrator
2. Check GitHub repository for existing issues
3. Consult GitHub Pages documentation for deployment issues

---

*Last updated: [Current Date]*
*Website: [Lab Website URL]*