---
title: Season Archive Guide
toc: true
last_updated: January 2026
---

This guide explains how to maintain the GPSA season results archive. The archive is **automatically built** when result files are committed - manual intervention is only needed when setting up a new season.

## Quick Start: New Season Setup

To set up a new season (e.g., 2026):

1. Create the year folder: `results/2026/`
2. Create `divisions.csv` with team assignments (see format below)
3. Commit both to the repository
4. Add result HTML files as meets complete - the archive rebuilds automatically

## How It Works

### Automated Build Process

A GitHub Action automatically rebuilds the season archive when:

- HTML result files are added to `results/YYYY/`
- The `divisions.csv` file is added or updated
- Someone manually triggers a rebuild

The action runs `build_archive.py` which:

1. Reads all HTML result files in the year folder
2. Extracts scores from each meet
3. Calculates division standings (wins/losses)
4. Generates the `index.html` archive page

### File Structure

```
results/
├── index.html              # Main results landing page
├── 2025/
│   ├── divisions.csv       # Team division assignments (required)
│   ├── index.html          # Generated archive page (auto-built)
│   ├── 2025-06-16_GG_v_WW.html
│   ├── 2025-06-16_HW_v_CV.html
│   └── ...
└── 2026/
    ├── divisions.csv
    ├── index.html
    └── ...
```

## Creating divisions.csv

The `divisions.csv` file tells the archive builder which teams are in which division. This is **required** for the archive to build.

### Format

```csv
season,team_code,division
2026,WPPI,red
2026,WO,red
2026,MBKM,red
2026,COL,red
2026,RMMR,red
2026,POQ,red
2026,CV,white
2026,WYCC,white
2026,GG,white
2026,HW,white
2026,WW,white
2026,GWRA,white
2026,KCD,blue
2026,JRCC,blue
2026,RRST,blue
2026,BLMA,blue
2026,EL,blue
```

### Team Codes

Use these abbreviations in the `team_code` column:

| Code | Team |
|------|------|
| BLMA | Beaconsdale |
| COL | Colony |
| CV | Coventry |
| EL | Elizabeth Lake |
| GG | Glendale |
| GWRA | George Wythe |
| HW | Hidenwood |
| JRCC | James River |
| KCD | Kiln Creek |
| MBKM | Marlbank |
| NHM | Northampton |
| POQ | Poquoson |
| RRST | Riverdale |
| RMMR | Running Man |
| WW | Wendwood |
| WO | Willow Oaks |
| WPPI | Windy Point |
| WYCC | Warwick Yacht |

**Note:** Use the filename abbreviations (BLMA, MBKM, WPPI) not the full abbreviations (BLMAR, MBKMT, WPPIR). The script handles the conversion automatically.

### Division Values

Use lowercase division names:

- `red`
- `white`
- `blue`

## Adding Meet Results

### File Naming Convention

Result files **must** follow this naming pattern:

```
YYYY-MM-DD_HOME_v_AWAY.html
```

Examples:
- `2025-06-16_GG_v_WW.html`
- `2025-07-14_KCD_v_RRST.html`

**Important:** The archive builder parses the filename to determine the date and teams. Incorrect naming will cause the meet to be skipped or misattributed.

### Where Results Come From

Result HTML files are generated using the [Publicity Processor](publicity-processor.md):

1. Export SDIF results from Meet Maestro after the meet
2. Process through the Publicity Processor tool
3. Save with the correct filename format
4. Commit to the appropriate `results/YYYY/` folder

See [Publicity Submittal Process](publicity-submittal.md) for detailed instructions.

## Manual Archive Rebuild

If you need to manually trigger a rebuild (e.g., after fixing a result file):

1. Go to the repository on GitHub
2. Click **Actions** tab
3. Select **Build Season Archive** workflow
4. Click **Run workflow**
5. Optionally enter a specific year, or leave blank to rebuild all

## Viewing the Archive

The season archives are published at:

- **All seasons:** https://www.gpsaswimming.org/results/
- **Specific year:** https://www.gpsaswimming.org/results/2025/

Each season archive includes:

- Division standings tables (wins/losses)
- Links to individual meet results
- Meet schedule with scores

## Troubleshooting

### Archive Not Building

**Check the GitHub Actions log:**

1. Go to repository → Actions tab
2. Find the failed workflow run
3. Check the error messages

**Common causes:**

- Missing `divisions.csv` - the archive won't build without it
- Malformed CSV - check for extra commas or missing columns
- Invalid HTML files - ensure files are valid HTML from Publicity Processor

### Team Missing from Standings

**Cause:** Team not listed in `divisions.csv`

**Solution:** Add the team to `divisions.csv` with correct division assignment and commit

### Meet Not Appearing

**Cause:** Filename doesn't match expected pattern

**Solution:** Rename file to `YYYY-MM-DD_HOME_v_AWAY.html` format

### Wrong Scores Displayed

**Cause:** HTML file contains incorrect data

**Solution:**
1. Re-export from Meet Maestro
2. Re-process through Publicity Processor
3. Replace the HTML file and commit

## Best Practices

### Pre-Season

1. Create the year folder early (e.g., `results/2026/`)
2. Add `divisions.csv` as soon as division assignments are finalized
3. Commit and verify the empty archive page generates

### During Season

1. Submit results within 24-48 hours of each meet
2. Use consistent filename formatting
3. Verify meets appear in the archive after committing

### Post-Season

1. Verify all meets are accounted for in the archive
2. Check division standings are correct
3. Archive is automatically preserved for historical reference

## Related Resources

- [Publicity Processor](publicity-processor.md) - Generate result HTML files
- [Publicity Submittal Process](publicity-submittal.md) - End-to-end results workflow
- [GPSA Rulebook - Scoring](https://rulebook.gpsaswimming.org/scoring.html) - Official scoring rules
