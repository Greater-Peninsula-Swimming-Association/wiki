---
title: Time Drops & SwimTopia Integration Setup
toc: true
last_updated: January 2026
---

This guide covers integrating the **Time Drops Timing System** with **SwimTopia's Meet Maestro** software for GPSA meets.

> **Note:** The timing configuration is per computer, not per session/team/meet. If you have a laptop set up to use a timing system, it will use that timing system for any session.

## Prerequisites

Before starting this integration, you should have:

- Time Drops hardware system (purchased and configured)
- SwimTopia team subscription with Meet Maestro access
- Meet entries already merged in SwimTopia
- Basic familiarity with Time Drops hardware setup

See [Time Drops Timing System](time-drops-about.md) for general system information.

## Hardware and Software Requirements

### Time Drops Requirements

**Critical:** The Time Drops system **cannot function without Wi-Fi**. Due to security restrictions, public Wi-Fi will most likely **not work**.

#### Required Hardware

- **Router** (2.4 GHz capable) - Not included with Time Drops
- **Android tablet** - Runs Time Drops Console App
- **Windows computer** - Runs Meet Maestro and MM-Link
- **Start adapter (SA-1)** - Included with Time Drops purchase
- **Timing controller (STC-1)** - Included with Time Drops purchase
- **Time Drops lane timer buttons (PB-2)** - Up to 3 per lane, included with purchase

#### Required Software

- **Time Drops Console App** - Free in Google Play Store
- **Time Drops MM-Link** - Free in Windows Store
- **Meet Maestro Desktop Application** - Free with SwimTopia subscription

### Meet Maestro Requirements

- **Microsoft Windows computer** with 64-bit Windows 7 or newer
  - Mac users can run Meet Maestro via Windows emulation software
- **At least 4 GB RAM** recommended (Chromebooks typically insufficient)
- **Internet connection** to download meet data
  - Mobile hotspot works for Meet Maestro (small data transfer)
  - **Important:** Time Drops does NOT work on 5 GHz wireless hotspot

## Time Drops Hardware Setup

> **Note:** If your Time Drops system is already configured, skip to [Meet Maestro Setup](#meet-maestro-setup) below.

**Setup must be done in a specific order.** Reference the [Time Drops Quick Start Guide](https://time-drops.com/quickstart.pdf) or contact Time Drops support if you have questions.

### Step 1: Router Setup

#### Configure the Router

1. **Power up the router** to create your 2.4 GHz Wi-Fi network
2. **Find the router** in your computer's WiFi networks list
3. **Open a web browser** to access the router's admin panel
   - First-time setup: Select language and set admin password
   - Subsequent logins: Enter your admin password

#### Connect to Internet

Choose your internet source in the router admin panel:

- **Tethering** (recommended): Connect phone hotspot via USB
- **Other options**: Ethernet, repeater mode, etc.

**Example Setup:**

- Router: GL.iNet SFT-1200 travel router
- Power: Anker 20,000mAh portable charger with USB-C cable
- Internet: Phone hotspot tethered via USB
- Placement: Position for clear view of pool, tablet, and STC-1 controller

#### Verify Connection

Once connected, you should see:

- Green dot next to "Tethering" (or your connection method)
- IP address displayed

### Step 2: Android Tablet Setup

1. **Log in** to the tablet with team's Time Drops Google Account
2. **Fully charge** the tablet before each meet
3. **Disable lock screen** (recommended) for quick access during meet
4. Open **Settings** → **Network & Internet**
5. **Connect to the same Wi-Fi network** created by your router

### Step 3: Time Drops Console App

The **Time Drops Console App** should already be installed on your tablet (from Google Play Store).

Open the app to verify it's working - you should see the main console interface.

### Step 4: STC-1 Controller Connection

The STC-1 has a USB rechargeable battery. **Fully charge before every meet** (lasts up to 10 hours).

#### Turn On Controller

1. Press and hold the power button on the STC-1
2. When not connected, red WiFi light blinks slowly

#### Connect to Wi-Fi

If the STC-1 doesn't automatically connect:

1. **Open Time Drops app** on tablet
2. Tap the **3 vertical dots** (upper right) → **Connect controller**
3. You'll see a red sad face if not connected
4. Tap **Choose** to select the correct WiFi network
5. Tap **Copy to Controller**
6. Watch for transmission progress bar
7. **Success:** Green happy face displays, red light blinks rapidly on STC-1

> **Troubleshooting:** If having trouble connecting, see [Time Drops Troubleshooting Guide](https://time-drops.com/user-manual.pdf).

### Step 5: Configure Lane Timer Buttons

Time Drops includes up to 3 buttons per lane. Each button has a lanyard marked with lane and button letter (e.g., Lane 1A, Lane 1B, Lane 1C).

Buttons should be pre-assigned during initial system setup. **Only reassign if:**

- Button runs out of batteries
- Button stops working and you're using a spare

#### To Assign Buttons

1. Tap **3 vertical dots** → **Buttons** in Time Drops app
2. **Press and hold** the physical button until it appears under "Unassigned"
3. **Drag** the button to correct lane and letter
4. **Tap SAVE** (grey squares mean unsaved changes)

#### Turn On Buttons

1. Press the blue button on the timer device
2. Beep sounds, faint red light blinks
3. Button shows as white (on) in the app
4. STC-1 controller shows blue blinking light when buttons connected

### Step 6: Starter Adapter (Optional)

If using a starter adapter that plugs into your starting system:

1. **Turn on the adapter:**
   - Use a small metal object (tiny screwdriver) to close circuit between two wire plugs
   - Blinking red light confirms it's on
2. **Add in app:** Same process as adding timer buttons (drag to assign)
3. **Connect to starter:** Plug cable into starter's "Starter Output" socket

**Signal Range:** Buttons have ~1,000 ft range in open terrain, reduced by walls/crowds.

**Best Practice:** Place STC-1 controller elevated with line-of-sight to start and finish areas. Example: Hang from backstroke flags in provided waterproof pouch with carabiner.

## Meet Maestro Setup

### Step 1: Download Meet Maestro Desktop App

1. Visit SwimTopia and download [Meet Maestro Windows Desktop Application](https://www.swimtopia.com/meet-maestro-download)
2. Run the installer (may take several minutes)
3. Close any currently running version before installing updates

> **Tip:** When updates are available, an "Install Update" button appears in the top bar. Application auto-downloads updates.

### Step 2: Log In and Select Time Drops

#### Log In

1. Open Meet Maestro Desktop application
2. Log in with your SwimTopia credentials
   - Must be Site Admin or have role permission to manage swim meets
   - Multiple teams: Select team first

#### Select Meet

You'll only see meets that have been **merged** (entries closed and processed).

#### Configure Timing System

1. Click **Settings** (gear icon)
2. Click **Add Timing System Configuration**
3. Select **Time Drops**

> **Note:** Desktop application is required for timing system integration. Web version shows message with link to instructions.

#### Multi-Session Meets

If this is a multi-session/virtual meet, you'll be prompted to select your session.

### Step 3: Choose Data Directory

Create a folder where Time Drops will save meet data. Both Meet Maestro and MM-Link must use the **same folder**.

**Recommended Structure:**

```text
TimeDrop Data/
  └── 2026 Season/
      ├── 2026-06-16-GG-vs-WW/
      ├── 2026-06-19-GG-vs-EL/
      └── 2026-06-23-Division-Meet/
```

**In Meet Maestro:**

1. Create new folder for this meet
2. Click **Browse** under "Data Directory"
3. Select your meet folder

### Step 4: Install and Configure MM-Link

**MM-Link** bridges Time Drops to Meet Maestro.

1. Download [Time Drops MM-Link from Microsoft Store](https://www.microsoft.com/store/apps)
2. When prompted, **enable Windows firewall access** for both 'private' and 'public' networks
3. Open MM-Link
4. Verify **green bar** shows (STC-1 and tablet connected)
5. Click **Browse** to select path for file exchange
6. Select the **SAME folder** you chose in Meet Maestro

### Step 5: Verify Configuration

1. Return to Meet Maestro
2. Click **Check Configuration**

**Success indicators:**

- **"Connected"** displays in top right
- Green checkmark shows correct meet found
- Tablet displays Event/Heat/Lane assignments

**If you see an error:**

- Directories between Meet Maestro and Time Drops don't match
- Reselect directory in both applications
- Click "Check Configuration" again

## Meet Maestro Settings

### Expected Watches Per Lane

Time Drops automatically communicates expected watches per lane to Meet Maestro (1, 2, or 3).

**Only update this if Time Drops shows an incorrect value.**

### SwimTopia Mobile App - Live Event/Heat Bar

**Enable the live event/heat bar** to show current event/heat in the SwimTopia mobile app.

1. Slide bar to **ON** (right)
2. Time Drops will automatically send current event/heat info to mobile users

**When to enable:**

- During initial setup (recommended)
- Any time via timing system bar on results entry screen

## Editing Settings and Testing

### Editing Settings After Setup

All settings can be changed from the **Timing Setup** screen:

1. Click **Settings** (gear icon) → **Timing Setup**
2. Click **Update Meet Details**

**Shortcut:** When on results entry interface, click **Update Meet Details** on timing system bar.

### Testing Before the Meet

**We HIGHLY encourage** completing setup several times before your first meet. Practice in the actual location to verify:

- Cable lengths are adequate
- Plugs and connectors work
- WiFi signal is strong enough
- Equipment positioning is optimal

#### Early Start Warning

To prevent premature swim reminders and notifications to SwimTopia mobile app users, an early start warning displays when:

1. "Enable Live Event/Heat Bar" is checked, AND
2. Meet/session start time is in the future

**What happens:**

- Warning displays for each test until you confirm "Yes, start the meet"
- Selecting "Yes..." adjusts estimated times and begins notifications
- **No option to revert** back to pre-notification state

## Next Steps

After completing this setup:

1. **Practice runs:** Test the full system several times before meet day
2. **Meet day:** Follow your team's standard meet procedures
3. **Troubleshooting:** See [Time Drops Timing System](time-drops-about.md) for general guidance

## Product Support

### Time Drops Support

For questions about Time Drops hardware or setup:

- **Website:** [time-drops.com](https://time-drops.com/)
- **User Manual:** [time-drops.com/user-manual.pdf](https://time-drops.com/user-manual.pdf)
- **Quick Start Guide:** [time-drops.com/quickstart.pdf](https://time-drops.com/quickstart.pdf)
- **Meet Checklist:** [time-drops.com/checklist.pdf](https://time-drops.com/checklist.pdf)
- **Overview Video:** [YouTube](https://youtu.be/O_VuwbtgSNA)
- **YouTube Channel:** [Time Drops Timing](https://www.youtube.com/@TimeDropsTiming)

### SwimTopia Support

For issues with Meet Maestro integration:

- **Business Hours:** (M-F 9am-6pm CST) 877-856-2940 (Option 2)
- **After Hours (Meet Day Emergency):** 877-856-2940 (Option 6)
- **Submit Support Ticket:** Via SwimTopia Help Center
- **Remote Troubleshooting:** Enable in Meet Maestro help menu, recreate issue, include Session ID in ticket

### Meet Maestro Help Resources

Click the **?** icon (top right) in Meet Maestro to access:

- **Help Center** - Topic-organized documentation
- **Submit Support Request**
- **Phone Contact**
- **Remote Support** - Enable to create read-only replay of steps for troubleshooting

## Related Guides

- [Time Drops Timing System](time-drops-about.md) - General system overview
- [Scorekeeper Guide](scorekeeper.md) - Running meets with Meet Maestro
- [Meet Preparation](meet-preparation.md) - Pre-meet checklist for GPSA reps

---

**Source:** Adapted from SwimTopia Help Center documentation for GPSA teams using Time Drops.
