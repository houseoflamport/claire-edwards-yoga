# Clair Edwards Yoga — Health Forms
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
| Branding | Match clairedwardsyoga.com | ✅ Done |

**MVP is complete, branded, and live.** Awaiting final sign-off from Clair.

---

## File Structure

```
clair-edwards-yoga/
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

- **Sheet:** Clair Edwards Yoga — Health Forms (in Clair's Google account)
- **Tabs:** Restorative, Pregnancy, Postnatal
- **Apps Script URL:** `https://script.google.com/macros/s/AKfycbxaQRmaE1LVouTX5BRm0XBMICsQHNe9F3tNd2SAMYLL-nM-zMZZugj1Sf6GZl0jnXh_/exec`
- **Email notifications:** Sent to clairedwardsyoga@gmail.com on every submission
- **Subject line format:** `New Health Questionnaire — [Name] — [Class Type]`

⚠ **Important:** If submissions stop arriving, the most likely cause is the Apps Script deployment expiring or losing permissions after a Google account password change. Fix: open Apps Script, redeploy as a new deployment, and update the URL in all three HTML files.

---

## Branding

- **Background:** `#f3ede7` (warm cream — matches clairedwardsyoga.com exactly)
- **Text:** `#2c2420` (warm dark brown)
- **Buttons:** `#1a1a1a` black (Submit, Next only)
- **Heading font:** Playfair Display (Google Fonts — close match to her Kepler Std)
- **Body font:** Raleway (Google Fonts)
- **To tweak:** Edit `:root` variables at the top of `styles.css` — changes apply to all three forms instantly

---

## Parking Lot (Next Sessions)

| Item | Priority | Notes |
|------|----------|-------|
| Clair sign-off | High | Showing Clair tonight — minor CSS tweaks may follow |
| Weekly summary email | Medium | Apps Script sends Clair a weekly submission count — doubles as a heartbeat |
| Error logging | Medium | Log failed submissions to an Errors tab in the Google Sheet |
| Error log email | Medium | Email Clair if a submission fails so nothing is lost silently |
| End-to-end test with real data | High | Full realistic test on all three forms before first class |
| Custom domain | Low | Subdomain e.g. `forms.clairedwardsyoga.com` — do after sign-off |
| QR code regeneration | Low | Redo QR codes after URL changes to custom domain |
| TeamUp integration | Low | Mark questionnaire complete in TeamUp — complex, likely not worth it |

---

## Reliability & Testing Notes

**Before first real class use:**
- [ ] Submit all three forms with realistic data (not random characters)
- [ ] Verify sheet rows look sensible with real data
- [ ] Verify email content reads clearly with real data
- [ ] Test failed network scenario: fill form, turn wifi off, submit — confirm error message shows

**Known vulnerability:**
Apps Script deployments can expire if Clair's Google account password changes or Google revokes access. If submissions stop, redeploy the Apps Script and update the URL in all three HTML files.

**Planned improvements (parked):**
- Weekly heartbeat email from Apps Script
- Error tab in Google Sheet for failed submissions
- Email alert to Clair on submission failure

---

## Session Start Checklist (Playbook)

When picking this up next time:
- [ ] Attach all form HTML files + styles.css + this STATUS.md to the opening message
- [ ] Confirm which parking lot item we're working on
- [ ] Check GitHub Actions green tick before testing any changes
- [ ] Use Cmd+Shift+R hard reload if changes don't appear on the live site
