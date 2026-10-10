# MyViralReach — Influencer Marketing & Creator Partnerships

MyViralReach connects brands with creators for influencer campaigns, UGC, short-form video, creator management, and campaign coordination.

## Website
- Main page: `index.html`
- Stack: HTML5, embedded CSS, and vanilla JavaScript
- Hosting: static hosting providers such as Netlify

## Current website features
- Responsive landing page for brands and creators
- Mobile navigation with keyboard dismissal and accessible expanded state
- Creator pitch builder and download/copy tools
- Campaign brief form
- Creator rate and campaign cost calculators
- Reduced-motion support and accessible focus styles

## Business model
MyViralReach works on a **20% commission when a deal closes**, with no retainer or upfront fee. Campaign scope, deliverables, creator availability, payment timing, usage rights, and approval terms should be agreed in writing before a campaign starts.

## Contact
- Email: shivgarg597@gmail.com
- Website: https://myviralreach.netlify.app
- GitHub: https://github.com/Shivamgarg581/Myviralreach

## Run locally
From this repository directory, run:
```bash
python3 -m http.server 4173
```
Then visit `http://localhost:4173`.

## Deploy
This repository is currently a static website. Push/merge the approved code to the branch configured in your Netlify site to publish it. Check the Netlify deploy log after pushing.

## Important limitation
This repository does **not** currently contain a backend, user login, Supabase data access, or Gmail OAuth integration. The public landing page's forms use an external form service. Do not treat the website as a complete influencer CRM until those server-side features are implemented and tested.
