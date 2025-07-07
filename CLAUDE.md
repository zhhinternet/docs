# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Mintlify documentation site starter kit. The project uses Mintlify's platform to generate and host documentation from MDX files.

## Development Commands

### Local Development
```bash
# Install Mintlify CLI globally (note: package name is 'mint', not 'mintlify')
npm i -g mint

# Start local development server (runs on port 3000 by default)
mint dev

# Start on custom port
mint dev --port 3333

# Update CLI to latest version
mint update
```

### Validation and Troubleshooting
```bash
# Check for broken links in documentation
mint broken-links

# If encountering issues, try updating the CLI
mint update

# Common troubleshooting:
# - If dev environment isn't running: Run `mint update`
# - Page loads as 404: Make sure you're running in a folder with `docs.json`
```

## Project Structure

This is a documentation site built with Mintlify. The key components are:

- **docs.json**: Main configuration file that defines site structure, navigation, theming, and all site settings
- **MDX files**: Documentation content written in MDX (Markdown + JSX components)
- **api-reference/**: API documentation section with OpenAPI spec integration
- **essentials/**: Core documentation topics and guides
- **images/**: Static assets including hero images and screenshots
- **logo/**: Brand assets (light and dark mode SVG logos)

### Content Organization

The site is organized into two main tabs as defined in docs.json:

1. **Guides Tab**: General documentation including quickstart, development guides, and essentials
2. **API Reference Tab**: API documentation with endpoint examples and OpenAPI integration

### Key Configuration

- Navigation and site structure are controlled via `docs.json`
- Theme colors: Primary (#16A34A), Light (#07C983), Dark (#15803D)
- Supports both light and dark mode logos
- Includes social links and external anchors to Mintlify resources

## Working with This Codebase

- All content is written in MDX format, allowing for both Markdown and JSX components
- The site auto-deploys when changes are pushed to the default branch (via Mintlify GitHub App)
- Local preview is available at `http://localhost:3000` when running `mintlify dev`
- Node.js version 19 or higher is required for development

## File Types

- `.mdx`: Documentation pages and content
- `.json`: Configuration files (docs.json for site config, openapi.json for API specs)
- `.svg`: Vector graphics for logos and icons
- `.png`: Raster images for screenshots and hero images