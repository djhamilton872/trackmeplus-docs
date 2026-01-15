# TrackMe+ User Manual

**Version:** 2.52.3
**URL:** https://trackmeplus.com

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Dashboard](#dashboard)
3. [Compounds](#compounds)
4. [Doses](#doses)
5. [Weight Tracking](#weight-tracking)
6. [Lab Results](#lab-results)
7. [Budget](#budget)
8. [Vendors](#vendors)
9. [Supplies](#supplies)
10. [Settings](#settings)
11. [Subscription Plans](#subscription-plans)
12. [Features Reference](#features-reference)

---

## Getting Started

### Creating an Account

1. Navigate to https://trackmeplus.com
2. Click **Sign Up** on the login screen
3. Enter your name, email address, and password
4. Click **Create Account**
5. You'll be automatically logged in to your new account

### Logging In

1. Enter your email address
2. Enter your password
3. Click **Log In**

### Password Reset

If you forget your password:
1. Click **Forgot Password** on the login screen
2. Enter your email address
3. Check your email for a reset link
4. Follow the link to create a new password

---

## AI Smart Lookup (New in v2.42+)

TrackMe+ includes intelligent auto-complete that helps you enter compound and vendor names accurately.

### How It Works

When adding a new compound:

1. **Compound Name Field** - Start typing and suggestions appear
   - Suggestions come from our master database of 47+ compounds
   - Shows match confidence (e.g., "95% match")
   - Displays category (GLP-1, Peptide, Hormone, etc.)
   - Click a suggestion to auto-fill

2. **Vendor Name Field** - Start typing and vendor suggestions appear
   - Suggestions from our verified vendor database
   - Shows vendor category (Pharmacy, Domestic Supplier, etc.)
   - **Auto-fills website** - When you select a vendor, the website field is automatically populated

### AI Suggestions Badge

Look for the "+ AI Suggestions" indicator below input fields. This shows the smart lookup is active and ready to help.

### Tips

- Type at least 2 characters to trigger suggestions
- Common abbreviations work (e.g., "BPC" finds "BPC-157")
- Misspellings are often corrected (e.g., "tirzepatid" finds "Tirzepatide")
- You can still type custom names if the suggestion doesn't match

---

## Dashboard

The Dashboard is your home screen, providing an overview of your peptide tracking activity.

[screenshot placeholder: Dashboard overview]

### What You'll See

- **Welcome Message** - Personalized greeting with your name
- **Stats Cards** - Quick metrics including:
  - Total Compounds
  - Total Doses Logged
  - This Week's Doses
  - Total Spent on Compounds
- **Today's Schedule** - Your doses scheduled for today
- **Usage Widget** - Shows your plan limits (compounds, lab results)
- **Dose Timer** - Timer for spacing doses
- **Recent Activity** - Your 5 most recent completed doses

### Today's Schedule Widget

The schedule shows all doses due today based on your compound settings:

- **Time** - When the dose is scheduled
- **Compound** - Name of the peptide
- **Type** - Shows both form and route, e.g., "Vial (Injection)", "Drops (Sublingual)", "Pills (Oral)"
- **Units** - Calculated injection units (for vials)
- **Dose** - Amount and unit (e.g., "5 mg")
- **Done** - Checkbox to mark as complete (separate checkbox for each scheduled dose time)

**Multi-Dose Support:**
If a compound is scheduled multiple times per day, each dose time gets its own checkbox. For example, a compound taken twice daily at 8 AM and 8 PM will show two separate rows, each with its own Done checkbox.

**Future Dates:**
- You can view future dates using the date picker
- Future doses are shown but cannot be marked complete until that day arrives
- Compounds with future start dates show "starts in X days"

**Actions:**
- Click the **date picker** to view other days
- Click **Print** to print the schedule
- Click **Email** to send the schedule to yourself

---

## Compounds

Manage all your peptide compounds in one place.

[screenshot placeholder: Compounds list view]

### Adding a Compound

1. Click **Add Compound**

**Smart Auto-Complete:**
As you type the compound name, suggestions will appear from our database. Select a suggestion to ensure consistent naming and get helpful defaults like typical dosing ranges. The same applies to the Vendor Name field - select a vendor to auto-fill their website.

2. Fill in the required fields:
   - **Name** - e.g., "Semaglutide"
   - **Form** - Vial (Injectable), Drops, Pills, Patches, Powder, or Cream
   - **Status** - Active, On Hold, or Completed
   - **Dose Amount** - e.g., "5"
   - **Dose Unit** - mg, mcg, or mL
   - **Frequency** - Daily, Twice Daily, Weekly, etc.
   - **Time of Day** - When to take it (supports multiple times)

3. Optional fields:
   - **Quantity** - Vial size (e.g., "10 mg")
   - **Reconstitution** - mL of BAC water added (for lyophilized peptides)
   - **Concentration** - For drops (e.g., "20mg/mL")
   - **Start Date** - When you began (or will begin) the compound
   - **Cycle Duration** - For cycling compounds
   - **Vendor** - Where you purchased it
   - **Cost** - Price paid
   - **Vials on Hand** - How many vials you have
   - **Notes** - Any additional information

4. Click **Save Compound**

### Compound Types (Forms)

| Form | Route | Description | Unit Calculation |
|------|-------|-------------|------------------|
| **Vial (Injectable)** | Injection | Lyophilized or pre-mixed injectable | See below |
| **Drops** | Sublingual | Liquid drops under tongue | (dose_mg / concentration_mg_ml) × 20 = drops |
| **Pills** | Oral | Tablets or capsules | N/A |
| **Patches** | Transdermal | Skin patches | N/A |
| **Powder** | Varies | Raw powder | N/A |
| **Cream** | Topical | Topical cream | N/A |

### Compound Status

Each compound has a status that controls whether it appears on your dosing schedule:

| Status | Badge Color | On Schedule? | Use When |
|--------|-------------|--------------|----------|
| **Active** | Green | Yes | Currently taking this compound |
| **On Hold** | Orange | No | Have it, waiting to start |
| **Completed** | Gray | No | Finished with this compound |

**On Hold** is perfect for compounds you've purchased but aren't ready to start yet - for example, if you're waiting to finish your current supply of a similar compound first.

To change status:
1. Go to **Compounds**
2. Click **Edit** on the compound
3. Select the new status from the dropdown
4. Click **Save**

You can filter the compound list by status using the filter buttons at the top of the Compounds page.

### Pre-Mixed (Oil-Based) Vials

For pre-constituted injectable compounds like Testosterone Cypionate, Deca, or other oil-based medications:

1. Select **Vial (Injectable)** as the Form
2. Check the **Pre-mixed (oil-based, like Testosterone)** checkbox
3. Enter the **Concentration (mg/mL)** - e.g., 200 for 200mg/mL Testosterone
4. Enter the **Vial Size (mL)** - e.g., 1 for a 1mL vial, 10 for a 10mL vial
5. Set your **Dose Amount** in mL - e.g., 0.6 mL weekly

The app will correctly calculate your doses and days supply based on the vial size and your dosing schedule.

### Compound Grouping (Variants)

When you have multiple vials of the same compound from different vendors or in different sizes, you can group them together:

**When to Use:**
- Multiple vials of BPC-157 from different vendors
- Same peptide in different sizes (5mg vs 10mg vials)
- Tracking which vial you're currently using

**How to Enable:**
1. When adding/editing a compound, you'll see a **Compound Group** field
2. Enter the base compound name (e.g., "BPC-157")
3. Compounds with the same group name are displayed together

**Setting the Active Vial:**
1. Click on a grouped compound card to expand it
2. Click **Set Active** on the vial you're currently using
3. Only the active vial appears on your dosing schedule

**Group Benefits:**
- See total inventory across all variants
- Low stock alerts based on total group inventory
- Easy switching between vials when one runs out

### Future Start Dates

You can set a start date in the future for compounds you haven't started yet:

1. Enter a future date in the **Start Date** field
2. The compound will show "starts in X days" on the dashboard
3. The compound will NOT appear on the schedule until the start date arrives
4. Once the start date arrives, doses automatically appear on your schedule

### Inventory Display

Each compound card shows:
- **Doses remaining** - Approximate number of doses left (e.g., "~20 doses")
- **Days supply** - How many days until you run out (e.g., "~140 days")

Both values are displayed: "~20 doses / ~140 days"

### Frequency Options

- **Daily** - Once per day
- **Twice Daily** - Two times per day
- **Three Times Daily** - Three times per day
- **Every Other Day** - Alternating days
- **Every X Days** - Custom interval (e.g., every 3 days)
- **Weekly** - Once per week
- **Custom Days** - Select specific days of the week

### Editing a Compound

1. Find the compound in the list
2. Click the **Edit** button
3. Make your changes
4. Click **Save Compound**

### Deleting a Compound

1. Click the **Delete** button
2. Confirm the deletion

---

## Doses

Log and track all your dose administrations.

[screenshot placeholder: Doses view]

### Logging a Dose

**From Today's Schedule:**
1. Check the **Done** checkbox next to any scheduled dose
2. The dose is automatically logged with the current time

**Multi-Dose Per Day:**
If a compound is scheduled multiple times per day (e.g., Twice Daily at 8 AM and 8 PM), each dose time appears as a separate row with its own checkbox. This allows you to:
- Mark each dose individually as complete
- Track exactly which doses you've taken
- See "Dose 1", "Dose 2", etc. for count-based matching

**From the Doses Tab:**
1. Click **Add Dose**
2. Select the **Compound**
3. Enter the **Date** and **Time**
4. Enter the **Dose Amount** and **Unit**
5. Optionally add:
   - **Injection Site** - Where you administered it
   - **Notes** - Any observations
6. Click **Save Dose**

### Future Dates

- You can view future dates on the schedule using the date picker
- Future doses are displayed but **cannot be marked complete** until that day arrives
- This prevents accidentally logging doses ahead of time

### Viewing Dose History

The Doses tab shows all logged doses organized by time period:
- Morning (6 AM - 12 PM)
- Afternoon (12 PM - 5 PM)
- Evening (5 PM - 9 PM)
- Night (9 PM - 6 AM)

### Dose Timer

Use the dose timer to space your peptide doses properly:

1. Click a preset time (5, 10, 15, or 30 minutes)
2. Or enter a custom time (1-120 minutes)
3. The timer counts down
4. You'll receive a notification when complete (if enabled)

**Timer Features:**
- Pause/Resume capability
- Persists across page refreshes
- Audio alert when complete
- Browser notification (if permitted)

### Exporting Doses

1. Click **Export** in the Doses view
2. Choose your format:
   - **PDF** - Formatted report
   - **CSV** - Spreadsheet format
3. Select date range
4. Download the file

---

## Weight Tracking

Track your weight over time to monitor the effects of your peptide therapy.

[screenshot placeholder: Weight tracking view]

### Accessing Weight Tracking

Click **Weight** in the sidebar navigation to access the weight tracking feature.

### Logging Weight

1. Click **Log Weight**
2. Enter the **Date** (defaults to today)
3. Enter your **Weight**
4. Select the **Unit** (lbs or kg)
5. Optionally add **Notes** (e.g., "After breakfast", "Morning weigh-in")
6. Click **Save**

Your preferred unit (lbs or kg) is remembered for future entries.

### Stats Cards

The weight tracking page displays four summary cards:

| Card | Description |
|------|-------------|
| **Current** | Your most recent weight entry (with unit) |
| **Change** | Difference from your starting weight (green = loss, red = gain) |
| **Lowest** | Your lowest recorded weight |
| **Highest** | Your highest recorded weight |

### Weight Trend Chart

When you have 2 or more entries, a line chart displays your weight trend:
- Shows the last 30 entries
- X-axis: Date range
- Y-axis: Weight values
- Points are connected to show the trend
- Hover over points to see exact values

### Weight History Table

All your weight entries are displayed in a table showing:
- **Date** - When the weight was recorded
- **Weight** - Value and unit (e.g., "185.5 lbs")
- **Notes** - Any notes you added
- **Actions** - Edit or Delete buttons

### Editing a Weight Entry

1. Find the entry in the history table
2. Click the **Edit** button
3. Make your changes
4. Click **Update**

### Deleting a Weight Entry

1. Find the entry in the history table
2. Click the **Delete** button
3. Confirm the deletion

### One Entry Per Day

The system allows one weight entry per day. If you log weight for a date that already has an entry, the existing entry is updated with the new value.

---

## Lab Results

Track your lab tests, monitor biomarkers, and visualize trends over time.

### Views

The Lab Results page has two views, toggled by the **Results** and **Trends** buttons:

| View | Description |
|------|-------------|
| **Results** | Table of all lab results with filters |
| **Trends** | Line chart showing test values over time |

### Adding Lab Results Manually

1. Click **Add Lab Result**
2. Enter the **Test Date**
3. Enter the **Test Name** (e.g., "IGF-1", "A1C", "Testosterone")
4. Enter the **Result Value**
5. Enter the **Unit** (e.g., "ng/mL", "%")
6. Optionally add:
   - **Reference Range** - Normal range for comparison (e.g., "0-100")
   - **Lab Name** - Where the test was performed
   - **Notes** - Observations or context
7. Click **Save Lab Result**

### Import from Screenshot (Premium)

Don't want to type in all your lab results by hand? Just take a photo! Premium members can snap a picture of their lab results and the app will read them automatically.

**How to Use:**
1. Click the purple **Import from Screenshot** button
2. Take a photo of your lab results (or use a screenshot from your patient portal)
3. Upload the photo
4. Wait a few seconds while the app reads your results
5. Check that everything looks right in the preview
6. Click **Import** to save

**Tips for Good Photos:**
- Make sure the text is clear and readable (not blurry)
- Get the whole results table in the photo
- Good lighting helps!
- Photos from your phone work great

**What the App Can Read:**
- Test names (like "Testosterone", "A1C", "Cholesterol")
- Your result numbers
- The normal range (if it's shown on your report)

**Limits:**
- Premium members get 10 photo imports per month
- Your count resets on the 1st of each month

### Status Filters

Filter your lab results by status using the buttons at the top:

| Filter | Color | Description |
|--------|-------|-------------|
| **All** | Blue | Shows all results |
| **Normal** | Gray | Results within reference range |
| **Flagged** | Gray | User-flagged results (coming soon) |
| **Abnormal** | Gray | Results outside reference range |

The count badge on each button shows how many results match that filter.

**How Status is Determined:**
- Results with reference ranges are automatically categorized
- Values within range = Normal
- Values outside range = Abnormal
- Results without reference ranges are not categorized

### Lab Trend Charts

Visualize how your test results change over time.

**Accessing Trends:**
1. Click the **Trends** button (chart icon) in the Lab Results view
2. Select a test from the dropdown menu
3. View the line chart showing your values over time

**Chart Features:**
- **Line graph** with data points for each result
- **Reference range** displayed above the chart (e.g., "Reference Range: 0 - 100")
- **Date axis** showing the time period covered
- **Stats panel** showing:
  - Latest value
  - Minimum value
  - Maximum value
  - Number of data points

**Tips:**
- You need at least 2 results for a test to see a trend
- Tests are sorted alphabetically in the dropdown
- The chart auto-scales to fit your data range

### Lab Result Limits by Plan

| Plan | Annual Lab Results | OCR Imports |
|------|-------------------|-------------|
| Free | 10 per year | Not available |
| Standard | 50 per year | Not available |
| Premium | Unlimited | 10 per month |

---

## Budget

Track spending on your peptide therapy.

[screenshot placeholder: Budget view]

### Adding Budget Entries

1. Click **Add Budget Entry**
2. Select the **Category**:
   - Compounds
   - Supplies
   - Lab Tests
   - Consultations
   - Shipping
   - Other
3. Enter the **Amount Spent**
4. Enter the **Date**
5. Add optional **Description**
6. Click **Save Entry**

### Budget Overview

- **Total Spent** - Sum of all budget entries
- **By Category** - Breakdown of spending
- **Monthly Trend** - Spending over time

### Import from Receipt (Premium)

Tired of typing in every purchase? Just snap a photo of your receipt!

**How to Use:**
1. Go to the **Budget** page
2. Click the purple **Import Receipt** button (top right)
3. Take a photo of your receipt, invoice, or order confirmation
4. Click **Extract Purchases**
5. Wait a few seconds while the app reads your receipt
6. Check that everything looks right
7. Click **Import** to save

**What the App Can Read:**
- Peptides and compounds you purchased
- Medical supplies (syringes, BAC water, etc.)
- Shipping costs
- Lab test fees
- Pretty much anything on a receipt!

**Tips for Good Photos:**
- Make sure the text is clear and readable
- Get the whole receipt in the photo
- Good lighting helps!
- Screenshots from email order confirmations work great

**Limits:**
- Premium members get 10 receipt imports per month
- Your count resets on the 1st of each month

### Duplicate Protection

Don't worry about accidentally importing the same receipt twice! The app automatically checks for duplicates.

**How it works:**
An item is considered a duplicate if ALL THREE of these match:
- Same store/vendor name
- Same exact dollar amount
- Same date on the receipt

**What happens:**
- If you try to import something that's already in your records, it gets skipped automatically
- You'll see a message telling you which items were skipped
- New items from the same receipt still get imported normally

**Example:** Let's say you imported an Amazon order last week. If you accidentally try to import it again, the app will say "Already imported" and skip those items. No duplicates!

**When you CAN import the same item:**
- You bought it on a different date
- The price was different
- You bought it from a different store
- You deleted the original entry (you can re-import it)

---

## Vendors

Manage your peptide suppliers.

[screenshot placeholder: Vendors view]

### Adding a Vendor

1. Click **Add Vendor**
2. Enter vendor details:
   - **Name** (required)
   - **Website URL**
   - **Email**
   - **Phone**
   - **Notes**
3. Click **Save Vendor**

### Vendor Information

Store important details about each supplier:
- Contact information
- Website links
- Notes about quality, shipping times, etc.

### Vendor Auto-Fill

When adding a compound, typing in the Vendor Name field shows suggestions from our verified vendor database. Selecting a vendor automatically populates:
- Vendor Name (standardized spelling)
- Vendor Website (if available in our database)

This saves time and ensures you have accurate vendor contact information.

---

## Supplies

Track your peptide-related supplies and inventory.

[screenshot placeholder: Supplies view]

### Adding Supplies

1. Click **Add Supply**
2. Enter supply details:
   - **Name** - e.g., "Insulin Syringes"
   - **Category** - Syringes, Needles, BAC Water, etc.
   - **Quantity** - How many you have
   - **Cost** - Price paid
   - **Expiration Date** - When it expires
   - **Notes** - Additional info
3. Click **Save Supply**

### Supply Categories

- Syringes
- Needles
- BAC Water
- Alcohol Swabs
- Sharps Container
- Storage (vials, containers)
- Other

### Import Supplies from Receipt (Premium)

You can also import supplies directly from receipts! This works the same way as the Budget import - just take a photo and the app reads it for you.

The app automatically knows the difference between peptides and supplies, so everything gets sorted into the right place.

**How to Use:**
1. Click the purple **Import from Screenshot** button
2. Take a photo of your receipt, invoice, or Amazon order
3. Upload the photo
4. Wait a few seconds while the app reads your items
5. Check that everything looks right
6. Click **Import** to save

**What the App Can Read:**
- Product names (syringes, needles, BAC water, etc.)
- Quantities
- Prices
- Vendor/seller name (when shown)

**Tips:**
- Amazon order confirmations work great
- Pharmacy receipts work too
- Make sure the text is readable
- Don't worry about duplicates - the app checks automatically!

**Limits:**
- Premium members get 10 photo imports per month
- This shares the same limit as Budget imports

---

## Settings

Customize your TrackMe+ experience.

[screenshot placeholder: Settings view]

### Profile Tab

**Account Information:**
- Edit your **Name**
- Edit your **Email**

### Display Tab

**Display Preferences:**
- **Dark Mode** - Toggle dark/light theme
- **Time Format** - 12-hour (2:30 PM) or 24-hour (14:30)
- **Date Format** - MM/DD/YYYY, DD/MM/YYYY, or YYYY-MM-DD
- **Day Start Time** - Define when your "day" begins (useful for night shift)
- **Default View** - Which page to show on login

### Notifications Tab

**Notification Settings:**
- **Email Notifications** - Receive email alerts
- **Dose Reminders** - Get reminded about scheduled doses
- **Low Supply Alerts** - Warning when supplies run low

### Data Tab

**Data Management:**
- **Data Retention** - How long to keep historical data
- **Export Data** - Download all your data
- **Delete Account** - Permanently remove your account

### Billing Tab

**Subscription Management:**
- View current plan and status
- See usage statistics (compounds used, lab results used)
- Upgrade or downgrade plan
- Switch between Monthly and Annual billing
- Cancel subscription
- Reactivate a cancelled subscription (before it expires)

**Subscription Status:**
| Status | Description |
|--------|-------------|
| **Active** | Your subscription is current and active |
| **Cancelling** | Cancelled but still active until period ends |
| **Expired** | Subscription has ended |

**Cancelling Your Subscription:**
1. Go to **Settings** > **Billing**
2. Click the **Cancel Subscription** button
3. Confirm the cancellation
4. Your subscription remains active until the end of your billing period
5. Status changes to "Cancelling" with the expiration date shown

**Reactivating a Cancelled Subscription:**
If you cancelled but changed your mind:
1. Go to **Settings** > **Billing**
2. You'll see a **Reactivate Subscription** button (only visible if cancelled but not yet expired)
3. Click **Reactivate**
4. Your subscription continues without interruption

**Annual vs Monthly Billing:**
When upgrading, you can choose between:
- **Monthly** - Pay monthly, cancel anytime
- **Annual** - Pay yearly, save ~17% compared to monthly

To switch billing cycles:
1. Go to **Settings** > **Billing**
2. Click **Upgrade**
3. Toggle between Monthly/Annual using the billing toggle
4. Select your plan and complete checkout

---

## Subscription Plans

### Free Plan - $0/month

- Up to **3 compounds**
- Up to **10 lab results per year**
- Basic features
- Email support

### Standard Plan - $9.99/month or $99.99/year

- **Unlimited compounds**
- Up to **50 lab results per year**
- All Free features
- Priority support
- Data export

### Premium Plan - $19.99/month or $199.99/year

- **Unlimited compounds**
- **Unlimited lab results**
- All Standard features
- **AI-Powered OCR** - Import labs and receipts from photos
- Advanced analytics
- Phone support

### Annual Savings

Save ~17% by choosing annual billing:
| Plan | Monthly | Annual | Savings |
|------|---------|--------|---------|
| Standard | $9.99/mo | $99.99/yr | $19.89/yr |
| Premium | $19.99/mo | $199.99/yr | $39.89/yr |

### Upgrading Your Plan

1. Go to **Settings** > **Billing**
2. Click **Upgrade**
3. Choose **Monthly** or **Annual** billing
4. Select your new plan
5. Enter payment information
6. Confirm the upgrade

---

## Mobile App (PWA)

TrackMe+ works great on your phone as a Progressive Web App (PWA). Install it for a native app-like experience.

### Installing on iPhone/iPad

1. Open Safari and go to https://trackmeplus.com
2. Log in to your account
3. Tap the **Share** button (square with arrow)
4. Scroll down and tap **Add to Home Screen**
5. Name it "TrackMe+" and tap **Add**
6. The app icon appears on your home screen

### Installing on Android

1. Open Chrome and go to https://trackmeplus.com
2. Log in to your account
3. Tap the **three dots** menu (top right)
4. Tap **Add to Home screen** or **Install app**
5. Name it "TrackMe+" and tap **Add**
6. The app icon appears on your home screen

### Mobile Features

| Feature | Description |
|---------|-------------|
| **Dose Timer** | Timer with presets (5, 10, 15, 30 min) |
| **Quick Logging** | Mark doses complete with one tap |
| **Inventory** | Check supply levels on the go |
| **Streak Tracking** | See your dosing consistency |
| **Notifications** | Get dose reminders (when enabled) |

### Offline Capability

The PWA works offline for viewing your schedule and compound info. Changes sync when you reconnect to the internet

---

## Features Reference

### AI-Powered Features

| Feature | Description | Available In |
|---------|-------------|--------------|
| Smart Compound Lookup | Auto-complete with 47+ compounds | All Plans |
| Smart Vendor Lookup | Auto-complete with verified vendors | All Plans |
| Vendor Website Auto-Fill | Auto-populates website when vendor selected | All Plans |

### Dose Timer

The dose timer helps you properly space peptide doses:

- **Preset Times:** 5, 10, 15, or 30 minutes
- **Custom Time:** Enter any value from 1-120 minutes
- **Controls:** Start, Pause, Resume, Reset
- **Alerts:** Audio beep and browser notification
- **Persistence:** Timer continues even if you navigate away

### Unit Calculations

**For Injectable Vials:**
```
Units = (Dose in mg / (Vial total mg / Reconstitution mL)) × 100
```

Example: 0.5mg dose from 10mg vial with 2mL BAC water
= (0.5 / (10 / 2)) × 100 = 10 units

**For Drops:**
```
Drops = (Dose in mg / Concentration mg/mL) × 20
```

Example: 5mg dose from 20mg/mL solution
= (5 / 20) × 20 = 5 drops

### Schedule Email

Email your daily schedule:
1. Click **Email** on the schedule
2. Enter recipient email address
3. Schedule is sent as a formatted email

### Print Schedule

Print your daily schedule:
1. Click **Print** on the schedule
2. Use your browser's print dialog
3. Schedule prints in a clean format

### CSV Export

Export your data to spreadsheet:
1. Navigate to the relevant section (Doses, Labs, etc.)
2. Click **Export** or **Download CSV**
3. Open in Excel, Google Sheets, or any spreadsheet app

### PDF Export

Generate formatted PDF reports:
1. Navigate to Doses view
2. Click **Export PDF**
3. Select date range
4. Download the formatted report

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Enter` | Save/Submit forms |
| `Escape` | Close modals |

---

## Troubleshooting

### Schedule Not Showing Doses

- Verify compound **Status** is "Active"
- Check the **Frequency** settings
- Confirm **Start Date** is on or before today
- For custom days, verify the current day is selected

### Timer Notification Not Working

1. Click the 🔔 button to enable notifications
2. Allow notifications when prompted by browser
3. Ensure browser notifications are not blocked system-wide

### Data Not Syncing

1. Check your internet connection
2. Refresh the page
3. Log out and log back in
4. Clear browser cache if issues persist

---

## Support

For help with TrackMe+:

- **Email:** support@hamiltonsweb.com
- **Documentation:** This manual
- **Billing Issues:** Settings > Billing

---

*Last updated: January 2026*
*Version: 2.52.3*
