# Huangshu Xu's Homepage

Academic personal website for Huangshu Xu, LMSW, Ph.D. Candidate in Social Work at Fordham University.

Live site: https://www.huangshuxu.com/

## About

This is a Jekyll-based academic homepage built with Bootstrap 5, featuring a clean and professional design optimized for showcasing academic work, research, and professional experience.

## Features

- **Responsive Design**: Mobile-friendly layout using Bootstrap 5
- **Publications Section**: Organized by publication status (Published, Under Review) with automatic author name highlighting
- **Research Projects**: Display ongoing and completed research with abstracts and PDFs
- **Teaching Experience**: Showcase current and past teaching roles
- **News Section**: Highlight recent presentations, publications, and achievements
- **Professional Affiliations**: Display memberships and work history
- **Contact Information**: Integrated contact details with social media links
- **Visitor Map**: MapMyVisitors widget to track site visitors geographically
- **Google Scholar Integration**: Direct link to Google Scholar profile with icon
- **CV/Resume Download**: Easy access to downloadable CV

## Technology Stack

- **Jekyll**: Static site generator
- **Bootstrap 5**: CSS framework for responsive design
- **GitHub Pages**: Hosting platform
- **Liquid**: Template engine for dynamic content
- **YAML**: Data files for easy content management

## Setup and Installation

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler
- Git

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/ccj5351/xhsHomePage.git
cd xhsHomePage
```

2. Install dependencies:
```bash
bundle install
```

3. Run the local development server:
```bash
bundle exec jekyll serve --baseurl ''
```

4. Open your browser and navigate to `http://127.0.0.1:4000/`

### Deployment to GitHub Pages

The site is configured to deploy automatically to GitHub Pages when changes are pushed to the main branch.

### Custom Domain Setup

To use a custom domain (e.g., `www.huangshuxu.com`) with your GitHub Pages site:

1. **Add CNAME file to repository**:
   - Create a file named `CNAME` in the root directory
   - Add your custom domain (e.g., `www.huangshuxu.com`) as the only content
   - See our example in this repository: [CNAME](./CNAME)


2. **Configure DNS records** with your domain provider:
   - Add a CNAME record:
     - **Name/Host**: `www`
     - **Value/Points to**: `ccj5351.github.io` (your GitHub Pages domain)
     - **TTL**: Automatic or 3600

   Example DNS configuration (GoDaddy):

   ![GoDaddy DNS Setup Example](./assets/images/godaddy-dsn-domain-setup-for-github-page-repo.png)

   - For apex domain (e.g., `huangshuxu.com`), add A records pointing to GitHub's IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`

3. **Enable HTTPS** in GitHub repository settings:
   - Go to Settings → Pages
   - Check "Enforce HTTPS" after DNS propagates (may take 24-48 hours)

4. **Update `_config.yml`** (optional - GitHub Pages handles this automatically):

   Your current configuration works with the custom domain:
   ```yaml
   baseurl: "/xhsHomePage"  # Keep as-is, GitHub Pages will handle it
   url: "https://ccj5351.github.io"  # Your GitHub Pages domain
   ```

   Note: When using a custom domain with GitHub Pages, you typically don't need to change these settings. GitHub automatically serves your site from the custom domain specified in the CNAME file while maintaining compatibility with the original GitHub Pages URL.

## Customization

### Updating Content

All content is managed through YAML data files for easy updates without touching HTML:

**Main Content** (`_data/hometext.yml`):
- Header information (name, title, bio, profile image)
- Publications (organized by category)
- Research projects
- Teaching experience
- News items
- Professional affiliations
- Contact information

**Navigation** (`_data/navigation.yml`):
- Site navigation menu items

### Adding Publications

Edit `_data/hometext.yml` under the `publications` section:

```yaml
publications:
  categories:
    - name: "Published"
      papers:
        - authors: "Author Names Here"
          year: "2025"
          title: "Paper Title"
          journal: "Journal Name"
          url: "https://link-to-paper"
          status: ""
```

The author name "Huangshu Xu" will be automatically bolded in the output.

### Adding Research Projects

Edit `_data/hometext.yml` under the `projects` section:

```yaml
projects:
  list:
    - title: "Project Title"
      contributors: "Contributor Names"
      abstract_text: "Project description and presentation details"
      pdf: "/assets/pdf/file.pdf"
      status: "ongoing" # or "completed"
```

### Updating Profile Image

1. Add your image to `/assets/images/`
2. Update the path in `_data/hometext.yml`:

```yaml
header:
  image: "/assets/images/your-image.jpg"
```

### Customizing Colors and Styles

- Bootstrap theme: Edit `_sass/_bootstrap.scss`
- Custom styles: Add to `/assets/css/main.scss`

## File Structure

```
xhsHomePage/
├── _data/
│   ├── hometext.yml          # Main content data
│   └── navigation.yml         # Navigation menu
├── _includes/
│   ├── hero.html              # Header/profile section
│   ├── publications.html      # Publications section
│   ├── projects.html          # Research projects section
│   ├── teaching.html          # Teaching section
│   ├── news.html              # News section
│   ├── affiliations.html      # Professional affiliations
│   ├── contact.html           # Contact section with visitor map
│   └── footer.html            # Footer
├── _layouts/
│   ├── default.html           # Base layout
│   └── home.html              # Homepage layout
├── assets/
│   ├── images/                # Images and icons
│   ├── pdf/                   # PDF files (CV, papers)
│   ├── css/                   # Stylesheets
│   └── js/                    # JavaScript files
├── _config.yml                # Jekyll configuration
├── Gemfile                    # Ruby dependencies
└── index.md                   # Homepage entry point
```

## Configuration

Key settings in `_config.yml`:

- `title`: Site title
- `description`: Site description for SEO
- `baseurl`: Subpath of your site (e.g., `/xhsHomePage`)
- `url`: Full URL of your site

## Features in Detail

### Contact Information Under Profile

Email, phone, and address are displayed under the profile image with custom icons and flexible sizing to accommodate different image dimensions.

### Visitor Map

The site includes a MapMyVisitors widget in the Contact section to track visitor locations. Update the widget code in `_includes/contact.html` with your own tracking ID.

### Spam-Resistant Email

Email addresses are displayed as images or obfuscated text to prevent spam harvesting while remaining visible to visitors.

## Credits

- Based on the [Jekyll Academic Template](https://avic.devpractical.com/personal-academic-website/)
- Hosted on [GitHub Pages](https://github.com/ccj5351/xhsHomePage)
- Built with [Bootstrap 5](https://getbootstrap.com/)
- Icons from [Icons8](https://icons8.com/)

## License

This project is open source and available for academic use.

## Contact

For questions or suggestions about this website template, please visit the repository: https://github.com/ccj5351/xhsHomePage
