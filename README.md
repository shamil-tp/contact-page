# Contact Shamil TP

> A lightweight, terminal-inspired communication hub for direct software engineering inquiries.

[![Contact portal](https://img.shields.io/badge/contact-contact.shamiltp.life-000000?style=flat-square&logo=cloudflare&logoColor=white)](https://contact.shamiltp.life)
[![Main site](https://img.shields.io/badge/main-shamiltp.me-000000?style=flat-square&logo=vercel&logoColor=white)](https://shamiltp.me)

## Live links

- **Contact portal:** [contact.shamiltp.life](https://contact.shamiltp.life)
- **Main portfolio:** [shamiltp.me](https://shamiltp.me)

## What it is

This repository contains a fast, single-file contact page for **Shamil TP**. It keeps the interface intentionally focused: a direct-message terminal, clear contact fields, and no unnecessary portfolio or project content.

## Highlights

- Pure black-and-white terminal interface with responsive, accessible controls
- SEO-ready metadata, canonical URL, Open Graph/Twitter previews, sitemap, and robots rules
- JSON-LD structured data for `Person`, `ContactPage`, and `ProfilePage`
- Social preview image for share cards
- No framework, build step, or runtime dependency for the frontend

## Message delivery

The form sends a JSON payload (`name`, `email`, and `message`) to a **Cloudflare Serverless Worker**. The Worker provides the API layer for the contact workflow, keeping the static frontend separate from server-side message handling.

```text
Browser contact form
        │  POST application/json
        ▼
Cloudflare Serverless Worker
        │
        ▼
Contact-message processing and delivery
```

## Local preview

Open `index.html` in a browser, or serve this directory with any static web server. The form requires the deployed Cloudflare Worker endpoint to submit messages successfully.

## Project files

```text
index.html                 Contact page, metadata, styles, schema, and form logic
og-contact-shamil-tp.png   Open Graph / social sharing image
robots.txt                 Crawler directives
sitemap.xml                Contact-page sitemap
```

## Deployment notes

Deploy the static files at the contact domain, keep HTTPS enabled, and make sure the Worker accepts requests from the production origin. After deployment, submit the sitemap in Google Search Console and test the live URL with Google’s Rich Results Test.

---

Built for direct communication with [Shamil TP](https://shamiltp.me).
