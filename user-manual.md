# TrackMe+ User Guide

Welcome to TrackMe+. This guide covers everything you need to track your medications, lab results, and health data. TrackMe+ is completely free — no subscriptions, no tiers, no upgrade prompts.

---

## Getting Started

### Creating Your Account

1. Go to [trackmeplus.com](https://trackmeplus.com)
2. Click **Sign Up**
3. Enter your name, email, and password (at least 8 characters)
4. Click **Create Account**

You'll be logged in automatically and land on your Today screen.

### Sign In with Apple

On iOS, you can sign in with Apple instead of email/password. Tap **Sign in with Apple** on the login screen and follow the prompts.

### Logging In

1. Go to the login page
2. Enter your email and password
3. Click **Log In**

### Forgot Your Password?

1. On the login page, click **Forgot Password?**
2. Enter your email address
3. Click **Send Reset Link**
4. Check your email for a reset link
5. Click the link and enter your new password

### Desktop vs Mobile

TrackMe+ works on desktop computers and mobile phones.

**Desktop**: Sidebar on the left with all main sections. Click any section to open it.

**Mobile**: Bottom navigation tabs. Tap a tab to switch sections.

Both do the same things.

---

## Today

Today is your home screen. It opens every time you log in. This is your daily dose checklist.

### What You'll See

- Your dose schedule for today
- Check/skip buttons for each dose
- Units column showing draw amount
- Per-med dose details

### Checking Off a Dose

1. Find the dose in your list
2. Click the checkmark icon
3. The dose is marked Completed with a timestamp

### Skipping a Dose

1. Find the dose
2. Click **Skip**
3. Pick a reason: Forgot / Out of stock / Side effects / Doctor advised / Other
4. Add notes if you want (optional)
5. Click **Confirm**

Skipped doses are recorded in your history so your records stay honest.

### Multi-Skip Mode

Need to skip several doses at once?

1. Click **Multi-Skip** at the top
2. Tap each dose you want to skip
3. Click **Skip Selected**
4. Pick your reason and confirm

### Changing the Date

1. Click the date at the top
2. Pick a date from the calendar
3. You'll see doses scheduled for that day

### Logging a Dose Manually

1. Click **Add Dose**
2. Select the medication
3. Pick the date and time
4. Enter how much you took
5. If an injection, pick the injection site
6. Add notes if you want
7. Click **Save**

---

## My Medications

This is where you manage all your medications.

### Adding a New Medication

1. Click **+ Add Medication**
2. Fill out the form
3. Click **Save**

### The Add Medication Form

**Basic Info**:
- **Name**: What you're taking
- **Type**: Vial, Bottle, Pre-mix, or other form
- **Status**: Active or Inactive

**How Much and How Often**:
- **Dose Amount**: How much you take each time
- **Unit**: mg, mcg, ml, IU, units, etc.
- **Frequency**: Daily, Twice Daily, Three Times Daily, Every X Days, Specific Days, or Custom

**Time(s) of Day**:
- Set when you take each dose
- Multiple times for multi-daily dosing

**For Injections**:
- **Injection Site**: Rotation site tracking

**Vial Tracking** (for vials):
- **Vial Number**: Simple increment tracking (Vial 1, Vial 2, etc.)
- **Concentration**: mg/ml for dose calculator
- **Reconstitution Info**: BAC water volume added

**Cycle Tracking** (for compounds taken in on/off cycles):
- Toggle **Is Cycle** on
- **Cycle Duration**: How long you take it (weeks)
- **Washout Duration**: Time off between cycles (weeks)
- **Start Date**: When the current cycle started

The card shows your current position: "Day 45/84" during the cycle, or "Rest Day 10" during washout, or "Ready" when washout is complete.

### Single-Use Depletion Mode

For TRT-style dosing where you draw from one vial over many doses:

- Toggle **Single-Use Depletion** on
- Each logged dose reduces the remaining vial quantity
- The card shows how much is left in the current vial

### Dose Calculator

TrackMe+ has a built-in dose calculator for injectable medications. Access it from any medication detail view.

**Injection tab**: Enter your dose in mg. The calculator shows the draw volume in ml and units.

**Reconstitution tab**: Enter vial mg and BAC water volume. The calculator shows the concentration and units per dose.

**Convert tab**: Convert between units, ml, and mg.

The formula:
```
Units = (Dose mg ÷ (Vial mg ÷ BAC water mL)) × 100
```

Example: 0.5mg dose from a 10mg vial with 2mL BAC water = 10 units.

### Editing a Medication

1. Click on the medication card (or click the three dots → **Edit**)
2. Make your changes
3. Click **Save**

### Archiving vs Deleting

**Archive**: Keeps the medication and all its dose history, removes it from your active list. Use this when you stop a medication.

**Delete**: Removes it completely, including all dose history. Cannot be undone.

To archive: click the three dots on the card → **Archive**.

To restore: filter by Archived → click the three dots → **Restore**.

---

## Dose History

See your full dose log.

- **List view**: All logged doses with date, time, amount
- **Calendar view**: Doses by day, color-coded by completion status
- **Edit a dose**: Click any logged dose to correct the time, amount, or notes
- **Adherence tracking**: See your completion percentage over time

---

## Lab Results

Track blood work, hormone panels, and other test results.

### Adding a Lab Result

1. Click **+ Add Lab Result**
2. Fill out the form:
   - **Test Name**: What was measured (e.g., "Testosterone Total")
   - **Test Date**: When you had the test
   - **Result Value**: The number from your lab report
   - **Unit**: The measurement unit (mg/dL, ng/mL, %, etc.)
   - **Reference Range**: The normal range from your lab report (e.g., "70-100")
   - **Notes**: Any comments (optional)
3. Click **Save**

The app automatically marks it Normal or Abnormal based on the reference range.

### Viewing Lab Results

You'll see a table with all results:
- Date, Test Name, Value, Unit, Reference Range
- Status badge: green = Normal, red = Abnormal

Click a result to see full details.

### Lab Trends

Click **View Trends** to see how a test has changed over time:
- Pick one or more tests to graph
- Choose a date range
- See a line chart with your values over time and the normal range shaded

### Filtering

Use the filter buttons: **All**, **Normal**, **Abnormal**. Search by test name.

### Editing or Deleting

Click the lab result → **Edit** or **Delete**.

---

## Health Data

### Weight Tracking

**Adding a weight entry**:
1. Go to Vitals → Weight
2. Click **+ Add Weight**
3. Enter the date, weight, unit (lbs or kg), and optional notes
4. Click **Save**

**Viewing history**:
- Current weight with recent change indicators
- 7-day and 30-day change
- All-time high/low
- Line chart of your weight over time

### Blood Pressure Tracking

**Adding a BP reading**:
1. Go to Vitals → Blood Pressure
2. Click **+ Add BP Reading**
3. Enter systolic, diastolic, pulse (optional), date/time, and notes
4. Click **Save**

After saving you'll see a classification badge:
- **Normal**: Under 120/80
- **Elevated**: Systolic 120-129
- **High**: Systolic 130-179 or diastolic 80-119
- **Crisis**: Systolic 180+ or diastolic 120+

*This is informational only, not medical advice. Talk to your doctor about your readings.*

**Viewing history**:
- Current reading with classification
- 7-day and 30-day averages
- All-time high/low
- Chart with systolic and diastolic lines, normal range reference

### Apple HealthKit

TrackMe+ can sync with Apple Health on iOS:
- **Weight**: pulls weight entries from Health
- **Blood Pressure**: pulls BP readings from Health

Go to Settings → HealthKit to connect. Once connected, data flows in automatically.

---

## Notifications

### Setting Up Notifications

Go to **Settings → Notifications**:
- **Master toggle**: Enable or disable all notifications
- **Per-medication settings**: Each medication can have its own reminder schedule

### Types

- **Dose reminders**: Notification when a dose is due
- **Missed dose alerts**: Follow-up if you haven't logged a dose

### Per-Medication Config

1. Open a medication
2. Tap Notifications
3. Set reminder time and frequency for that medication specifically

---

## Reports & Data

### Adherence Report

Go to **Reports → Adherence**:
- Expected doses vs. doses actually taken
- Compliance percentage
- Calendar heatmap showing which days you completed your doses
- Selectable date range and which medications to include

### Data Export

Go to **Settings → Export All Data**:
- Downloads a ZIP file with all your data as CSV spreadsheets
- Includes: medications, doses, labs, weight, blood pressure, and cycles
- Opens in Excel, Google Sheets, or any spreadsheet app

Your data is yours. Export anytime.

---

## Settings

### Profile

Update your name and email.

### Display

- **Dark Mode**: Toggle light/dark theme
- **Time Format**: 12-hour or 24-hour
- **Date Format**: US (MM/DD/YYYY), International (DD/MM/YYYY), or ISO (YYYY-MM-DD)
- **Day Start Time**: For night-shift schedules — if your "day" starts at 6am, doses before 6am count as the previous day

### Notifications

Master toggle and notification preferences. (See Notifications section above.)

### Data

**Export All Data**: Download everything as a ZIP/CSV. See Reports & Data section above.

**Delete Account**: Permanently deletes your account and all data. Cannot be undone. Requires confirmation.

### Support TrackMe+

A Ko-fi tip jar link. TrackMe+ is free and always will be. If it's helped you, a tip keeps the lights on. No pressure — it's a dollar on the counter, not a busker at the door.

### What's New

Changelog with recent updates. An indicator dot appears when new updates are available.

### Help & Support

- Contact support via **Support → Report an Issue**
- Or email [support@trackmeplus.com](mailto:support@trackmeplus.com)

### Legal

- Privacy Policy
- Terms of Service
- Medical Disclaimer

---

## Troubleshooting

### Can't Log In / Forgot Password

1. Click **Forgot Password?** on the login page
2. Enter your email
3. Check your email (including spam) for a reset link
4. Click the link and set a new password

If the email doesn't arrive: wait 5 minutes, check spam, make sure you entered the right email, then try again.

### Doses Not Showing on Today

Check these things:

1. **Is the medication Active?** Go to My Medications and confirm the status badge says "Active"
2. **Is the frequency correct?** Open the medication and verify the schedule
3. **Are you on the right date?** Check the date picker at the top of Today
4. **Is the start date in the past?** Doses only show from the start date forward
5. **Is the cycle in washout?** If cycle tracking is on, the medication may be in its off period

### Data Not Syncing Between Desktop and Mobile

1. Refresh the page (Ctrl+R on desktop, pull down on mobile)
2. Make sure you're logged into the same account on both devices
3. Check your internet connection
4. Log out and back in

### How to Contact Support

- **In-app**: Settings → Support → Report an Issue
- **Email**: [support@trackmeplus.com](mailto:support@trackmeplus.com)

---

## Tips & Best Practices

| Tip | Why |
|:----|:----|
| Start with one medication | Get comfortable logging for a few days before adding everything |
| Use Today every day | Takes 30 seconds and builds a complete history over time |
| Archive, don't delete | Deleting removes your dose history. Archiving keeps it safe |
| Skip doses instead of ignoring them | Your records stay honest — you can see patterns in why you miss |
| Use the dose calculator | Takes the math out of reconstituting vials |
| Export your data before doctor visits | A CSV of your labs and doses is more useful than memory |

---

## Frequently Asked Questions

**Q: Is TrackMe+ really free?**  
A: Yes. Completely free. Every feature, every user. No tiers, no trial limits, no upgrade prompts. There's a Ko-fi tip jar in Settings if you want to support the app.

**Q: Is my data private?**  
A: Yes. Your data is encrypted and only you can access it. We never share it with third parties. See the Privacy Policy for details.

**Q: Can I export my data?**  
A: Yes. Go to Settings → Export All Data for a ZIP file with all your data in CSV format.

**Q: Is there an iOS or Android app?**  
A: iOS native app is coming soon. For now, the full web app works great on mobile at trackmeplus.com. Add it to your home screen for an app-like experience (see below).

**Q: What's the difference between Archive and Delete?**  
A: Archive keeps the medication and all dose history but hides it from your active list. Delete removes everything permanently. Archive is almost always the right choice.

**Q: Can I use this offline?**  
A: On mobile you can view data that's already loaded, but you need internet to add or sync data.

**Q: Does TrackMe+ give medical advice?**  
A: No. TrackMe+ is a tracking tool, not a medical device. It doesn't check drug interactions, recommend dosages, or provide medical guidance. Always work with your healthcare provider.

---

## Installing on Mobile

**iPhone (Safari)**:
1. Open trackmeplus.com in Safari
2. Tap the Share button (square with arrow)
3. Tap **Add to Home Screen**
4. Tap **Add**

**Android (Chrome)**:
1. Open trackmeplus.com in Chrome
2. Tap the three dots menu
3. Tap **Add to Home screen**

You'll have a TrackMe+ icon on your home screen that opens like a native app.

---

**Welcome to TrackMe+. We hope it makes your health tracking easier.**

*Updated: April 2026 | v3.2.0*
