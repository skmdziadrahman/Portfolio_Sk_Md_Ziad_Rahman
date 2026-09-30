# Sk Md Ziad Rahman — Portfolio Website

Personal portfolio site for **Sk Md Ziad Rahman**, an E-commerce Project Manager & QA Engineer. Built as a single-page, static HTML site — no build step, no frameworks, just clean HTML/CSS/JS.

🔗 **Live site:** [www.skziad.com](https://www.skziad.com)

## About

A single-page site with the following sections:

- **Home** — intro / hero with photo and quick CTAs (schedule a meeting, send a message)
- **About** — background in e-commerce operations (order management, fulfillment, logistics, inventory, customer service) and software quality assurance
- **Skills** — operations, QA and tools (WooCommerce, Shopify, WordPress, Klaviyo, Brevo, Stripe, Jira, Postman, Newman, Apache JMeter, MySQL, etc.), styled as a grid
- **Experience** — work history presented as a git-log-style timeline
- **Projects** — QA and testing projects (API automation, performance, database and manual testing), each linking to its GitHub repository
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



## Search & AI Discoverability

The site is set up so search engines and AI assistants (ChatGPT, Claude, Perplexity, Google, etc.) can find and describe it accurately:

- **Structured data (JSON-LD)** in `index.html` — a schema.org `Person` / `ProfilePage` describing name, job title, employer, roles, education, certifications, skills and profile links
- **Open Graph & Twitter tags** — rich link previews when the site is shared on LinkedIn, WhatsApp, Facebook, Slack or X
- **Canonical URL** — `https://www.skziad.com/`
- **`llms.txt`** — a plain-text career summary written for AI assistants
- **`robots.txt`** — allows search engines and AI crawlers, and points to the sitemap
- **`sitemap.xml`** — lists the public pages
- **`assets/docs/.htaccess`** — keeps files in `assets/docs/` out of search and AI indexes (`noindex`) and disables folder listing; files there still open for anyone with the direct link



## Project Structure

```
.
├── index.html                        # Main site (single-page)
├── llms.txt                          # Plain-text summary for AI assistants
├── robots.txt                        # Crawler rules + sitemap location
├── sitemap.xml                       # Public pages for search engines
├── 400.shtml                         # Bad Request error page
├── 401.shtml                         # Unauthorized error page
├── 403.shtml                         # Forbidden error page
├── 404.shtml                         # Not Found error page
├── 500.shtml                         # Internal Server Error page
├── assets/
│   ├── images/
│   │   └── Sk_Md_Ziad_Rahman.jpeg    # Profile photo
│   ├── docs/                         # Private-by-link documents (not indexed)
│   │   └── .htaccess                 # noindex header + no directory listing
│   └── favicons/
│       ├── favicon.ico
│       ├── favicon-16x16.png
│       ├── favicon-32x32.png
│       ├── favicon-48x48.png
│       ├── apple-touch-icon.png
│       ├── android-chrome-192x192.png
│       └── android-chrome-512x512.png
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
3. The workflow connects to the Hosting Bangladesh server over **FTP** and syncs the updated files — including the full `assets/` folder — to the live web root (`public_html`). Git files, the `.github/` folder and this README are excluded from the upload.
4. The domain `www.skziad.com` (registered on Namecheap) points to the Hosting Bangladesh server, so changes go live within moments of a successful deploy.

**Deployment credentials** (FTP host, username, password, and remote path) are stored securely as **GitHub Actions Secrets** and are never committed to the repository.

## License

© Sk Md Ziad Rahman. All rights reserved. This code is shared for portfolio/reference purposes; please don't reuse the personal content (name, resume, photos) as your own.
