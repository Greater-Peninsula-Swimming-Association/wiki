# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a **documentation wiki** for the Greater Peninsula Swimming Association (GPSA), a youth summer swim league on the Virginia Peninsula. The wiki provides:

- League information (about, FAQ, rules)
- Web tools documentation (Meet Schedule Generator, Roster Formatter, Publicity Processor)
- Meet management guides (preparation, scorekeeper, timing systems)
- Team administration guides (roster submittal, SwimTopia guidelines)

## Content Structure

### File Organization

All documentation is in **markdown files** (`.md`) in the root directory:

- **`index.md`** - Homepage/landing page
- **League Info**: `about.md`, `faq.md`
- **Tools**: `meet-schedule-generator.md`, `roster-formatter.md`, `publicity-processor.md`
- **Meet Management**: `meet-preparation.md`, `scorekeeper.md`, `publicity-submittal.md`, `time-drops-about.md`, `time-drops-swimtopia-integration.md`
- **Team Admin**: `gpsa-rep-duties.md`, `roster-submittal.md`, `swimtopia-guidelines.md`

Navigation is defined in `_quarto.yml` under `website.sidebar.contents`.

### Frontmatter Format

Each markdown file uses **Quarto frontmatter**:

```yaml
---
title: Page Title
toc: true | false
last_updated: Month Year
---
```

**Required fields:**
- `title` - Page title (displayed as H1)

**Optional fields:**
- `toc` - Enable/disable table of contents (default: true)
- `last_updated` - Human-readable update timestamp

## Writing Documentation

### Style Guidelines

1. **Headers**: Use ATX-style headers (`#`, `##`, `###`)
2. **Code blocks**: Use fenced code blocks with language identifiers
3. **Tables**: Use GitHub-flavored Markdown tables
4. **Links**: Use reference-style links for external URLs, relative paths for internal
5. **Lists**: Use `-` for unordered lists, numbers for ordered lists

### Internal Linking

Link to other wiki pages using **relative paths**:

```markdown
[Roster Formatter](roster-formatter.md)
[Meet Schedule Generator](meet-schedule-generator.md)
[About GPSA](about.md)
```

For section links within a page:
```markdown
[Scorekeeper Post-Meet](scorekeeper.md#post-meet-procedures)
```

## Cross-Referencing Standards

**Philosophy:** The wiki should not duplicate content from the rulebook. Instead, provide practical how-to guidance and link to the rulebook for authoritative rules. Every wiki page should be well-connected to related resources.

### Rulebook Links

The GPSA Rulebook is published at `https://rulebook.gpsaswimming.org/`. Always link to relevant rulebook sections when discussing rules or procedures.

**When to add rulebook links:**
- Any mention of official rules, requirements, or procedures
- Deadlines and consequences defined by league rules
- Role responsibilities (officials, representatives, coaches)
- Scoring, eligibility, protests, postponements

**Link format:**
```markdown
See [GPSA Rulebook - Section Name](https://rulebook.gpsaswimming.org/page.html#section-anchor).
```

**Available rulebook pages:**
- `officials.html` - Roles, responsibilities, certification
- `conduct-of-meets.html` - Meet procedures, scheduling, protests
- `eligibility-and-rosters.html` - Roster rules, eligibility
- `scoring.html` - Scoring system
- `awards.html` - Award procedures
- `order-of-events.html` - Event order
- `facilities.html` - Pool requirements
- `definitions.html` - Term definitions

### Wiki Cross-References

Link to related wiki pages throughout content where contextually relevant.

**When to add wiki links:**
- First mention of a process that has its own guide
- References to tools, procedures, or roles with dedicated pages
- "See also" or "for more details" contexts
- Tables listing roles or equipment (link role names to their guides)

**Examples of good contextual linking:**
```markdown
| [Scorekeeper](scorekeeper.md) | 1 |
```

```markdown
After the meet, [submit results](publicity-submittal.md) within 24 hours.
```

```markdown
See [Meet Preparation Guide](meet-preparation.md) for detailed instructions.
```

### Required Links for New Pages

When creating or substantially modifying a wiki page:

1. **Add a "Related Resources" section** at the bottom with links to:
   - Related wiki pages
   - Relevant rulebook sections

2. **Link contextually throughout the content** - don't just dump links at the bottom

3. **Update other pages** that should link to the new content

4. **Update navigation** in `_quarto.yml` if adding a new page

### Team Abbreviations

Use these **standard team abbreviations** consistently:

| Abbreviation | Team Name |
|--------------|-----------|
| BLMAR | Beaconsdale |
| COL | Colony |
| CV | Coventry |
| EL | Elizabeth Lake |
| GG | Glendale |
| GWRA | George Wythe |
| HW | Hidenwood |
| JRCC | James River |
| KCD | Kiln Creek |
| MBKMT | Marlbank |
| NHM | Northampton |
| POQ | Poquoson |
| RRST | Riverdale |
| RMMR | Running Man |
| WW | Wendwood |
| WO | Willow Oaks |
| WPPIR | Windy Point |
| WYCC | Warwick Yacht |

### Division Structure

GPSA has three divisions:
- **Red Division**
- **White Division**
- **Blue Division**

### Age Groups

Standard age groups (age as of June 1st):
- 6 & Under
- 7-8
- 9-10
- 11-12
- 13-14
- 15-18

## Tools Documentation Pattern

When documenting web tools (like the three existing tools), follow this structure:

1. **Quick Start** - Step-by-step minimal instructions
2. **What It Does** - High-level overview
3. **Getting the Input File** - How to obtain required files (CSV, SDIF, etc.)
4. **Required Format** - Table of required columns/fields
5. **Using the Tool** - Step-by-step detailed instructions
6. **Output Format** - What gets generated
7. **Troubleshooting** - Common errors and solutions
8. **Best Practices** - Organized by role (Team Reps, Webmasters, etc.)
9. **Technical Details** - Libraries, browser compatibility, file limits
10. **Related Tools** - Links to other relevant tools
11. **Support** - Contact information

## GPSA Technical Context

### File Formats

- **SDIF (.sd3, .txt)** - Swimming Data Interchange Format for meet results
- **CSV** - Used for schedules and rosters (exported from SwimTopia)
- **HY3** - NOT supported (use SDIF instead)

### File Naming Conventions

Meet results follow strict naming:
```
YYYY-MM-DD_TEAM1_v_TEAM2.html
Example: 2025-06-16_GG_v_WW.html
```

This format is **critical** for archive builder compatibility.

### External Tools & Services

- **SwimTopia** - League management platform (roster, meet entry, results)
- **Meet Maestro** - Scoring software used by scorekeepers
- **Time Drops** - Digital timing system used by over half of GPSA teams
- **Archive Builder** (`build_archive.py`) - Python script that processes meet results

### GPSA Brand Colors

- **Navy Blue**: `#002366` (primary)
- **Red**: `#d9242b` (secondary/accents)

## Common Maintenance Tasks

### Adding a New Page

1. Create markdown file in root: `new-page.md`
2. Add Quarto frontmatter with `title` and `last_updated`
3. Write content following style guidelines
4. **Add cross-references:**
   - Link to relevant rulebook sections throughout content
   - Link to related wiki pages where contextually appropriate
   - Add a "Related Resources" section at the bottom
5. **Update navigation:**
   - Add to `_quarto.yml` sidebar contents in appropriate section
   - Add to `index.md` in appropriate section
6. **Update other pages** that should link to the new content

### Updating Existing Documentation

1. Read the existing file to understand structure
2. Make necessary edits
3. Update `last_updated` in frontmatter if present
4. Ensure internal links still work

### Adding Tool Documentation

1. Follow the "Tools Documentation Pattern" structure above
2. Include concrete examples with real team abbreviations
3. Document all error messages and solutions
4. Add to "Web Tools Documentation" section in `index.md`

## Git Workflow

This is a standard git repository. Common commands:

```bash
# View changes
git status
git diff

# Commit changes
git add <files>
git commit -m "Descriptive message"

# Push to remote
git push origin main
```

## Assets

The `assets/swimtopia/` directory contains image assets (likely screenshots for SwimTopia guidelines).

## Important Context

- This is **documentation only** - no application code, build steps, or tests
- Content is written for swim league volunteers (team reps, coaches, webmasters)
- Audience ranges from non-technical parents to league administrators
- Documentation must be clear, concise, and action-oriented
- Screenshots and examples are highly valued for complex processes
