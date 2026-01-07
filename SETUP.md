# Setup Instructions

## Fixed Bundle Install Issues

The `bundle install` errors were caused by Ruby 3.4+ compatibility issues where several gems are no longer part of the default Ruby installation. 

### Solution Applied:

1. **Configured local gem installation**:
   ```bash
   bundle config set --local path 'vendor/bundle'
   ```

2. **Added required gems to Gemfile**:
   - `csv` - CSV handling
   - `logger` - Logging functionality  
   - `base64` - Base64 encoding/decoding
   - `erb` - ERB template processing
   - `ostruct` - OpenStruct functionality
   - `bigdecimal` - BigDecimal support

3. **Updated platform specification** to remove deprecated `:mingw` warnings

## Commands to Run:

```bash
# Initial setup
bundle config set --local path 'vendor/bundle'
bundle install

# Build the site
bundle exec jekyll build

# Run development server
bundle exec jekyll serve

# Run development server accessible from other machines
bundle exec jekyll serve --host 0.0.0.0
```

## Deployment:
- The site is configured for GitHub Pages with automatic deployment via GitHub Actions
- Push to main branch will trigger automatic build and deployment
- Generated site will be available at your GitHub Pages URL

## Local Development:
- Site will be available at `http://localhost:4000/booklets/`
- The `vendor/bundle` directory contains all gems locally
- This directory is git-ignored to keep the repository clean