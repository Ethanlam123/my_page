# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site using the PaperMod theme. The site is configured to use PaperMod as a Git submodule and is currently set up with minimal configuration.

## Common Commands

### Development
- `hugo server` - Start local development server with live reload
- `hugo server -D` - Start server including draft content
- `hugo server --bind 0.0.0.0 --baseURL http://localhost:1313` - Start server accessible from other devices

### Build
- `hugo` - Build the static site to `public/` directory
- `hugo -D` - Build including draft content
- `hugo --minify` - Build with minified output

### Content Management
- `hugo new posts/my-post.md` - Create new post
- `hugo new page/about.md` - Create new page
- `hugo list drafts` - List all draft content

### Theme Management
- `git submodule update --init --recursive` - Initialize/update PaperMod theme submodule
- `git submodule update --remote --merge` - Update theme to latest version

## Architecture

### Directory Structure
- `content/` - Markdown content files (currently empty)
- `layouts/` - Custom layout overrides (if needed)
- `static/` - Static assets (images, files, etc.)
- `assets/` - Assets to be processed by Hugo pipes
- `themes/PaperMod/` - PaperMod theme as Git submodule
- `public/` - Generated site output (ignored by git)
- `hugo.yaml` - Main configuration file

### Configuration
The site uses `hugo.yaml` for configuration. Key settings:
- Theme: PaperMod (managed as Git submodule)
- Base URL: https://example.org/ (should be updated for production)
- Language: English (en-us)

### PaperMod Theme
- Modern, responsive Hugo theme
- Supports multiple modes: Regular, Home-Info, Profile
- Built-in search functionality with Fuse.js
- Light/dark theme switching
- SEO optimized
- No external dependencies (webpack, nodejs) required

### Content Creation
- New content uses the archetype in `archetypes/default.md`
- Posts should be created in `content/posts/`
- Pages can be created in `content/` or subdirectories
- All new content is created as drafts by default

### Deployment
The `public/` directory contains the built site and should be deployed to your web server or hosting platform.