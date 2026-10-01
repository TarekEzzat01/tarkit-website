# Tarkit — V.Final_one

A static company website combining the consultancy homepage from V.01 and CRM product page from V.03. Open `index.html` through a static HTTP server. No build process or package installation is required.

## Pages

- Home: `index.html`
- Consulting: `services.html`
- Product: `crm.html`
- Insights: `insights.html` and three linked practical guides
- Work samples and downloads: `sample-work.html` and `resources/*.csv`
- Company: `about.html`
- Sales: `contact.html`
- Demo access: `login.html`
- Privacy: `privacy.html`
- Missing page: `404.html`

## Audience and evidence

The primary markets are Saudi Arabia, the wider Gulf, and Egypt. Public work samples use fictional scenarios; they are not client case studies or proof of results. Guides include blank CSV worksheets and organization authorship. Further founder credentials and client evidence require verified facts and publication permission.

## Editing

Shared styles are in `assets/base.css` (preserved source design) and `assets/site.css` (final responsive refinements). Shared behavior is in `assets/site.js`. Page content and navigation are static HTML so they remain crawlable. Every page includes a canonical URL and Organization/WebSite/page structured data. When editing JSON-LD, update its SHA-256 hash in that page's Content-Security-Policy.

The contact form prepares an email draft; it does not send a message or store a form submission. Configure the recipient consistently in contact.html and assets/site.js before changing addresses.

## Demo access

The login screen is an explicitly approved browser-side demo check. It is bypassable, the credentials are public source code, and it is not production authentication. It redirects to the existing public fictional CRM demo without putting credentials in its URL. No production CRM data or authentication service is included in this repository.

## Hosting and domain

Publish this directory alone. The larger private company workspace must never be uploaded as the website. Canonical URLs target https://tarkit.io/. GitHub Pages can serve the static files from the main branch root. Configure the custom domain in GitHub before changing DNS; the deployment handoff records the required records and verification status.

## Security boundaries

All runtime resources are local. A restrictive meta CSP blocks off-origin scripts, network connections, objects, form submissions, and base-URL changes; JSON-LD uses per-page script hashes. Fonts and the icon library are pinned copies. The site has no analytics, cookies, database, API secrets, or third-party embeds.

GitHub Pages does not provide arbitrary custom response-header configuration. Meta CSP cannot enforce frame-ancestors, and header-only defenses such as X-Content-Type-Options and Permissions-Policy need a hosting/proxy layer that supports them. Do not claim a full security certification or a headers score from these source checks.

## Asset provenance

See ASSETS.md for font and logo sources. Displayed logos identify tools; they do not assert certifications or product integrations. The inherited GTM Heist relationship is not displayed pending clarification and permission.
