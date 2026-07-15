# HH Site Pro

A field inspection and issue-tracking Progressive Web App (PWA) for **Howard Humphreys Consulting Engineers**. Built for construction site audits — capture observations and photos, log issues by severity and status, and export professional branded PDF reports directly from a phone or desktop.

**Live app:** https://muhindichristine-se.github.io/HH-SITE-PRO/

---

## What it does

- **Site inspections** — create audit projects with client, project, and reference details
- **Issue logging** — record issues with title, description, assignee, severity (Critical / Moderate / Minor), and status (Open / In Progress / Closed)
- **Photo capture** — attach and annotate site photos; text-only issues are also supported
- **GPS tagging** — location data captured with issues where available
- **PDF reports** — export a fully branded multi-page report (cover, revision page, summary, and issue pages with photos)
- **PDF preview** — review all pages on-screen before downloading or sharing
- **Sharing** — send reports via the device share sheet (email, WhatsApp, Drive, etc.) with an auto-generated summary
- **Offline first** — works with no internet connection; all data is stored locally on the device
- **Installable** — add to a phone or desktop home screen as a standalone app

---

## Installing the app

**On Android (Chrome):** open the live link, then tap the **⬇ Install App to Home Screen** button, or use the browser menu (⋮) → *Install app*.

**On iPhone (Safari):** open the live link, tap the **Share** button, then *Add to Home Screen*.

Once installed, the app runs full-screen and works offline.

---

## Data & privacy

All inspection data — projects, issues, and photos — is stored **locally on each device** using the browser's IndexedDB. Nothing is uploaded to a server. Use **Backup Data** to export a JSON file and **Restore Data** to load it on another device.

> Clearing browser data for this site will erase local projects. Back up regularly.

---

## Repository contents

| File | Purpose |
|------|---------|
| `index.html` | The complete single-file application (UI, logic, styling) |
| `manifest.json` | PWA manifest — app name, colours, icons, install config |
| `sw.js` | Service worker — enables offline use (network-first strategy) |
| `icon-192.png` | App icon (192×192) |
| `icon-512.png` | App icon (512×512) |

---

## Deployment

The app is served via **GitHub Pages** from the `main` branch. To update:

1. Replace the relevant file(s) in the repository root
2. Commit and push to `main`
3. GitHub Pages redeploys automatically within a minute or two

The main file **must** be named `index.html` for GitHub Pages to serve it as the site root.

---

## Tech notes

- Single-file architecture — the app lives entirely in `index.html`
- **jsPDF** for PDF generation, **PDF.js** for on-screen preview
- **IndexedDB** for local storage of projects and photos
- **Web Share API** for sharing reports to other apps
- Service worker + manifest provide offline support and installability

---

*Built for Howard Humphreys Consulting Engineers.*
