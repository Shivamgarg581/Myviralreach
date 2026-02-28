# Myviralreach — Premium Agency Landing Website

A premium, modern, single-page website for **Myviralreach** and **Shivam Garg** focused on influencer marketing and creator management.

## Overview

This project is a static front-end website designed to present:
- Agency positioning and value proposition
- About profile and role details
- Core services
- Creator showcase cards
- Brand collaboration workflow
- Creator onboarding CTA (Google Form)
- Email-only support/contact

It is built with plain HTML, CSS, and JavaScript, and is ready to host on GitHub Pages.

## Tech Stack

- **HTML5**
- **CSS3**
- **Vanilla JavaScript**

No backend or framework is required.

## Project Structure

```text
.
├── index.html   # Main single-page site (includes embedded CSS + JS)
├── styles.css   # Legacy standalone stylesheet
├── script.js    # Legacy standalone script
└── README.md
```

> The current primary implementation is in `index.html`.

## Features

- Premium clean cream/stone visual design
- Responsive layout (desktop + mobile)
- Smooth scrolling navigation
- Dark/light mode toggle with local storage persistence
- 3D tilt hover interactions for cards
- Scroll reveal animations (IntersectionObserver)
- Parallax visual accents on scroll
- Floating card hero composition
- Email-only contact section
- Footer year auto-updates via JavaScript

## Required Business Information Included

- **Name:** Shivam Garg
- **Role:** Influencer Marketing Agent | Creator Manager | Brand Collaboration Partner
- **Creator Form:** https://forms.gle/gqeakCTjyVFMNVd47
- **Contact Email:** shivgarg597@gmail.com

## Run Locally

From the project root:

```bash
python3 -m http.server 4173
```

Then open:

```text
http://localhost:4173
```

## Deployment (GitHub Pages)

1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Set Source to your main branch (root).
4. Save and wait for deployment.
5. Open your published URL.

## Customization Notes

- Update all copy/content in `index.html` sections.
- Modify design tokens in the `:root` CSS variables.
- Extend card sections for real creator/brand data.
- Replace sample collaboration flow with your live process.

## License

This project is provided for business website use and customization.
