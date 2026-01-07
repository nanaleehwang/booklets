# Booklet Visualizer

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
├── _booklets/          # Markdown booklets
│   ├── linear-algebra.md
│   └── calculus.md
├── tex-sources/        # Original LaTeX files (optional)
│   ├── linear-algebra/
│   │   ├── chapter1-vectors.tex
│   │   └── chapter2-matrices.tex
│   └── calculus/
│       └── chapter1-limits.tex
├── _layouts/           # Jekyll templates
├── assets/css/         # Stylesheets
└── _config.yml         # Jekyll configuration
```

## Adding New Booklets

1. Create a new file in `_booklets/` directory
2. Use the following front matter structure:

```yaml
---
title: "Your Booklet Title"
subtitle: "Optional subtitle"
author: "Author Name"
description: "Brief description of the booklet"
date: 2024-01-01
chapters:
  - title: "Chapter 1 Title"
    content: |
      Your chapter content in Markdown format.
      
      ## Section Headers
      Content here...
      
  - title: "Chapter 2 Title"
    content: |
      More content...
---
```

## LaTeX Integration

The `tex-sources/` directory is provided for organizing original LaTeX files that correspond to your booklets. While not required for the Jekyll site to function, it helps maintain the source files for your mathematical content.

To convert LaTeX to Markdown:
1. Place your `.tex` files in appropriate directories under `tex-sources/`
2. Convert mathematical expressions to MathJax format
3. Update the corresponding booklet file in `_booklets/`

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