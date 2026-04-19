# CheckMyThing — Full Site

A free online calculators site built with plain HTML + React via CDN. Everything runs client-side; no backend needed.

## Files included

**Calculator pages (React-powered)**
- `age-calculator.html` — date-to-date age + health tips
- `bmi-calculator.html` — metric/imperial BMI
- `date-difference.html` — days/weeks/business days between dates
- `due-date-calculator.html` — pregnancy due date from LMP

**Site pages**
- `index.html` — homepage
- `calculators.html` — all calculators, by category
- `tools.html` — full tool listing
- `blog.html` — blog landing page
- `about.html` — about page
- `contact.html` — contact form (mailto-based)
- `privacy.html` — privacy policy (AdSense-compliant)
- `terms.html` — terms of service
- `404.html` — not found page

**SEO infrastructure**
- `sitemap.xml` — for Google Search Console
- `robots.txt` — crawler directives

## Deployment

1. Upload all files to your web host's root directory.
2. Configure "pretty URLs" (no `.html` extension). Options:
   - On Netlify / Vercel / Cloudflare Pages: works by default.
   - On Apache: add `.htaccess` with `Options +MultiViews`.
   - On Nginx: use `try_files $uri $uri.html $uri/ =404;`
   - Or: put each page in its own folder as `index.html` (e.g. `age-calculator/index.html`).
3. Set `404.html` as your custom error page.

## Before going live — replace these placeholders

- `ca-pub-XXXXXXXXXXXXXXXX` → your real Google AdSense publisher ID (6 pages)
- `data-ad-slot="1111111111"` etc. → real ad slot IDs from AdSense
- `/favicon.svg`, `/apple-touch-icon.png` → add real favicon files
- `/assets/og-home.png`, `/assets/age-calculator-og.png` → create 1200×630 social images
- Contact form (in `contact.html`) → connect to Formspree, Netlify Forms, or your own backend

## Submitting to Google

1. Add site to [Google Search Console](https://search.google.com/search-console).
2. Upload `sitemap.xml`.
3. Apply for AdSense only after privacy/terms/about/contact are live and reachable.

## License

Your project — adapt as needed.
