# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal blog built with Hugo using the PaperMod theme. Topics: Evolution, Algorithmic Trading, and Cybersecurity. Deploys to https://joseporiolcarne.github.io/

## Commands

```bash
# Start local development server
hugo server

# Start dev server with drafts visible
hugo server -D

# Build the site for production (outputs to /public)
hugo

# Create a new blog post
hugo new posts/my-new-post/index.md
```

## Architecture

- **Hugo static site** using [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme (git submodule in `themes/PaperMod`)
- **Configuration**: `hugo.toml` - site settings, menu structure, theme parameters
- **Content**: `content/` - blog posts in `content/posts/`, each post in its own directory with `index.md`
- **Custom layouts**: `layouts/partials/` - template overrides for PaperMod theme

## Content Structure

Blog posts use Hugo's page bundles pattern:
```
content/posts/my-post/
├── index.md          # Post content with front matter
└── images/           # Post-specific images (optional)
```

## Publishing to GitHub Pages

```bash
# 1. Build the site
hugo

# 2. Copy built files from public/ to root (for GitHub Pages)
cp -r public/* .

# 3. Commit and push
git add .
git commit -m "Publish: brief description"
git push origin main
```

## Blog Post Guidelines

When creating or editing blog posts, follow these SEO and readability guidelines:

- Write SEO-optimized content with relevant keywords naturally integrated
- Include a meta description (under 160 characters) in the front matter `description` field
- Ensure the reading level is suitable for a general audience
- Use clear headings and subheadings for better readability
- Choose tags that accurately reflect the post's content
