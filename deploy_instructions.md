```markdown
# Deploy & Domain setup instructions

This project includes a GitHub Action that deploys the static site to GitHub Pages on every push to `main`. Follow these steps to publish:

1) Create a GitHub repository
- Create a new public repository under your account (e.g., `sos-relay-site`).

2) Push files
- Locally:
  git init
  git add .
  git commit -m "Initial site"
  git branch -M main
  git remote add origin git@github.com:<your-username>/<repo>.git
  git push -u origin main

3) First deploy
- The workflow `.github/workflows/deploy.yml` runs on push to `main`. It copies the site files into a `public/` directory and uses an action to publish to the `gh-pages` branch.

4) Enable GitHub Pages (if not automatic)
- Go to repository Settings → Pages. Confirm the source is `gh-pages` branch, `/ (root)`. GitHub will provide the site URL:
  https://<your-github-username>.github.io/<repo>/
- It may take a few minutes for the page to appear the first time.

5) Custom domain
- Purchase a domain (registrars: Google Domains, Namecheap, Cloudflare).
- Replace the content of the `CNAME` file with your domain (e.g., `niyazai.com`).
- Add DNS records at your registrar (example for GitHub Pages with a root/apex domain):
  - A records to GitHub Pages IPs:
    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153
  - Add a CNAME for `www` pointing to `<your-github-username>.github.io`.
- Alternatively, follow GitHub Pages domain setup UI which provides exact DNS entries.

6) Alternatives
- If you prefer Netlify or Vercel, follow the platform UI to connect the GitHub repo and configure domain mapping there. Both provide automated SSL.

Security & placeholders
- Before publishing publicly: replace `hello@example.com` and `TEST_DEVICE_TOKEN` / `YOUR_BACKEND_HOST` placeholders with real values.
- Review and adjust privacy.md and consent text with legal counsel.

If you want, I can:
- Provide a zip file of the repo content ready to upload.
- Walk you step-by-step through pushing to GitHub and setting the custom domain after you buy it.
```