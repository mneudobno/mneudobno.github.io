---
title: DevBlog
description: A personal blogging platform with Markdown support, syntax highlighting, and a custom CMS.
tech:
  - Next.js
  - MDX
  - Prisma
  - SQLite
  - Vercel
github: https://github.com/mneudobno/devblog
live: https://devblog-demo.vercel.app
featured: true
---

## Overview

DevBlog is a minimalist blogging platform designed specifically for developers. It combines the simplicity of writing in Markdown with powerful features like syntax highlighting and a built-in CMS.

## Why I Built This

While there are many blogging platforms available, I wanted something that:
- Supports Markdown and MDX natively
- Has beautiful code syntax highlighting
- Is fast and SEO-friendly
- Gives me full control over the design

## Key Features

- **MDX Support**: Write posts in Markdown with embedded React components
- **Syntax Highlighting**: Automatic code highlighting for 100+ languages using Prism
- **Admin Dashboard**: Built-in CMS for creating and editing posts
- **SEO Optimized**: Server-side rendering, meta tags, and sitemap generation
- **Dark Mode**: Toggle between light and dark themes
- **RSS Feed**: Automatic RSS feed generation for subscribers

## Technical Highlights

### MDX Processing
Used the MDX library to parse and render Markdown files with support for custom React components, enabling interactive elements within blog posts.

### Database Layer
Prisma ORM with SQLite provides a simple yet powerful database solution that works great for a personal blog scale.

### Static Generation
Leveraged Next.js static generation for blog posts, resulting in lightning-fast page loads and excellent Core Web Vitals scores.

## Performance Metrics

- **Lighthouse Score**: 98 Performance, 100 Accessibility
- **First Contentful Paint**: < 1s
- **Time to Interactive**: < 2s

## Lessons Learned

- Deep understanding of Next.js file-based routing and static generation
- Working with MDX and building custom plugins
- Implementing authentication and protected routes
- Deploying full-stack applications to Vercel
