# BRAINAI@UTA Website

This repository contains the website for the Brain and Artificial Intelligence Research Laboratory at the University of Texas at Arlington (BRAINAI@UTA), led by Dr. Xi Zhu.

## Overview

The BRAINAI@UTA website is a clean, modern, and responsive static website built with HTML, CSS, and minimal JavaScript. It is designed to be easily deployable on GitHub Pages and maintainable by lab members with minimal technical expertise.

## Site Structure

The website consists of the following pages:

- **Home** (`index.html`): Landing page with lab overview and latest news
- **About** (`about.html`): Detailed information about the lab's mission and research focus
- **Team** (`team.html`): Profiles of lab members including faculty, postdocs, and students
- **Publications** (`publications.html`): List of research papers organized by year and topic
- **Projects** (`projects.html`): Ongoing research projects and tools developed by the lab
- **Contact** (`contact.html`): Contact information, form, and opportunities to join the lab

## Getting Started

### Prerequisites

The website doesn't require any build tools or special software to run. You'll only need:

- A text editor (VS Code, Sublime, etc.)
- A modern web browser
- Git (for version control and deployment)

### Local Development

To work on the website locally:

1. Clone this repository to your local machine:
   ```
   git clone https://github.com/yourusername/brainai-website.git
   cd brainai-website
   ```

2. Open `index.html` in your web browser to view the site.

3. Make changes to the HTML, CSS, or JavaScript files as needed.

4. Refresh your browser to see the changes.

## Deployment to GitHub Pages

### Initial Setup

1. Create a GitHub repository for the website (e.g., `brainai-website`).

2. Push your local repository to GitHub:
   ```
   git remote add origin https://github.com/yourusername/brainai-website.git
   git branch -M main
   git push -u origin main
   ```

3. In your GitHub repository, go to "Settings" > "Pages".

4. Under "Source", select "main" branch and save.

5. Your site will be published at `https://yourusername.github.io/brainai-website/`.

### Using a Custom Domain (Optional)

If you have a custom domain for the lab (e.g., `brainai.uta.edu`):

1. Add a file named `CNAME` to the root of your repository with your domain name:
   ```
   brainai.uta.edu
   ```

2. Configure your DNS provider:
   - Add an `A` record pointing to GitHub Pages IP addresses:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - Alternatively, add a `CNAME` record from your subdomain (e.g., `www`) to `yourusername.github.io`.

3. In your GitHub repository settings, add your custom domain and enable HTTPS.

## Maintaining the Website

### Adding a New Team Member

1. Open `team.html` in your text editor.

2. Find the appropriate section (Faculty, Postdocs, Graduate Students, etc.).

3. Copy an existing team member card and update the information:
   ```html
   <div class="team-member">
       <div class="member-photo">
           <img src="images/new-member.jpg" alt="New Member Name">
       </div>
       <h3>New Member Name</h3>
       <p class="member-title">Position Title</p>
       <p class="member-bio">
           Brief bio and research interests.
       </p>
       <div class="member-links">
           <a href="mailto:email@example.com"><i class="fas fa-envelope"></i> Email</a>
       </div>
   </div>
   ```

4. Add the member's photo to the `images` folder.

### Adding a New Publication

1. Open `publications.html` in your text editor.

2. Find the appropriate year section or create a new one if needed.

3. Add a new publication item:
   ```html
   <div class="publication-item" data-year="2023" data-topic="topic1 topic2">
       <div class="publication-meta">
           <span class="publication-date">Month 2023</span>
           <span class="publication-journal">Journal Name</span>
       </div>
       <h3>Publication Title</h3>
       <p class="publication-authors">Author 1, Author 2, <strong>Zhu X</strong>, Author 3</p>
       <p class="publication-abstract">
           Publication abstract or summary.
       </p>
       <div class="publication-links">
           <a href="#" target="_blank" class="doi-link"><i class="fas fa-external-link-alt"></i> DOI: 10.xxxx/xxxxx</a>
           <a href="#" class="pdf-link"><i class="fas fa-file-pdf"></i> PDF</a>
       </div>
   </div>
   ```

### Adding a New Project

1. Open `projects.html` in your text editor.

2. In the `project-grid` section, add a new project card:
   ```html
   <div class="project-card">
       <div class="project-header">
           <div class="project-icon">
               <i class="fas fa-icon-name"></i>
           </div>
           <h3>Project Title</h3>
       </div>
       <div class="project-content">
           <p>
               Project description.
           </p>
           <h4>Key Research Questions:</h4>
           <ul>
               <li>Research question 1</li>
               <li>Research question 2</li>
           </ul>
           <div class="project-links">
               <a href="#" class="btn secondary-btn">Learn More</a>
               <a href="project-materials/document.pdf" class="pdf-link"><i class="fas fa-file-pdf"></i> Project Brief</a>
           </div>
       </div>
   </div>
   ```

### Updating Contact Information

1. Open `contact.html` in your text editor.

2. Update the relevant information in the contact details section.

3. If using the contact form with Formspree, replace `yourformid` in the form action with your actual Formspree form ID:
   ```html
   <form id="contact-form" class="contact-form" action="https://formspree.io/f/yourformid" method="POST">
   ```

## Customization

### Colors and Styling

The website uses CSS variables for consistent styling. To change the color scheme:

1. Open `css/styles.css`.

2. Modify the variables in the `:root` selector:
   ```css
   :root {
       --primary-color: #0064b1; /* UTA blue */
       --secondary-color: #ff5a00; /* UTA orange */
       --accent-color: #5c068c; /* Purple accent */
       /* Other variables */
   }
   ```

### Adding Google Analytics

To add Google Analytics tracking:

1. Get your Google Analytics tracking ID.

2. Add the Google Analytics tracking code to the `<head>` section of each HTML file:
   ```html
   <!-- Google Analytics -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXXX-X"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'UA-XXXXXXXX-X');
   </script>
   ```

## Troubleshooting

- **Images not displaying**: Ensure image paths are correct and the files exist in the specified folders.
- **Styling issues**: Check browser developer tools for CSS errors.
- **Form submission errors**: Verify your Formspree setup is correct and you're using a valid form ID.

## License

This website template is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Font Awesome for icons
- Google Fonts for typography
- Formspree for contact form processing 