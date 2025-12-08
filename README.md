```markdown
# Guardian's Voice — Website & Documentation

This repository is a static website for the "Guardian's Voice" project — a prototype design for an always-on voice-triggered safety system and vehicle-crash detector that captures encrypted pre/post-trigger media and posts an automated payload to an automation system (e.g., n8n).

Contents
- index.html — landing page
- styles.css, script.js — frontend assets
- docs/ — technical documentation (enrollment, crash detection, API payload, privacy)
- .github/workflows/deploy.yml — GitHub Actions to publish to GitHub Pages
- CNAME — placeholder (replace with your domain)
- LICENSE — MIT

Important caution
- This project captures audio, video and location data. Before any pilot, have the privacy/consent text reviewed by legal counsel and set up explicit informed consent for participants.

Deploy
- Option A: GitHub Pages (workflow included). Push to main and the action publishes to gh-pages.
- Option B: Netlify / Vercel — connect the repo and deploy.

Next steps
- Wire the mobile app repo and backend endpoints (presigned upload endpoints, device registration).
- Replace contact email and backend placeholders in docs and index.html.
- Review and adapt privacy.md for your jurisdiction.

```