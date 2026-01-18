# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

## Architecture

This is a Jekyll-based GitHub Pages portfolio site.

### Layout Hierarchy

- **default.html** - Base template with head, header, footer, SEO tags
- **home.html** - Homepage extending default: hero section, skills grid, featured projects (3), experience timeline (2)
- **page.html** - Generic content pages
- **project.html** - Individual project pages with metadata, tech tags, action buttons

### Data-Driven Content

Content is managed through YAML files in `_data/`:
- `navigation.yml` - Main nav links
- `skills.yml` - Technical skills with proficiency levels (organized by category)
- `experience.yml` - Work history timeline
- `education.yml` - Degrees and certifications (uses `degrees:` and `certifications:` keys)

### Projects Collection

Projects live in `_projects/` as markdown files with frontmatter:
```yaml
---
title: Project Name
description: Short description
tech: [React, Node.js, PostgreSQL]
github: https://github.com/user/repo
live: https://project-url.com
featured: true
---
```

Output to `/projects/:name/` URLs.

### Key Includes

- `header.html` - Responsive nav with separate desktop (`site-nav-desktop`) and mobile (`site-nav-mobile`) navigation
- `project-card.html` - Reusable card accepting `project` parameter
- `footer.html` - Site footer

### Styling

Single CSS file at `assets/css/main.css` with:
- CSS custom properties for colors, spacing, typography
- BEM-like class naming (`.hero-content`, `.project-card-image`)
- Mobile-responsive with separate mobile nav overlay

### Jekyll Plugins (GitHub Pages compatible)

jekyll-feed, jekyll-seo-tag, jekyll-sitemap, jekyll-avatar, jemoji, jekyll-github-metadata, jekyll-redirect-from, jekyll-relative-links, jekyll-mentions

### URL Redirects

Configured via `redirect_from` in page frontmatter:
- `/about/` also serves `/resume/`, `/cv/`
- `/projects/` also serves `/portfolio/`, `/work/`
