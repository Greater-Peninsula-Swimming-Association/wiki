# GPSA Wiki Deployment Guide

This document outlines the deployment setup and next steps to get wiki.gpsaswimming.org live.

## ✅ What's Been Completed

### 1. Repository Structure
- ✅ Migrated all wiki content from monolithic repository
- ✅ Copied Jekyll infrastructure (_layouts, _includes, css)
- ✅ Created standalone _config.yml for wiki subdomain
- ✅ Updated all internal links (removed `/wiki/` prefixes)
- ✅ Updated navigation sidebar for standalone structure

### 2. Build Configuration
- ✅ Created Gemfile with Jekyll dependencies
- ✅ Created GitHub Actions workflow (`.github/workflows/jekyll.yml`)
- ✅ Created .gitignore for Jekyll build artifacts
- ✅ Created CNAME file for custom domain

### 3. Content Files
All documentation pages migrated:
- index.md (homepage)
- about.md
- faq.md
- meet-preparation.md
- meet-schedule-generator.md
- publicity-processor.md
- roster-formatter.md
- roster-submittal.md
- scorekeeper.md
- swimtopia-guidelines.md
- time-drops.md
- CLAUDE.md (AI assistant guidance)

### 4. Assets
- ✅ SwimTopia screenshots (assets/swimtopia/)
- ✅ GPSA logo (assets/gpsa_logo.png)
- ✅ All CSS files (css/)

## 🚀 Next Steps to Deploy

### Step 1: Commit and Push to GitHub

```bash
# Stage all files
git add .

# Commit
git commit -m "Initial wiki migration: Complete Jekyll setup with GitHub Actions

- Migrate all wiki content from monolithic repo
- Set up Jekyll layouts and includes
- Configure GitHub Actions for automated deployment
- Add custom domain (wiki.gpsaswimming.org) via CNAME
- Update all internal links for standalone structure"

# Push to GitHub
git push origin main
```

### Step 2: Enable GitHub Pages

1. Go to repository Settings on GitHub
2. Navigate to **Pages** (left sidebar)
3. Under "Build and deployment":
   - Source: **GitHub Actions** (not "Deploy from a branch")
4. The GitHub Actions workflow will handle the rest

### Step 3: Configure DNS

Add a CNAME record in your DNS provider:

```
Type: CNAME
Name: wiki
Value: [your-github-org].github.io
TTL: 3600 (or Auto)
```

**Example:**
- If your GitHub org is `GPSA-Swimming`
- CNAME: `wiki.gpsaswimming.org` → `GPSA-Swimming.github.io`

### Step 4: Verify Custom Domain in GitHub

1. In repository Settings → Pages
2. Under "Custom domain", enter: `wiki.gpsaswimming.org`
3. Click "Save"
4. Enable "Enforce HTTPS" (after DNS propagates, ~10 minutes)

### Step 5: Test Deployment

After DNS propagates (5-30 minutes):

1. Visit https://wiki.gpsaswimming.org
2. Verify homepage loads
3. Test navigation links
4. Check that all pages render correctly
5. Test mobile responsiveness
6. Verify TOC functionality on pages with `toc: true`

## 📋 Deployment Checklist

- [ ] Repository pushed to GitHub
- [ ] GitHub Actions workflow runs successfully
- [ ] GitHub Pages enabled with "GitHub Actions" source
- [ ] DNS CNAME record created
- [ ] Custom domain configured in GitHub Pages settings
- [ ] HTTPS enabled
- [ ] Site loads at wiki.gpsaswimming.org
- [ ] All pages accessible
- [ ] Navigation works
- [ ] Images load correctly
- [ ] Mobile layout works

## 🔍 Troubleshooting

### GitHub Actions Build Fails

**Check the Actions tab:**
1. Go to repository → Actions
2. Click on failed workflow run
3. Review error logs

**Common issues:**
- Missing Gemfile.lock: Fixed by `bundler-cache: true` in workflow
- Ruby version mismatch: Workflow uses Ruby 3.1
- Missing dependencies: All specified in Gemfile

### Custom Domain Not Working

**DNS Propagation:**
- Wait 10-30 minutes after creating CNAME record
- Check DNS with: `nslookup wiki.gpsaswimming.org`
- Should point to `[github-org].github.io`

**GitHub Pages Configuration:**
- Ensure CNAME file exists in repository root
- Verify custom domain setting in GitHub Pages
- Check "Enforce HTTPS" is enabled (after DNS propagates)

### Pages Return 404

**Verify:**
- GitHub Actions build completed successfully
- CNAME file contains correct domain
- Pages are accessed without trailing .html (e.g., `/about` not `/about.html`)

### CSS Not Loading

**Check:**
- CSS files are in `/css/` directory
- Layout references `/css/gpsa-tools-common.css` correctly
- Build artifacts include CSS files

### Images Not Loading

**Verify:**
- Images are in `/assets/` directory
- Image paths in markdown are correct (e.g., `/assets/swimtopia/image1.png`)
- External images (GPSA logo CDN) are accessible

## 🔄 Continuous Deployment

After initial setup, deployment is automatic:

1. Edit markdown files locally or on GitHub
2. Commit and push to `main` branch
3. GitHub Actions automatically builds and deploys
4. Changes appear at wiki.gpsaswimming.org within 1-2 minutes

## 📁 Repository Structure

```
wiki/
├── .github/
│   └── workflows/
│       └── jekyll.yml          # Automated deployment workflow
├── _config.yml                 # Jekyll configuration
├── _layouts/
│   ├── wiki.html              # Main wiki layout template
│   └── sample-wiki.html       # Sample/demo layout
├── _includes/
│   └── wiki-nav.html          # Sidebar navigation component
├── assets/
│   ├── gpsa_logo.png          # GPSA logo
│   └── swimtopia/             # SwimTopia screenshots
├── css/
│   ├── gpsa-main.css          # GPSA brand styling
│   ├── gpsa-tools-common.css  # Common tool styles
│   └── *.css                  # Other stylesheets
├── *.md                       # Wiki content pages
├── CNAME                      # Custom domain configuration
├── Gemfile                    # Ruby dependencies
├── .gitignore                 # Git ignore rules
├── README.md                  # Wiki authoring guide
├── CLAUDE.md                  # AI assistant guidance
└── DEPLOYMENT.md              # This file
```

## 🌐 URLs After Deployment

- **Production:** https://wiki.gpsaswimming.org
- **Homepage:** https://wiki.gpsaswimming.org/
- **Example pages:**
  - https://wiki.gpsaswimming.org/about
  - https://wiki.gpsaswimming.org/roster-formatter
  - https://wiki.gpsaswimming.org/scorekeeper

## 🔗 Related Resources

- **Main GPSA Site:** https://www.gpsaswimming.org
- **Main Repo:** Greater-Peninsula-Swimming-Association.github.io
- **GitHub Actions Docs:** https://docs.github.com/en/actions
- **GitHub Pages Docs:** https://docs.github.com/en/pages
- **Jekyll Docs:** https://jekyllrb.com/docs/

## 📞 Support

For deployment issues:
- Check GitHub Actions logs
- Review this deployment guide
- Contact GPSA webmaster
- Check GitHub Pages documentation

---

**Ready to deploy?** Follow the steps in "Next Steps to Deploy" above!
