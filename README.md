# Personal Portfolio - John Doe

A modern, responsive portfolio website built with Jekyll and hosted on GitHub Pages.

**Live site:** [mneudobno.github.io](https://mneudobno.github.io)

## Features

- Dark theme with gradient accents
- Responsive design with mobile navigation
- Skills showcase with proficiency levels
- Project portfolio with individual detail pages
- Work experience timeline
- SEO optimized with sitemap and meta tags

## Local Development

```bash
# Install dependencies
bundle install

# Start development server
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

The site will be available at `http://localhost:4000`

## Project Structure

```
├── _config.yml        # Site configuration
├── _data/             # YAML data files (skills, experience, navigation)
├── _includes/         # Reusable components (header, footer, project-card)
├── _layouts/          # Page templates
├── _projects/         # Project collection (markdown files)
├── assets/css/        # Stylesheets
├── index.md           # Homepage
├── about.md           # About/Resume page
├── projects.md        # Projects listing
└── contact.md         # Contact page
```

## Adding a New Project

Create a markdown file in `_projects/`:

```yaml
---
title: Project Name
description: Brief description
tech: [React, Node.js, PostgreSQL]
github: https://github.com/user/repo
live: https://live-demo.com
featured: true
image: /assets/images/project.png
---

Detailed project description here...
```

## Customization

- **Personal info:** Edit `_config.yml` (name, email, location, social links)
- **Skills:** Edit `_data/skills.yml`
- **Experience:** Edit `_data/experience.yml`
- **Education:** Edit `_data/education.yml`
- **Styling:** Edit `assets/css/main.css`

## License

MIT
