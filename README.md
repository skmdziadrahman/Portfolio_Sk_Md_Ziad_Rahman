# Sk Md Ziad Rahman — Portfolio Website

Personal portfolio site for **Sk Md Ziad Rahman**, an e-commerce project management & QA professional. Built as a single-page, static HTML site — no build step, no frameworks, just clean HTML/CSS/JS.

🔗 **Live site:** [www.skziad.com](https://www.skziad.com)

## About

A single-page site with the following sections:

- **Home** — intro / hero with photo and quick CTAs (schedule a meeting, send a message)
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
- **Hosting:** GitHub Pages with a custom domain (see `CNAME`)

## Project Structure

```
.
├── index.html                   # Main site (single-page)
├── 400.shtml                    # Bad Request error page
├── 401.shtml                    # Unauthorized error page
├── 403.shtml                    # Forbidden error page
├── 404.shtml                    # Not Found error page
├── 500.shtml                    # Internal Server Error page
├── CNAME                        # Custom domain config for GitHub Pages
├── Resume.pdf                   # Downloadable resume
├── Sk_Md_Ziad_Rahman.jpeg       # Profile photo
├── favicon.ico
├── favicon-16x16.png
├── favicon-32x32.png
├── favicon-48x48.png
├── apple-touch-icon.png
├── android-chrome-192x192.png
├── android-chrome-512x512.png
└── .gitignore
```

## Deployment

The site is deployed via **GitHub Pages**, served from the `main` branch, and mapped to the custom domain `skziad.com` through the `CNAME` file. Any push to `main` updates the live site automatically.

## License

© Sk Md Ziad Rahman. All rights reserved. This code is shared for portfolio/reference purposes; please don't reuse the personal content (name, resume, photos) as your own.
