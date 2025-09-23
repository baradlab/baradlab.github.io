# Barad Lab Jekyll Website - GitHub Copilot Instructions

**ALWAYS follow these instructions first and fallback to additional search and context gathering only if the information here is incomplete or found to be in error.**

## Overview
The Barad Lab website is a Jekyll-based static site using GitHub Pages. It features academic publications, lab member profiles, news posts, and contact information. The site is built with Ruby/Jekyll, uses Bootstrap for styling, and deploys automatically via GitHub Pages.

## Working Effectively

### Essential Environment Setup
1. **Install system dependencies:**
   ```bash
   sudo apt-get update && sudo apt-get install -y ruby-bundler
   ```

2. **Install project dependencies (REQUIRED before any other operations):**
   ```bash
   cd /path/to/repository
   sudo bundle install
   ```
   - **NOTE:** May show warnings about running as root - this is expected and safe in development environments
   - **Timing:** Takes 60-90 seconds to complete
   - **NEVER CANCEL:** Wait for completion even if it appears to hang

### Build and Development

3. **Build the site:**
   ```bash
   bundle exec jekyll build
   ```
   - **Timing:** Completes in under 1 second 
   - **Output:** Generates `_site/` directory with static files

4. **Development server (recommended):**
   ```bash
   bundle exec jekyll serve --host 0.0.0.0 --port 4000 --livereload
   ```
   - **Timing:** Starts in 2-3 seconds
   - **Access:** http://localhost:4000
   - **Features:** Auto-rebuilds on file changes, live reload in browser
   - **NEVER CANCEL:** Let server run continuously during development

5. **Clean build artifacts:**
   ```bash
   bundle exec jekyll clean
   ```

### Validation and Testing

6. **Check for Jekyll warnings:**
   ```bash
   bundle exec jekyll doctor
   ```
   - Should report "Everything looks fine"

7. **Build with verbose output (for debugging):**
   ```bash
   bundle exec jekyll build --verbose
   ```

8. **ALWAYS manually test the site after changes:**
   - Start development server: `bundle exec jekyll serve --host 0.0.0.0 --port 4000`
   - Navigate to http://localhost:4000
   - Test all navigation links: home, publications, members, teaching, news, join, contact
   - Verify responsive design and content displays correctly
   - Check browser console for JavaScript errors (some CDN blocking is normal in development)

## Key Repository Structure

### Content Files
- `_config.yml` - Main Jekyll configuration
- `_data/navigation.yml` - Site navigation menu structure
- `_includes/` - Reusable HTML components (header, footer, etc.)
- `_layouts/` - Page templates (default, members, parallax, etc.)
- `_members/` - Lab member profile markdown files
- `_posts/` - News/blog posts in Jekyll format
- `_publications/` - Research publication entries
- `index.md` - Homepage content
- `Gemfile` - Ruby dependency definitions

### Generated/Build Files (DO NOT EDIT)
- `_site/` - Generated static site (excluded in .gitignore)
- `Gemfile.lock` - Ruby dependency lock file (excluded in .gitignore)

### Static Assets
- `static/css/custom.css` - Custom styling
- Various content pages: `contact/`, `join/`, `members/`, etc.

## Common Development Tasks

### Adding a New Lab Member
1. Create new file in `_members/` following existing naming pattern
2. Use YAML frontmatter with required fields: name, image, position, email, etc.
3. Add member description in Markdown format
4. Test locally with development server

### Adding a Publication
1. Create new file in `_publications/` with YYYY_lastname.md format
2. Use `_publications/_template.md.txt` as reference
3. Set `publish: true` when ready to display
4. Verify all links and metadata are correct

### Adding a News Post
1. Create new file in `_posts/` with YYYY-MM-DD-title.md format
2. Include required frontmatter: title, author, layout, group
3. Use `layout: parallax` for standard news posts

### Modifying Site Navigation
1. Edit `_data/navigation.yml`
2. Follow existing structure with name, link, and group fields
3. Test navigation changes thoroughly

## Build Timing and Performance

### Expected Command Times
- `bundle install`: 60-90 seconds (first time only)
- `bundle exec jekyll build`: < 1 second
- `bundle exec jekyll serve`: 2-3 seconds to start
- `bundle exec jekyll clean`: < 1 second
- `bundle exec jekyll doctor`: < 1 second

### NEVER CANCEL Commands
- **NEVER CANCEL** `bundle install` - may take up to 2 minutes
- **NEVER CANCEL** long-running serve processes - these should run continuously

## Troubleshooting

### Common Issues and Solutions

1. **"Permission denied" during bundle install:**
   - Use `sudo bundle install` in development environments
   - Warnings about running as root are expected and safe

2. **Jekyll command not found:**
   - Ensure bundler is installed: `sudo apt-get install ruby-bundler`
   - Run commands with `bundle exec` prefix

3. **Site not loading external assets (CDN errors):**
   - This is normal in development - external CDNs may be blocked
   - Site functionality remains intact
   - External assets load correctly in production

4. **Changes not appearing:**
   - Ensure development server is running with `--livereload`
   - Check that files are being saved properly
   - Restart server if configuration files were changed

5. **Build fails:**
   - Run `bundle exec jekyll doctor` to check for issues
   - Verify YAML frontmatter syntax in content files
   - Check for liquid template syntax errors

## Important Notes

### Testing Requirements
- **ALWAYS** start development server and manually test changes
- **ALWAYS** verify navigation works across all sections
- **ALWAYS** check responsive design on different screen sizes
- **ALWAYS** test any new content additions (members, publications, posts)

### No Automated Testing
- This repository has NO automated test suite
- This repository has NO CI/CD pipeline currently
- This repository has NO linting tools configured
- Manual validation is critical for all changes

### Deployment
- Site automatically deploys via GitHub Pages when pushed to main branch
- No manual deployment steps required
- Changes appear live within 2-3 minutes of pushing to main

## Content Guidelines

### Publication Entries
- Use CDN URLs for images and PDFs: `https://cdn.baradlab.com/file/baradlabweb/`
- Include all available metadata: PMID, DOI, GitHub links, etc.
- Bold lab member names with `**Name**` syntax
- Set `publish: true` only when entry is complete

### Member Profiles
- Use high-quality images in consistent format
- Include ORCID, GitHub, social media links where available
- Write descriptions in first person for consistency
- Include pronouns and contact information

### News Posts
- Use descriptive filenames with YYYY-MM-DD prefix
- Include author information and publication date
- Use appropriate layout (usually `parallax`)
- Include relevant images with CDN URLs

Remember: This is an academic website representing the Barad Lab, so maintain professional tone and accuracy in all content.