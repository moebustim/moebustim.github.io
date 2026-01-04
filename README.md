# Jekyll Academic Website Template

A clean Jekyll template for academics and researchers. Features structured templates for CV, publications, and talks.

## Quick Start

### Prerequisites

- Ruby (2.7+)
- Bundler gem
- Git

### Installation

1. Fork or clone this repository
2. Navigate to the project directory
3. Update the relevant files with your personal information (see below)
4. Install dependencies:

   ```bash
   bundle install
   ```

5. Start the development server:

   ```bash
   bundle exec jekyll serve
   ```

6. Visit `http://localhost:4000/` to see your site

## Configuration

### Site Settings (_config.yml)

Update the main configuration file with your information:

```yaml
# Site settings
title: "Your Name"
description: >
  Your professional description here.
baseurl: "" # Leave empty for root domain, or add subpath like "/repo-name"
url: "https://yourusername.github.io" # the base hostname & protocol for your site

# Social media usernames (without @ symbol)
github_username: "your-github-username"
orcid_id: "0000-0000-0000-0000"
linkedin_username: "your-linkedin-username"
email_user: "youremailusername"
email_domain: "example.com"

# Credit :) 
credit-title: "Paul Gondolf"
credit-url: "https://paul-the-wizord.github.io"
```

Of course you should also update the cv.md, index.md, projects.md and talks.md with your own information.

### Additional Customizations

Don't forget to personalize these visual elements:

- **Profile Image**: Replace the default profile image in `/assets/images/profile.png` with your own professional photo
- **Favicon**: Create and add a favicon (the small icon in browser tabs) - you can use your initials, a professional headshot, or a symbol related to your field. Place favicon files in `/assets/images/` and add the appropriate `<link>` tags to your layout's `<head>` section

In the robots.txt you should change the link to the Sitemap and also set your privacy settings.

```txt
User-agent: *
Allow: /

Sitemap: https://yourusername.github.io/sitemap.xml
```

## Page Templates & Usage

### CV Page (cv.md)

The CV template supports structured data for education, employment, and teaching experience:

```yaml
---
layout: cv
title: "Curriculum Vitae"
permalink: /cv/
last_updated: "January 2026"
description: "Brief description of your background"

education:
  - date: "2025"
    degree: "PhD in Your Field"
    institution: "University Name"
    institution_url: "https://university.edu/"
    location: "City, Country"
    details:
      - label: "Graduation"
        text: "Month Year"
      - label: "Dissertation"
        text: "Your dissertation title"
        url: "https://link-to-dissertation.com"
      - label: "Research Focus"
        text: "Your research area"
      - label: "Extracurricular"
        text: "List of programs, workshops, seminars (collapsible)"
      - label: "Curriculum"
        text: "List of relevant courses and their topics (collapsible)"

employment:
  - date: "present"
    title: "Job Title"
    institution: "Institution Name"
    institution_url: "https://institution.edu/"
    location: "City, Country"
    details:
      - label: "Period"
        text: "MM.YYYY - present"
      - label: "Funding"
        text: "Grant information (optional)"

teaching:
  - "Course Title 1 (Years, Institution)"
  - "Course Title 2 (Years, Institution)"
---
```

### Projects Page (projects.md)

The projects template displays code projects and research papers in a combined layout:

```yaml
---
layout: projects
title: "Projects"
permalink: /projects/
last_updated: "January 2026"
description: "A selection of public coding projects and research publications"

numerical_simulations:
  - url: "https://github.com/yourusername/project1"
    preview_title: "Project Title"
    preview_image: "/assets/images/project-preview.png"
  - url: "https://zenodo.org/records/12345"
    preview_title: "Another Project"
    preview_image: "/assets/images/project2-preview.png"

papers:
  - title: "Your Paper Title"
    paper_type: published  # or 'preprint'
    journal: "Journal Name"  # for published papers
    status: "Submitted to Journal"  # for preprints
    year: 2025
    authors:
      - name: "Coauthor Name"
      - name: "Your Name"
        highlight: true  # Highlights your name in bold
    abstract: "Your paper abstract here..."
    links:
      - text: "arXiv:2512.04066"
        url: "https://arxiv.org/abs/2512.04066"
      - text: "PDF"
        url: "https://arxiv.org/pdf/2512.04066"
---
```

### Talks Page (talks.md)

The talks page supports flexible metadata with optional links and YouTube video embeds:

```yaml
---
layout: talks
title: "Talks"
permalink: /talks/
last_updated: "January 2026"
description: "Conference presentations, seminars, and invited talks"

talks:
  - title: "Your Talk Title"
    meta:
      # Mix plain text and objects with optional URLs
      - text: "Conference Name"  # Object with optional URL
        url: "https://conference.com"
      - "City, Country"  # Plain text string
      - "01.2026"  # Date in MM.YYYY format
      - "|"  # Pipe separator groups metadata (renders as ' | ')
      - text: "Seminar Name"
        url: "https://seminar.com"
      - "Cambridge"
      - "12.2025"
    description: "Your talk abstract or summary..."
    youtube_id: "XnyQFTr7pqE"  # Optional: YouTube video ID for embedding
    links:  # Optional: additional links for slides, etc.
      - text: "Slides"
        url: "https://example.com/slides.pdf"
---
```

**Metadata Rendering Details:**
- Items are separated by `•` bullet points by default
- Special item `"|"` renders as `&nbsp;|&nbsp;` to separate groups
- Objects with `url` field render as clickable links (opens in new tab)
- Plain strings render as text
- YouTube videos embed responsively below the talk description

## Customization Tips

### Colors & Styling

Modify CSS variables in `assets/css/style.css`:

```css
:root {
    --color-primary: #B8724D;        /* Your brand color */
    --color-primary-dark: #9A5F42;   /* Darker variant */
    --content-max-width: 700px;      /* Content width */
    --sidebar-width: 320px;          /* Sidebar width */
}
```

### Adding New Sections

1. Create a new layout in `_layouts/`
2. Add corresponding styles to `style.css`
3. Create the markdown file with appropriate front matter

### File Organization

Your Jekyll site should be organized as follows:

```
your-academic-website/
├── _config.yml              # Site configuration
├── _layouts/                # HTML templates for different page types
│   ├── default.html         # Main template (sidebar, navigation, footer)
│   ├── cv.html              # CV page template
│   ├── projects.html        # Projects/research page template
│   ├── talks.html           # Talks page template
│   └── home.html            # Homepage template
├── _posts/                  # (Disabled - kept for reference)
├── _pages/                  # Pages (.md files)
│   ├── index.md             # Homepage
│   ├── cv.md                # CV page
│   ├── projects.md          # Projects & research page
│   ├── talks.md             # Talks page
│   └── 404.md               # 404 error page
├── assets/                  # Static files
│   ├── css/
│   │   └── style.css        # Main stylesheet with CSS variables
│   ├── images/              # Images for profile, projects, etc.
│   │   ├── profile.jpg      # Profile picture
│   │   └── project-preview.png
│   └── files/               # PDFs and downloadable files
├── robots.txt              # Search engine instructions
├── Gemfile                 # Ruby dependencies
└── README.md               # Repository documentation
```

**Key Directories:**

- `_layouts/`: HTML templates for different page types
- `_pages/`: Markdown files for main pages
- `assets/`: Static files (CSS, images, PDFs)

## Deployment

### GitHub Pages

1. Push your repository to GitHub
2. Go to Settings > Pages
3. Select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Your site will be available at `https://username.github.io/repository-name`

### Serving at Root Domain (Optional)

To serve your site at `yourusername.github.io` instead of `yourusername.github.io/repository-name`:

1. **Rename your repository** to `yourusername.github.io` (must match your GitHub username exactly)
2. Update your `_config.yml`:

   ```yaml
   baseurl: ""  # Leave empty for root domain
   url: "https://yourusername.github.io"
   ```

3. Update your `robots.txt`:

   ```txt
   Sitemap: https://yourusername.github.io/sitemap.xml
   ```

Note: You can only have one `username.github.io` repository per GitHub account.

## Troubleshooting

- **Build errors**: Check `_config.yml` syntax and front matter formatting
- **Styling issues**: Verify CSS file paths and variable names
- **Math not rendering**: Ensure MathJax configuration is correct in `default.html`
- **Images not loading**: Check file paths and case sensitivity

For more help, refer to the [Jekyll documentation](https://jekyllrb.com/docs/).

## Deployment

Push to GitHub and enable Pages in repository settings. Your site will be available at `https://yourusername.github.io/repository-name`.

## Documentation

For more help, refer to the [Jekyll documentation](https://jekyllrb.com/docs/).

## Credits

This Jekyll academic website template was originally created by [Paul Gondolf](https://paul-the-wizord.github.io) and is distributed under a dual license:

- **Template Code**: MIT License - free to use, modify, and distribute
- **Personal Content**: Copyright protected - requires permission

## License

This project uses a dual licensing approach:

- **Template & Code**: Licensed under the MIT License - see [LICENSE-CODE](LICENSE-CODE)
- **Personal Content**: All rights reserved - see [LICENSE-CONTENT](LICENSE-CONTENT)

The Jekyll template, layouts, and styling may be freely used. Personal content
(CV, research info, photos) requires permission.
