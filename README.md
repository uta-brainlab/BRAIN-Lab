# BRAIN Lab @ UTA Website

This repository contains the source code for the website of the Biomedical Research in AI and Neuroimaging Laboratory at the University of Texas at Arlington (BRAIN Lab @ UTA), led by Dr. Xi Zhu.

## Overview

The BRAIN Lab @ UTA website is a clean, modern, and responsive static website built with HTML, CSS, and minimal JavaScript. It is designed to be easily deployable on GitHub Pages and maintainable by lab members.

## Features

- Clean and professional design
- Fully responsive layout
- Fast loading and minimal JavaScript
- Easy to maintain and update
- SEO-friendly structure
- Accessible design

## Directory Structure

```
brain-lab-website/
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── images/
├── team_members/
├── lab projects/
├── lab grants/
├── index.html
└── README.md
```

## Local Development

To work on the website locally:

1. Clone the repository:
```bash
git clone https://github.com/yourusername/brain-lab-website.git
cd brain-lab-website
```

2. Open the files in your preferred code editor.

3. Use a local server to preview changes (e.g., Live Server in VS Code).

## Deployment

### GitHub Pages

To deploy the website to GitHub Pages:

1. Create a GitHub repository for the website (e.g., `brain-lab-website`).

2. Push your code to GitHub:
```bash
git remote add origin https://github.com/yourusername/brain-lab-website.git
git branch -M main
git push -u origin main
```

3. Go to your repository settings on GitHub.

4. Under "GitHub Pages", select the main branch as the source.

5. Your site will be published at `https://yourusername.github.io/brain-lab-website/`.

### Custom Domain

If you have a custom domain for the lab (e.g., `brain.uta.edu`):

1. Add a CNAME file to the repository root.
2. Add your domain to the file:
```
brain.uta.edu
```

3. Update your domain's DNS settings according to GitHub Pages documentation.

## Contributing

Lab members can contribute to the website by:

1. Creating a fork of the repository
2. Making changes in a new branch
3. Submitting a pull request
4. Getting approval from the lab administrator

## License

Copyright (c) 2024 BRAIN Lab @ UTA (Biomedical Research in AI and Neuroimaging Laboratory at the University of Texas at Arlington)

All rights reserved. 