# Sk Md Ziad Rahman — Portfolio Website

Personal portfolio site for **Sk Md Ziad Rahman**, an e-commerce project management & QA professional. Built as a single-page, static HTML site — no build step, no frameworks, just clean HTML/CSS/JS.

🔗 **Live site:** [skziad.com](https://skziad.com)

## About

A single-page site with the following sections:

- **Home** — intro / hero with photo, resume download, and quick CTAs (schedule a meeting, send a message)
- **About** — background in e-commerce operations, fulfillment, logistics, inventory, QA, and SOP development
- **Skills** — tools and expertise (WooCommerce, Shopify, WordPress, Jira, Trello, HubSpot, Stripe, Google Analytics, etc.), styled as a grid
- **Experience** — work history presented as a git-log-style timeline
- **Education** — academic background and certifications
- **Contact** — a working contact form that submits directly to email via [Web3Forms](https://web3forms.com/) (no backend required)

## Tech Stack

- **HTML5 / CSS3 / vanilla JS** — single-file `index.html`, styles inline in a `<style>` block using CSS custom properties for theming
- **Fonts:** [Fraunces](https://fonts.google.com/specimen/Fraunces), [Inter](https://fonts.google.com/specimen/Inter), [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) via Google Fonts
- **Contact form:** [Web3Forms](https://web3forms.com/) — submits via `fetch()`, no server-side code needed
- **Custom error pages:** `400.shtml`, `401.shtml`, `403.shtml`, `404.shtml`, `500.shtml`
- **Favicons & touch icons:** generated for all standard sizes (16×16 up to 512×512)
- **Domain:** registered via [Namecheap](https://www.namecheap.com/)
- **Hosting:** shared hosting via [Hosting Bangladesh](https://www.hostingbangladesh.com/), deployed automatically from GitHub using GitHub Actions + FTP

## Project Structure

```
.
├── index.html                        # Main site (single-page)
├── 400.shtml                         # Bad Request error page
├── 401.shtml                         # Unauthorized error page
├── 403.shtml                         # Forbidden error page
├── 404.shtml                         # Not Found error page
├── 500.shtml                         # Internal Server Error page
├── assets/
│   ├── images/
│   │   └── Sk_Md_Ziad_Rahman.jpeg    # Profile photo
│   ├── favicons/
│   │   ├── favicon.ico
│   │   ├── favicon-16x16.png
│   │   ├── favicon-32x32.png
│   │   ├── favicon-48x48.png
│   │   ├── apple-touch-icon.png
│   │   ├── android-chrome-192x192.png
│   │   └── android-chrome-512x512.png
│   └── docs/
│       └── Resume.pdf                # Downloadable resume
├── .github/
│   └── workflows/
│       └── deploy.yml                # GitHub Actions workflow (auto-deploy on push)
└── .gitignore
```

> Note: the custom error pages (`400.shtml`–`500.shtml`) are kept at the site root, since that's where cPanel's error-page handling expects to find them.

## Deployment

The site is version-controlled on **GitHub** and deployed automatically to **Hosting Bangladesh** via **GitHub Actions**.

**How it works:**

1. Code changes are pushed to the `main` branch on GitHub.
2. A GitHub Actions workflow (`.github/workflows/deploy.yml`) triggers automatically on every push.
3. The workflow connects to the Hosting Bangladesh server over **FTP** and syncs the updated files — including the full `assets/` folder — to the live web root (`public_html`).
4. The domain `skziad.com` (registered on Namecheap) points to the Hosting Bangladesh server, so changes go live within moments of a successful deploy.

**Deployment credentials** (FTP host, username, password, and remote path) are stored securely as **GitHub Actions Secrets** and are never committed to the repository.

**To deploy an update:**
```bash
git add .
git commit -m "update site"
git push origin main
```
Then check the **Actions** tab on GitHub to confirm the deployment succeeded.

## License

© Sk Md Ziad Rahman. All rights reserved. This code is shared for portfolio/reference purposes; please don't reuse the personal content (name, resume, photos) as your own.
