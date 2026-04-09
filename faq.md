---
layout: default
title: FAQ
nav_order: 4
---

# Frequently Asked Questions
{: .fs-9 }

Common questions about TrackMe+
{: .fs-6 .fw-300 }

---

## General

<details open markdown="block">
<summary>What is TrackMe+?</summary>

TrackMe+ is a free web application for tracking medications, peptides, supplements, and related health data. It helps you manage dosing schedules, calculate injection units, log doses, track lab results, and monitor your health data over time.
</details>

<details markdown="block">
<summary>Is my data secure?</summary>

Yes. Your data is stored securely with encryption. We never share your personal health information with third parties. See our [Privacy Policy]({% link privacy-policy.md %}) for details.
</details>

<details markdown="block">
<summary>Can I use this on my phone?</summary>

Yes! TrackMe+ has a dedicated mobile experience that works on smartphones and tablets. Visit [trackmeplus.com](https://trackmeplus.com) in your mobile browser, or install it as a Progressive Web App for an app-like experience. See the [Mobile PWA Install](#mobile-pwa) section below.
</details>

<details markdown="block">
<summary>Is there a dark mode?</summary>

Yes. Go to **Settings → Display** and toggle Dark Mode. It applies across the entire app, including the mobile version.
</details>

<details markdown="block">
<summary>How much does TrackMe+ cost?</summary>

TrackMe+ is completely free. No subscription, no tiers, no credit card required. Sign up and get access to everything.
</details>

---

## Medications & Doses

<details markdown="block">
<summary>How do I calculate injection units?</summary>

TrackMe+ calculates units automatically when you set up a vial medication. The formula is:

```
Units = (Dose mg ÷ (Vial mg ÷ BAC water mL)) × 100
```

**Example:** 0.5mg dose from a 10mg vial with 2mL BAC water = 10 units
</details>

<details markdown="block">
<summary>What's the difference between medication types?</summary>

| Type | Use For | Unit Calculation |
|:-----|:--------|:-----------------|
| Vial | Injectable medications | Syringe units |
| Drops | Sublingual liquids | Number of drops |
| Pills | Tablets/capsules | N/A |
</details>

<details markdown="block">
<summary>How do I track multiple time doses?</summary>

When setting up a medication, you can add multiple "Time of Day" entries. Each will appear separately in your daily schedule on the Today page.
</details>

<details markdown="block">
<summary>How do I skip a dose?</summary>

On the **Today** page, click the **Skip** button next to any scheduled dose. You can enter an optional reason (e.g., "traveling", "ran out"). Skipped doses show up in your history so you have a complete, honest record.
</details>

<details markdown="block">
<summary>Can I skip multiple doses at once?</summary>

Yes. Use **Multi-Skip** mode on the Today page to select several doses and skip them all at once with a single reason. Handy for travel days or when you're taking a break from a protocol.
</details>

<details markdown="block">
<summary>How does cycle tracking work?</summary>

When editing a medication, turn on **Is Cycle** and set your cycle length and washout period. The app will track exactly where you are in the cycle — "Day 45 of 84", "Rest Day 10", or "Ready to Start" — and automatically pause doses during washout periods.
</details>

---

## Data & Export

<details markdown="block">
<summary>Can I export my data?</summary>

Yes. Go to **Settings → Export All Data** to download a ZIP file containing all your medications, doses, lab results, and other data in a portable format. Your data is yours.
</details>

<details markdown="block">
<summary>Does TrackMe+ sync with Apple Health?</summary>

Yes. On iOS, TrackMe+ can write dose events to Apple Health. Enable it in **Settings → Integrations → Apple Health**.
</details>

---

## Mobile PWA
{: #mobile-pwa }

<details markdown="block">
<summary>How do I install TrackMe+ on my iPhone?</summary>

1. Open **Safari** and go to [trackmeplus.com](https://trackmeplus.com)
2. Log in to your account
3. Tap the **Share** button (square with upward arrow)
4. Scroll down and tap **Add to Home Screen**
5. Tap **Add**

You'll now have a TrackMe+ icon on your home screen that opens like a native app.
</details>

<details markdown="block">
<summary>How do I install TrackMe+ on Android?</summary>

1. Open **Chrome** and go to [trackmeplus.com](https://trackmeplus.com)
2. Log in to your account
3. Tap the **three dots** menu (top right)
4. Tap **Add to Home screen**

You'll now have a TrackMe+ icon on your home screen.
</details>

<details markdown="block">
<summary>Is there a native iOS or Android app?</summary>

A native iOS app is in development. In the meantime, the mobile PWA provides a full-featured experience with an app-like interface. See the install instructions above.
</details>

---

## Troubleshooting

<details markdown="block">
<summary>Why isn't my scheduled dose showing on Today?</summary>

If a medication isn't appearing on your Today dosing schedule, check these common causes:

1. **Quantity on Hand is 0** — This is the most common reason. If you've used all your supply, the medication won't show on your dosing schedule. Go to **Medications**, find the medication (it will show a red "Critical" badge), tap **Edit**, and update your inventory with your new supply. Your doses will reappear immediately.
2. **Status is not "Active"** — Only active medications show on Today. Check that Status is set to "Active" in the medication settings.
3. **Frequency doesn't match today** — For weekly or custom-day medications, make sure today is one of your scheduled days.
4. **Start Date is in the future** — Doses won't appear until the start date arrives.
5. **Cycle is in washout** — If you use cycle tracking, your medication may be in an OFF/washout period.
</details>

<details markdown="block">
<summary>How do I contact support?</summary>

Two ways:
1. **In-app:** Settings → Support → Report an Issue
2. **Email:** [support@trackmeplus.com](mailto:support@trackmeplus.com)
</details>

---

## Still Have Questions?

[Contact Support](mailto:support@trackmeplus.com){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Back to Home]({% link index.md %}){: .btn .fs-5 .mb-4 .mb-md-0 }

---

*Updated: April 2026 | v1.0*
