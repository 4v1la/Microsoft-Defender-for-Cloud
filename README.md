# Microsoft Defender for Cloud Website

A responsive, accessible website built with MkDocs Material theme for Microsoft Defender for Cloud documentation and resources.

## Features

- ✅ **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- ✅ **Accessibility**: WCAG compliant with keyboard navigation, screen reader support, and ARIA labels
- ✅ **Light/Dark Mode**: Automatic theme switching based on user preference
- ✅ **Gradient Theme**: Custom gradient color scheme using Microsoft Defender branding
- ✅ **Defender Logo**: Microsoft Defender for Cloud branding on every page
- ✅ **Blog System**: Built-in blog with posts, categories, and tags
- ✅ **Contact Page**: Contact form and support information
- ✅ **GitHub Pages**: Automated deployment via GitHub Actions
- ✅ **Azure Static Web Apps Ready**: Can be deployed to Azure Static Web Apps

## Quick Start

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/4v1la/Microsoft-Defender-for-Cloud.git
cd Microsoft-Defender-for-Cloud
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Local Development

Run the development server:
```bash
mkdocs serve
```

The site will be available at `http://127.0.0.1:8000`

### Building the Site

Build the static site:
```bash
mkdocs build
```

The built site will be in the `site/` directory.

## Project Structure

```
Microsoft-Defender-for-Cloud/
├── docs/
│   ├── assets/
│   │   ├── images/
│   │   │   ├── defender-logo.svg      # Defender logo
│   │   │   └── favicon.svg            # Site favicon
│   │   └── stylesheets/
│   │       └── custom.css             # Custom gradient styling
│   ├── blog/
│   │   ├── index.md                   # Blog home page
│   │   └── posts/                     # Blog posts directory
│   │       ├── getting-started.md
│   │       ├── top-10-security-recommendations.md
│   │       └── multi-cloud-security.md
│   ├── index.md                       # Home page
│   └── contact.md                     # Contact page
├── .github/
│   └── workflows/
│       └── deploy.yml                 # GitHub Pages deployment
├── mkdocs.yml                         # MkDocs configuration
├── requirements.txt                   # Python dependencies
├── LICENSE
└── README.md
```

## Adding Blog Posts

To add a new blog post:

1. Create a new markdown file in `docs/blog/posts/`
2. Add front matter with date, authors, categories, and tags:

```markdown
---
date: 2024-02-20
authors:
  - defender-team
categories:
  - Security
tags:
  - cloud-security
---

# Your Post Title

![Defender for Cloud](../../assets/images/defender-logo.svg){: .defender-logo }

Your introduction text here.

<!-- more -->

Your full post content here.
```

3. The post will automatically appear in the blog index

## Customization

### Colors and Theme

Edit `docs/assets/stylesheets/custom.css` to modify:
- Gradient colors
- Component styling
- Responsive breakpoints
- Accessibility features

### Logo

Replace `docs/assets/images/defender-logo.svg` with your custom logo.

### Navigation

Edit the `nav:` section in `mkdocs.yml` to modify site navigation.

## Deployment

### GitHub Pages

The site automatically deploys to GitHub Pages when you push to the `main` branch.

1. Ensure GitHub Pages is enabled in repository settings
2. Set the source to "GitHub Actions"
3. Push changes to trigger deployment

### Azure Static Web Apps

To deploy to Azure Static Web Apps:

1. Create an Azure Static Web App resource
2. Connect to your GitHub repository
3. Configure build settings:
   - App location: `/`
   - API location: (leave empty)
   - Output location: `site`
   - Build command: `pip install -r requirements.txt && mkdocs build`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the terms specified in the LICENSE file.

## Support

For questions or issues:
- Visit the [Contact Page](https://4v1la.github.io/Microsoft-Defender-for-Cloud/contact/)
- Open an issue on GitHub
- Check the [documentation](https://www.mkdocs.org/) for MkDocs

## Acknowledgments

- Built with [MkDocs](https://www.mkdocs.org/)
- Theme: [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- Blog plugin: [MkDocs Blog Plugin](https://pypi.org/project/mkdocs-blog-plugin/)
