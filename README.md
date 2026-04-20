# CheckMyThing — Fixed Bundle (Netlify)

**Changes in this version:**

1. ✅ **Fixed broken nav on age-calculator.html** — all links pointed to the not-yet-connected checkmything.com domain. Now use relative paths like the other pages.
2. ✅ **All canonical URLs updated to `https://checkmything.netlify.app`** — so Google doesn't get confused about which version to index.
3. ✅ **All Open Graph URLs, JSON-LD URLs, breadcrumb schema, and organization schema updated** to the Netlify domain.
4. ✅ **sitemap.xml and robots.txt updated** to reference the Netlify URLs.
5. ✅ **Privacy & Terms "Last updated" dates** changed from January 2025 → April 2026.
6. ✅ **Favicon added** (`favicon.svg`) — small inline SVG with your brand gradient. No more browser 404s for favicon.

## How to deploy

1. Unzip this bundle.
2. Drag the extracted folder onto your Netlify site (or `git push` if you have a repo connected).
3. Done. All links will work immediately.

## When you connect your real domain (checkmything.com)

You'll need to find-and-replace `https://checkmything.netlify.app` → `https://checkmything.com` across all HTML + sitemap.xml + robots.txt. Should take 30 seconds with sed:

```bash
find . -type f \( -name "*.html" -o -name "*.xml" -o -name "*.txt" \) \
  -exec sed -i 's|https://checkmything.netlify.app|https://checkmything.com|g' {} +
```

Also set up a 301 redirect from `checkmything.netlify.app` → `checkmything.com` in Netlify's domain settings so you don't lose SEO juice.

## Still to do (not in this bundle)

- Replace `ca-pub-XXXXXXXXXXXXXXXX` with your real AdSense publisher ID
- Replace `data-ad-slot="XXXXXXXXXX"` placeholders with real slot IDs after AdSense approval
- Create a 1200×630 OG share image at `/assets/og-home.png` and `/assets/age-calculator-og.png`
- Verify the site in Google Search Console and submit `sitemap.xml`
- Enable Google Analytics (currently commented out in index.html)
- Optional: move to a proper build pipeline (Vite + compiled Tailwind) for ~10× faster page loads
