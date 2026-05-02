# birthcertificateapostilles.com

Static site for birthcertificateapostilles.com. Pure HTML/CSS, no build step.

## Deploy

1. Push this repo to GitHub
2. Enable GitHub Pages: Settings → Pages → Branch: `main`, folder: `/ (root)`
3. Add custom domain in GitHub Pages settings: `www.birthcertificateapostilles.com`
4. At Porkbun: configure DNS (see DEPLOY.md)
5. Wait for SSL cert (usually < 1 hour)

## Pre-deploy checklist

- [ ] Replace `FORM_ID_HERE` everywhere with your Formspree form ID:
      `grep -rl "FORM_ID_HERE" . | xargs sed -i 's/FORM_ID_HERE/YOUR_ID_HERE/g'`
      (on macOS: `xargs sed -i ''`)
- [ ] Verify Formspree form is set to deliver to jared@apostillellc.com
- [ ] Spot-check a few state pages to confirm hero photos load

## Notes

- Hero images are sourced from Unsplash Source API (`source.unsplash.com`).
  These return a working image for the given keywords every request.
  No specific photo IDs to maintain.
- Site has 75 pages: home, blog index, 4 blog posts, 51 state pages,
  5 territory pages, 13 Canadian province pages.
