# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Jekyll-based academic personal website using the al-folio theme. The site is hosted on GitHub Pages and showcases academic publications, news, research, and personal information.

## Development Commands

### Local Development
```bash
bundle install          # Install Ruby dependencies
bundle exec jekyll serve # Start local development server (typically at http://localhost:4000)
bundle exec jekyll build # Build the site for production
```

### Dependency Management
```bash
bundle update           # Update all gems to latest versions
bundle check           # Verify dependencies are satisfied
```

## Site Architecture

### Key Configuration
- **_config.yml**: Main site configuration including personal information, social links, Jekyll settings, and plugin configuration
- **Gemfile**: Ruby dependencies for Jekyll and plugins

### Content Structure
- **_pages/**: Main site pages (about.md, publications.md, research.md, service.md, talks.md, etc.)
- **_news/**: News items displayed on the homepage (markdown files)
- **_bibliography/**: BibTeX files for publications (books.bib, preprint.bib)
- **_data/**: YAML data files (coauthors.yml)
- **assets/**: Static files including CSS, images, and PDF files

### Layout System
- **_layouts/**: HTML templates for different page types
  - `about.html`: Homepage layout with profile, news, and selected papers
  - `default.html`: Base layout for all pages
  - `bib.html`: Bibliography entry layout
  - `post.html`: Blog post layout
- **_includes/**: Reusable template components (header, footer, social links, etc.)
- **_sass/**: SCSS stylesheets for theming

### Jekyll Configuration
- Uses kramdown for markdown processing
- Jekyll Scholar plugin for bibliography management
- Jekyll Responsive Image plugin for image optimization
- Collections for news and projects

## Important Notes

### Personal Information
The site belongs to Wenbo Zhang, a Ph.D. student at University of Adelaide. Personal details are configured in `_config.yml` and `_pages/about.md`.

### Publications
Academic publications are managed through Jekyll Scholar plugin using BibTeX files in `_bibliography/`. The main bibliography file is `pubs.bib`.

### Deployment
The site is deployed to GitHub Pages automatically. The CNAME file configures the custom domain (zwbx.github.io).

### Theme
Based on the al-folio theme with local CSS/JS files for better performance. Academic-focused with support for publications, news items, and project showcases.