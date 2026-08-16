# Sk Md Ziad Rahman — Portfolio Website

Personal portfolio website for **Sk Md Ziad Rahman**, Project Manager. Built with plain HTML, CSS, and JavaScript — no frameworks, no build step.

🔗 **Live site:** [www.skziad.com](https://www.skziad.com)

---

## About

This site showcases my background in e-commerce project management, including:

- Career summary and professional stats
- Technical skills (WooCommerce, WordPress, Jira, Trello, Google Analytics, HubSpot, Stripe, and more)
- Work experience at MiraiLit Limited
- Education background
- A working contact form

## Tech Stack

- **HTML5 / CSS3 / vanilla JavaScript** — no frameworks or dependencies
- **[Web3Forms](https://web3forms.com/)** — handles contact form submissions without a backend server
- **GitHub Actions** — automatically deploys changes to production on every push to `main`

## Project Structure

```
.
├── index.html              # Main site file
├── .github/
│   └── workflows/
│       └── deploy.yml      # Auto-deploy workflow (GitHub → cPanel via SFTP)
└── README.md
```

## Deployment

This repo auto-deploys to production hosting on every push to the `main` branch, using a GitHub Actions workflow that uploads files to the server over SFTP.

**How it works:**
1. Push a commit to `main`
2. GitHub Actions triggers automatically
3. Files are synced to the live server via SFTP
4. Changes appear on [www.skziad.com](https://www.skziad.com) within about a minute

**Required repository secrets** (Settings → Secrets and variables → Actions):

| Secret name       | Description                                  |
|--------------------|-----------------------------------------------|
| `SSH_PRIVATE_KEY`  | Private SSH key (RSA, PEM format) authorized on the host |
| `SSH_HOST`         | Server hostname or IP address                |
| `SSH_USERNAME`     | Hosting account username                      |
| `REMOTE_TARGET`    | Server path to the site's `public_html` folder |





---

© Sk Md Ziad Rahman. All rights reserved.
