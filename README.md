# Nana's Booklets

A Jekyll-based booklet visualizer for GitHub Pages that organizes academic content into structured booklets with chapters and table of contents.

## Features

- 📚 **Organized Booklets**: Each booklet contains multiple chapters
- 📝 **Table of Contents**: Automatic generation for easy navigation  
- 🎨 **Clean Design**: Minimal, academic-focused styling
- 📱 **Responsive**: Works on desktop and mobile devices
- ⚡ **GitHub Pages**: Easy deployment with Jekyll

## Structure

```
booklets/
├── _booklets/             # All booklet and chapter files in one collection
│   ├── calculus.md               # Main booklet file
│   ├── calculus/                 # Calculus chapters
│   │   ├── chapter1-limits.md
│   │   └── chapter2-derivatives.md
│   ├── linear-algebra.md         # Main booklet file
│   └── linear-algebra/           # Linear algebra chapters
│       ├── chapter1-vectors.md
│       ├── chapter2-matrices.md
│       └── chapter3-transformations.md
├── _layouts/              # Jekyll templates
├── assets/css/           # Stylesheets
└── _config.yml           # Jekyll configuration
```

## Adding New Booklets

1. Create a new main booklet file in `_booklets/` directory (e.g., `physics.md`) with this front matter:

```yaml
---
title: "Your Booklet Title"
subtitle: "Optional subtitle"
author: "Author Name"
description: "Brief description of the booklet"
date: 2024-01-01
slug: "subject-name"
---
```

2. Create a subdirectory for the booklet's chapters (e.g., `_booklets/physics/`)

3. Add chapter files in the booklet's subdirectory with this front matter:

```yaml
---
layout: chapter
booklet: "subject-name"
booklet_title: "Your Booklet Title"
booklet_subtitle: "Optional subtitle"
booklet_author: "Author Name"
chapter_number: 1
title: "Chapter Title"
subtitle: "Chapter subtitle"
author: "Author Name"
---
```


## Local Development

1. Install Ruby and Bundler
2. Run `bundle install`
3. Start the development server: `bundle exec jekyll serve`
4. Open http://localhost:4000

## Deployment

This site is configured for GitHub Pages deployment. Simply:
1. Push to your GitHub repository
2. Enable GitHub Pages in repository settings
3. Set source to "Deploy from a branch" and select `main`

## Customization

- **Styling**: Edit `assets/css/style.css`
- **Layout**: Modify files in `_layouts/`
- **Configuration**: Update `_config.yml`

The current design is inspired by clean, academic websites with focus on readability and mathematical content display.
