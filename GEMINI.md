# Directory Overview

This directory contains the source files for the Greater Peninsula Swimming Association (GPSA) Wiki, a knowledge base for league information, web tools, and meet management procedures. The site is built using Jekyll and hosted on GitHub Pages.

The content is written in Markdown and organized into various pages covering topics such as league administration, meet management, and documentation for custom web tools.

## Key Files

*   `_config.yml`: The main Jekyll configuration file. It contains site-wide settings like the title, description, and build configurations.
*   `README.md`: Provides a comprehensive guide for contributors on how to create, edit, and manage wiki pages. It covers Markdown syntax, front matter, navigation management, and local testing.
*   `index.md`: The main landing page of the wiki. It provides a brief introduction to the GPSA and links to the main sections of the wiki.
*   `_layouts/wiki.html`: The Jekyll layout template for all wiki pages. It defines the overall structure and includes the header, footer, and navigation.
*   `_includes/wiki-nav.html`: The HTML include for the side navigation bar. This file is manually updated to add, remove, or reorder links to wiki pages.
*   `swimtopia-guidelines.md`: A detailed guide for team administrators on using SwimTopia to manage their teams, including roster management, registration, and meet entries.
*   `time-drops.md`: A comprehensive document about the Time Drops wireless swim timing system, which is used by many teams in the league.
*   `assets/`: This directory contains all the static assets for the wiki, such as images and logos.
*   `css/`: This directory contains all the CSS files for the wiki.

## Usage

This directory is used to maintain the content of the GPSA Wiki. The typical workflow for updating the wiki is:

1.  **Create or Edit a Markdown File:** Create a new `.md` file for a new page or edit an existing one. Add the necessary Jekyll front matter (layout, title, etc.).
2.  **Update Navigation:** If a new page is created, add a link to it in `_includes/wiki-nav.html`.
3.  **Test Locally (Optional):** Use `bundle exec jekyll serve` to build and serve the site locally to preview changes.
4.  **Commit and Push:** Commit the changes and push them to the `main` branch on GitHub.
5.  **Deployment:** GitHub Pages automatically builds the site from the `main` branch and deploys it to `https://wiki.gpsaswimming.org`.
