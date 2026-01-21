---
layout: default
title: FAQ
nav_order: 4
---

# Frequently Asked Questions
{: .fs-9 }

Common questions about Peptide Track+
{: .fs-6 .fw-300 }

---

## General

<details open markdown="block">
<summary>What is Peptide Track+?</summary>

Peptide Track+ is a web application for tracking peptide therapy, supplements, and related health data. It helps you manage dosing schedules, calculate injection units, log doses, and track lab results.
</details>

<details markdown="block">
<summary>Is my data secure?</summary>

Yes. Your data is stored securely with encryption. We never share your personal health information with third parties.
</details>

<details markdown="block">
<summary>Can I use this on my phone?</summary>

Yes! Peptide Track+ is fully responsive and works on smartphones, tablets, and desktop computers. Just visit [trackmeplus.com](https://trackmeplus.com) in your mobile browser.
</details>

---

## Compounds

<details markdown="block">
<summary>How do I calculate injection units?</summary>

Peptide Track+ calculates units automatically when you set up a vial compound. The formula is:

```
Units = (Dose mg ÷ (Vial mg ÷ BAC water mL)) × 100
```

**Example:** 0.5mg dose from a 10mg vial with 2mL BAC water = 10 units
</details>

<details markdown="block">
<summary>What's the difference between compound types?</summary>

| Type | Use For | Unit Calculation |
|:-----|:--------|:-----------------|
| Vial | Injectable peptides | Syringe units |
| Drops | Sublingual liquids | Number of drops |
| Pills | Tablets/capsules | N/A |
</details>

<details markdown="block">
<summary>How do I track multiple time doses?</summary>

When setting up a compound, you can add multiple "Time of Day" entries. Each will appear separately in your daily schedule.
</details>

---

## Doses

<details markdown="block">
<summary>What's the easiest way to log a dose?</summary>

From your Dashboard, find the dose in "Today's Schedule" and check the **Done** checkbox. That's it!
</details>

<details markdown="block">
<summary>Can I log a dose for a past date?</summary>

Yes. Click **Add Dose** and select any date in the past.
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
<summary>What's included in the free plan?</summary>

- Up to 3 compounds
- 10 lab results per year
- Basic dashboard
- Email support
</details>

<details markdown="block">
<summary>How do I upgrade my plan?</summary>

Go to **Settings → Billing** and click the **Upgrade** button for your desired plan.
</details>

<details markdown="block">
<summary>Can I cancel anytime?</summary>

Yes. Go to **Settings → Billing** and click **Cancel Subscription**. You'll retain access until the end of your billing period.
</details>

---

## Troubleshooting

<details markdown="block">
<summary>Why isn't my scheduled dose showing?</summary>

Check that:
1. Compound **Status** is "Active"
2. **Frequency** is set correctly
3. **Start Date** is today or earlier
4. For weekly compounds, you're on the right day
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
