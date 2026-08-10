# STAR-C RCT — Study Team Resource Site

Internal resource site for the STAR-C RCT (NCT06855186). Hosts clinician-facing materials, study documentation, publications, and reference for the study team.

**Live site:** https://starcstudy.com

---

## What this repo is

A static website — one HTML file (`index.html`) plus a folder of documents. There is no database, no server-side code, and no framework. It is hosted for free on GitHub Pages, with the custom domain `starcstudy.com` registered through Cloudflare.

The design choice for a static site was deliberate: it keeps hosting free, keeps the site fast, and means the site will keep working with essentially no maintenance for years. Updates are made by editing files in this repo directly on GitHub — no login to any external system required.

## File structure

```
/
├── index.html          the entire site (all five pages in one file)
├── CNAME               the custom domain (do not delete — this makes starcstudy.com work)
├── README.md           this file
└── documents/          all downloadable materials (manuals, checklists, PDFs)
```

## How to make common edits

All edits happen in `index.html`. GitHub has a built-in editor: click the file, then click the pencil icon in the top right. Save by clicking "Commit changes" at the bottom. Changes go live within a minute or two.

**To add a new document to the Materials page:**

1. Upload the file to the `documents/` folder (in GitHub, use the "Add file" → "Upload files" button)
2. In `index.html`, find the section labeled `<!-- =============== MATERIALS =============== -->`
3. Copy an existing document card (the block starting with `<a href="documents/...`)
4. Paste it in the right category section and update the filename, title, version, and date

**To update an existing document:**

1. Upload the new version to `documents/` (with a new filename that includes the version and date, e.g. `..._v1_5_20260701.docx`)
2. In `index.html`, find the corresponding document card
3. Change the `href` to the new filename, and update the version badge and date

**To edit text (headline, description, FAQ, glossary, etc.):**

Just find the text in `index.html` and change it. HTML tags (things in angle brackets) should be left alone — only edit the text between them.

## Domain and hosting

- **Domain:** `starcstudy.com` registered through Cloudflare Registrar
- **Hosting:** GitHub Pages (free, from this repo)
- **DNS:** Cloudflare DNS points `starcstudy.com` and `www.starcstudy.com` at GitHub Pages

## Handoff notes

If this site needs to outlive its current maintainer, three things must not lapse:

1. **The Cloudflare domain registration.** Renews annually, ~$10/year. If it lapses, the domain expires and the site goes down.
2. **Admin access to this GitHub repo.** At least one active team member should have admin permissions.
3. **Admin access to the Cloudflare account** that owns the domain.

## Registration

STAR-C RCT is registered as **NCT06855186** on ClinicalTrials.gov.
