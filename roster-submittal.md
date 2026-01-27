---
title: Roster Submittal Process
toc: true
last_updated: January 2026
---

This guide walks GPSA team representatives and administrators through the complete process of publishing team rosters to the league SwimTopia site.

## Quick Reference

- **When to publish:** Prior to first dual meet and whenever roster changes
- **Tool used:** [GPSA Roster Formatter](https://publicity.gpsaswimming.org/tools/roster.html)
- **Data source:** SwimTopia Athlete Roster CSV export
- **Where to publish:** Your team's roster page on the league SwimTopia site

## Before You Start

Before using the formatter tool, gather the following:

### 1. Export Your Roster CSV

1. Log in to your **team's** SwimTopia website with admin access
2. Navigate to **Reports > Athlete Roster**
3. Click **Generate Report**
4. Click **Download Athlete Roster Data (CSV)** (top right)
5. Save the file to your computer

### 2. Gather Contact Information

**GPSA Representatives** - Your team's designated league representatives:
- Full name, phone number, email address
- Most teams have 1-2 GPSA Representatives

**Coaches** - Head coach and assistant coaches:
- Full name, phone number (optional), email address

### 3. Gather Officials List

**Stroke & Turn Judges** - Officials certified to judge stroke technique and turn legality

**Starter / Referee** - Officials certified as starters or meet referees

---

## Step-by-Step Walkthrough

### Logging into the GPSA Site

**1.** Log into the league SwimTopia site

![Login to league site](/assets/images/managing-rosters/image9.png)

![Logged in view](/assets/images/managing-rosters/image22.png)

**2.** Go to the Meet Schedule page

![Meet Schedule page](/assets/images/managing-rosters/image16.png)

**3.** Click on your team name - This will open your team's roster page in a new tab

![Click team name](/assets/images/managing-rosters/image3.png)

**4.** Also click on the GPSA Roster Formatting Tool link - This will open the GPSA Roster Formatter in a new tab

> **Tip:** It's best to have both your team's roster tab and the GPSA Roster Formatter tab open next to each other to aid in copying information between the two.

![Both tabs open](/assets/images/managing-rosters/image23.png)

**5.** In the top right corner, select **Edit Page Content**

![Edit Page Content](/assets/images/managing-rosters/image20.png)

---

### Updating Team Contacts

**1.** Select the **Contacts** tab of the Swim Team Roster Formatter

![Contacts tab](/assets/images/managing-rosters/image17.png)

**2.** Input the necessary information for your team's GPSA Rep(s) and Coach(es). Format phone numbers as: `123-456-7890`

**3.** Click the **Export Contacts HTML** button

![Export Contacts HTML](/assets/images/managing-rosters/image21.png)

**4.** Click the **Copy Code** button

![Copy Code](/assets/images/managing-rosters/image6.png)

**5.** Click the **Edit** icon for the Team Contacts snippet

![Edit Team Contacts](/assets/images/managing-rosters/image13.png)

**6.** Click the **HTML editor** button (the `<>` icon)

![HTML editor button](/assets/images/managing-rosters/image11.png)

**7.** Select all existing text and delete it

**8.** Paste the HTML code into the Contacts snippet editor

**9.** Press **Update**

![Paste and Update](/assets/images/managing-rosters/image24.png)

---

### Updating the Team Roster

**1.** Click on the **Roster Input** tab of the Swim Team Roster Formatter

**2.** Click to upload your team's CSV export from your team's SwimTopia site

![Roster Input tab](/assets/images/managing-rosters/image7.png)

![CSV uploaded](/assets/images/managing-rosters/image12.png)

**3.** Click the **Export Roster** button

![Export Roster](/assets/images/managing-rosters/image10.png)

**4.** Click the **Copy Code** button

![Copy Code](/assets/images/managing-rosters/image8.png)

**5.** Click the **Edit** icon for the Athlete Roster snippet

![Edit Athlete Roster](/assets/images/managing-rosters/image5.png)

**6.** Click the **HTML editor** button

![HTML editor](/assets/images/managing-rosters/image1.png)

**7.** Select all existing text and delete it

**8.** Paste the HTML code into the Athlete Roster snippet editor

**9.** Press **Update**

![Paste and Update](/assets/images/managing-rosters/image19.png)

---

### Updating the Team List of Certified Officials

**1.** Click on the **Officials** tab of the Swim Team Roster Formatter

**2.** Paste in the lists of certified officials (one name per line in each box)

**3.** Click the **Export Officials HTML** button

![Officials tab and Export](/assets/images/managing-rosters/image15.png)

**4.** Click the **Copy Code** button

**5.** Click the **Edit** icon for the Certified Officials snippet

![Edit Officials snippet](/assets/images/managing-rosters/image2.png)

**6.** Click the **HTML editor** button

![HTML editor](/assets/images/managing-rosters/image18.png)

**7.** Select all existing text and delete it

**8.** Paste the code into the Officials snippet

**9.** Click **Update**

![Paste and Update](/assets/images/managing-rosters/image4.png)

---

## Roster Update Process

### When to Update

Submit roster updates when:

- New swimmers join your team
- Swimmers leave your team
- Contact information changes
- Officials certifications change

### How to Update

1. Export fresh CSV from SwimTopia (for roster data changes)
2. Upload to the Roster Formatter tool
3. Your contacts and officials will load automatically from local storage
4. Update any changes to contacts or officials
5. Export and republish to the league site

> **Tip:** For minor contact updates only, you can skip the CSV upload and just export the updated contacts HTML.

---

## Troubleshooting

### "Missing required columns" Error

**Cause:** The CSV doesn't have the required columns.

**Solution:** Re-export from SwimTopia using **Reports > Athlete Roster**. Other report types may not include all required fields.

### Swimmers Appear in Wrong Age Group

**Cause:** SwimTopia age group assignments may not match GPSA age groups.

**Solution:**
- Verify swimmer birthdates in SwimTopia
- Check the age-up date setting for your team
- The tool strips gender prefixes automatically (e.g., "Boys 9-10" becomes "9-10")

### Contacts/Officials Didn't Save

**Cause:** Browser localStorage was cleared, or you're using a different browser/device.

**Solution:**
- Re-enter the information (it will auto-save)
- Use the same browser and device consistently
- Consider keeping a backup document with contact information

### Email Shows Red Border

**Cause:** The email format is invalid.

**Solution:**
- Verify the email includes `@` and a domain (e.g., `name@example.com`)
- Check for extra spaces or typos
- The border turns green when the format is valid

### Export Button Doesn't Work

**Cause:** Browser clipboard permissions or compatibility issue.

**Solution:**
- Use a modern browser (Chrome, Firefox, Safari, Edge)
- Allow clipboard permissions if prompted
- Refresh the page and try again
- The modal shows a "Copy Code" button as backup

---

## Checklist

Use this checklist to ensure complete roster submittal:

### Before You Start

- [ ] SwimTopia admin access available
- [ ] Current roster finalized in SwimTopia
- [ ] GPSA Representative contact info gathered
- [ ] Coach contact info gathered
- [ ] Officials names and certifications gathered

### Export and Format

- [ ] CSV exported from SwimTopia (Reports > Athlete Roster)
- [ ] CSV uploaded to Roster Formatter tool
- [ ] Roster preview reviewed for accuracy
- [ ] All GPSA Representatives added with valid emails
- [ ] All coaches added
- [ ] Stroke & Turn officials entered
- [ ] Starter/Referee officials entered

### Publish

- [ ] Roster HTML exported and published to league SwimTopia
- [ ] Contacts HTML exported and published
- [ ] Officials HTML exported and published
- [ ] Published page reviewed for accuracy

---

## Reference

### Required CSV Columns

The exported CSV must contain these columns (automatically included in SwimTopia exports):

| Column Name | Description | Example |
| ----------- | ----------- | ------- |
| `AgeGroup` | Age group (may include gender prefix) | `9-10`, `Boys 11-12` |
| `AthleteCompetitionCategory` | Gender code | `M` or `F` |
| `AthleteDisplayName` | Swimmer's full name | `Smith, John` |
| `AthleteAge` | Numeric age | `10` |

### Data Persistence

The formatter tool automatically saves your contacts and officials to your browser's local storage:

- Contacts and officials persist between browser sessions
- Roster data (CSV) is NOT saved and must be re-uploaded each time
- Use the same browser/device for consistency
- Use **Clear** buttons to reset saved data if needed

### Related Resources

- [Roster Formatter Tool](https://publicity.gpsaswimming.org/tools/roster.html) - The formatting tool
- [Roster Formatter Documentation](roster-formatter.md) - Detailed tool documentation
- [SwimTopia Guidelines](swimtopia-guidelines.md) - Complete SwimTopia guide

---

## Questions?

For questions about the roster submittal process:

- **Tool issues:** Contact the GPSA webmaster
- **SwimTopia export issues:** Contact SwimTopia support or your team administrator
- **Deadline questions:** Contact your division representative
