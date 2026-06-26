# Eagle Network Solutions — Website

Static marketing site. **No build step.** Plain HTML + CSS, with React/Babel and Google Fonts loaded from CDN and compiled in the browser. Deploys to Vercel as-is.

## Deploy to Vercel through GitHub

1. Create a new GitHub repository.
2. Upload everything in this folder to the repo root (drag the files into GitHub's "add file" uploader, or `git push`). The repo root must contain `index.html`, `vercel.json`, and the `site/`, `assets/`, etc. folders directly (not nested inside another folder).
3. Go to https://vercel.com → **Add New… → Project** → **Import** your repo.
4. Framework Preset: **Other**. Build Command: **leave empty**. Output Directory: **leave empty** (root). Install Command: leave empty.
5. Click **Deploy**.

That is it. `vercel.json` handles clean URLs, the pretty-path rewrites (e.g. `/cyber-insurance-readiness`), and the 301 redirects from old URLs.

### Updating later
Push a change to the GitHub repo and Vercel redeploys automatically.

## Pages
- `index.html` / `Homepage.html` — Home
- `Solutions.html` — Managed IT, Cybersecurity, Strategic IT, Hardware (tabs)
- `CoManagedIT.html`, `RemoteOnlyIT.html`, `CyberInsuranceReadiness.html` — service pages
- `Industries.html` — industries hub
- `Municipalities.html`, `Manufacturing.html`, `Distribution.html`, `ProfessionalServices.html`, `PropertyManagement.html`, `NonProfits.html` — industry pages
- `About.html` — Who We Are / Our Team / Customer Reviews (tabs)
- `Blog.html` — Blog & News
- `Contact.html` — lead-gen form
- `PrivacyPolicy.html`, `AccessibilityStatement.html` — legal
- `sitemap.xml`, `robots.txt` — SEO

## Shared code
- `site/chrome.js` — unified header nav + footer + Organization/LocalBusiness JSON-LD, injected on every page
- `site/page.js` — section builder for service/industry pages (emits Service + FAQPage JSON-LD)
- `site/site.css`, `solutions/solutions.css`, `colors_and_type.css` — styles

## Before launch
- Replace every `[PHOTO: … replace before launch]` placeholder with real images in `assets/`.
- Replace flagged placeholder team bios, reviews, and blog cards with real content.
- Embed the real TimeZest scheduling widget where the placeholder appears on service/contact pages.
- The contact form and newsletter are front-end only (they show a success state but do not submit anywhere). Wire them to your form handler / CRM.
- Confirm the Privacy Policy and Accessibility Statement with your team / counsel.
