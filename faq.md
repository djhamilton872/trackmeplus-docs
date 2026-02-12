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

TrackMe+ is a web application for tracking medications, peptides, supplements, and related health data. It helps you manage dosing schedules, calculate injection units, log doses, track lab results, and monitor your health data over time.
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
<summary>How does the dose timer work?</summary>

The timer helps you space peptide doses properly. Select a preset time (5-30 minutes) or enter a custom duration. The timer:
- Continues even if you navigate away
- Persists if you close and reopen your browser
- Plays an audio alert when complete
- Shows a browser notification (if enabled)
</details>

---

## Plans & Billing

<details markdown="block">
<summary>What plans are available?</summary>

| Plan | Price | Highlights |
|:-----|:------|:-----------|
| **Free** | $0/month | Up to 3 medications, 10 lab results/year |
| **Standard** | $6.99/month | Unlimited medications, full lab tracking, budget tools |
| **Premium** | $14.99/month | Everything in Standard plus AI features, priority support |
| **Family** | $19.99/month | Premium features for up to 5 family members |

</details>

<details markdown="block">
<summary>What's included in the free plan?</summary>

- Up to 3 medications
- 10 lab results per year
- Basic dashboard
- Email support
</details>

<details markdown="block">
<summary>How do I upgrade my plan?</summary>

Go to **Settings → Billing** and click the **Upgrade** button for your desired plan. Payments are handled securely through Stripe.
</details>

<details markdown="block">
<summary>Can I cancel anytime?</summary>

Yes. Go to **Settings → Billing** and click **Cancel Subscription**. You'll retain access to your paid features until the end of your current billing period.
</details>

<details markdown="block">
<summary>What's the Family plan?</summary>

The Family plan ($19.99/month) gives you all Premium features for up to 5 family members under one subscription. Each family member gets their own private account and data.
</details>

---

## Data & Export

<details markdown="block">
<summary>Can I export my data?</summary>

Yes. Go to **Settings → Export All Data** to download a ZIP file containing all your medications, doses, lab results, and other data in a portable format. Your data is yours.
</details>

<details markdown="block">
<summary>How does receipt scanning work?</summary>

On the Budget page, click **Scan Receipt**. Take or upload a photo of a receipt or invoice, and our AI will extract the line items. You can then select which items to import as purchases — you're always in control of what gets added.
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
<summary>Why isn't my scheduled dose showing?</summary>

Check that:
1. Medication **Status** is "Active"
2. **Frequency** is set correctly
3. **Start Date** is today or earlier
4. For weekly medications, you're on the right day
</details>

<details markdown="block">
<summary>I'm not getting timer notifications</summary>

1. Click the 🔔 button to enable notifications
2. When your browser prompts, click "Allow"
3. Make sure your device's Do Not Disturb is off
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

*Updated: February 2026 | v3.1.10*
