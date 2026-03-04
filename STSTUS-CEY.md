# Claire Edwards Yoga — Health Forms
## Project Status & Session Handoff

**Last updated:** March 2026  
**Repo:** `houseoflamport/claire-edwards-yoga`  
**Live URL:** `https://houseoflamport.github.io/claire-edwards-yoga/`

---

## Current Status

| Story | Description | Status |
|-------|-------------|--------|
| Story 1 | Restorative health form | ✅ Done |
| Story 2 | Pregnancy health form | ✅ Done |
| Story 3 | Postnatal health form (4 steps) | ✅ Done |
| Story 4 | Google Sheet + email notification | ✅ Done |
| Story 5 | QR codes | ✅ Done |

**MVP is complete and live.** All three forms are collecting data, writing to Google Sheets, and sending email notifications to Claire.

---

## File Structure

```
claire-edwards-yoga/
  restorative-health-form.html   — Restorative yoga form (single page)
  pregnancy-health-form.html     — Pregnancy yoga form (single page)
  postnatal-health-form.html     — Postnatal yoga form (4 steps)
  styles.css                     — Shared CSS for all three forms
  qr-codes.html                  — QR code page (all three, downloadable)
  README.md
  STATUS.md                      — This file
```

---

## Live Form URLs

| Form | URL |
|------|-----|
| Restorative | https://houseoflamport.github.io/claire-edwards-yoga/restorative-health-form.html |
| Pregnancy | https://houseoflamport.github.io/claire-edwards-yoga/pregnancy-health-form.html |
| Postnatal | https://houseoflamport.github.io/claire-edwards-yoga/postnatal-health-form.html |
| QR Codes | https://houseoflamport.github.io/claire-edwards-yoga/qr-codes.html |

---

## Google Sheet & Apps Script

- **Sheet:** Claire Edwards Yoga — Health Forms (in Claire's Google account)
- **Tabs:** Restorative, Pregnancy, Postnatal — sorted newest first
- **Apps Script URL:** `https://script.google.com/macros/s/AKfycbxaQRmaE1LVouTX5BRm0XBMICsQHNe9F3tNd2SAMYLL-nM-zMZZugj1Sf6GZl0jnXh_/exec`
- **Email notifications:** Sent to clairedwardsyoga@gmail.com on every submission
- **Subject line format:** `New Health Questionnaire — [Name] — [Class Type]`

---

## Parking Lot (Next Stories)

| Item | Notes |
|------|-------|
| Brand styling | **Priority next** — match clairedwardsyoga.com, see branding notes below |
| Custom domain | Subdomain pointing to GitHub Pages e.g. `forms.clairedwardsyoga.com` — do after branding |
| QR code regeneration | Must redo QR codes after URL changes to custom domain |
| TeamUp integration | Mark questionnaire complete in TeamUp — complex, likely not worth it |

---

## Branding Notes (Next Session)

Claire's website: `https://clairedwardsyoga.com`

**Before starting — inspect clairedwardsyoga.com in Chrome (F12 → Elements) and note:**
- Background colour (appears to be a soft blue-grey)
- Main font name and weights
- Heading font if different from body
- Accent/button colour (appears to be black `#000` or near-black)

**Where branding lives in the code:**  
All colours and fonts are in `styles.css` only — edit the `:root` variables at the top to restyle all three forms at once:

```css
:root {
  --sage: #7a8c6e;          /* change to match her brand */
  --sage-light: #a8b89a;
  --sage-pale: #eef1eb;
  --sage-dark: #4a5c3e;     /* header background — change to her brand colour */
  --warm-white: #faf9f6;    /* page background */
  --warm-grey: #f2efe9;
  --text: #2c2c2a;
  --text-muted: #7a7870;
  --border: #d8d4cc;
  --accent: #c17f4a;
  --error: #b85c4a;
}
```

Fonts are loaded from Google Fonts in each HTML file's `<head>`:
```html
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond...&family=Jost...">
```
Replace `Cormorant+Garamond` and `Jost` with Claire's fonts once identified.

---

## Session Start Checklist (Playbook)

When picking this up next time:
- [ ] Attach all form HTML files + styles.css + this STATUS.md to the opening message
- [ ] Confirm which story we're working on (branding next)
- [ ] Inspect clairedwardsyoga.com for brand colours and fonts before starting
- [ ] Review parking lot — anything to promote or dismiss?
