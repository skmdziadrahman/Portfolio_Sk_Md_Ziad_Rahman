# Sk Md Ziad Rahman — Portfolio Website

Personal portfolio site for **Sk Md Ziad Rahman**, an e-commerce operations and project management professional. Built as a single-page, static HTML site — no build step, no frameworks, just clean HTML/CSS.

🔗 **Live site:** [www.skziad.com](https://www.skziad.com)

## About

This site showcases my background in e-commerce operations, including:

- End-to-end order management, fulfillment, and logistics
- Team leadership and mentoring
- SOP development and process documentation
- Inventory, vendor, and procurement coordination
- Work history, education, and a contact section

## Tech Stack

- **HTML5 / CSS3** — single-file `index.html` with all styles inline (`<style>` block, CSS custom properties for theming)
- **Fonts:** [Fraunces](https://fonts.google.com/specimen/Fraunces), [Inter](https://fonts.google.com/specimen/Inter), [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) via Google Fonts
- **Custom error pages:** `400.shtml`, `401.shtml`, `403.shtml`, `404.shtml`, `500.shtml`
- **Favicons & touch icons:** generated for all standard sizes (16×16 up to 512×512)

## Project Structure

```
.
├── index.html                   # Main site (single-page)
├── 400.shtml                    # Bad Request error page
├── 401.shtml                    # Unauthorized error page
├── 403.shtml                    # Forbidden error page
├── 404.shtml                    # Not Found error page
├── 500.shtml                    # Internal Server Error page
├── favicon.ico
├── favicon-16x16.png
├── favicon-32x32.png
├── favicon-48x48.png
├── apple-touch-icon.png
├── android-chrome-192x192.png
├── android-chrome-512x512.png
└── .gitignore
```

## Running Locally

No build tools required. Clone the repo and open the file directly, or serve it with any static server:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# Option 1: just open it
open index.html   # macOS
# or double-click index.html in your file explorer

# Option 2: serve it locally (recommended, so favicons/paths resolve correctly)
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Customizing

Look for `EDIT:` comments inside `index.html` — each one marks a spot meant to be replaced with your own content (name, bio, projects, skills, work history, links). Colors and fonts are controlled via the CSS custom properties in the `:root` block near the top of the `<style>` section.

The contact form currently just displays a confirmation message client-side. To make it functional, wire it up to a backend or a service such as [Formspree](https://formspree.io).

## Deployment

This is a static site, so it can be deployed to any static host — GitHub Pages, Netlify, Vercel, Cloudflare Pages, etc. For GitHub Pages:

1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Set the source to the `main` branch (root).
4. Point your custom domain (e.g. `skziad.com`) at GitHub Pages if desired, and add a `CNAME` file with your domain.

## Contact

- **Email:** skmdziadrahman00@gmail.com
- **LinkedIn:** [linkedin.com/in/skmdziadrahman0](https://www.linkedin.com/in/skmdziadrahman0/)
- **Website:** [www.skziad.com](https://www.skziad.com)

## License

© Sk Md Ziad Rahman. All rights reserved. This code is shared for portfolio/reference purposes; please don't reuse the personal content (name, resume, photos) as your own.
