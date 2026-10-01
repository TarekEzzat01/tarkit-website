# Website security review

Scope: public V.Final_one marketing site only; 1 October 2026.

Applied guidance from `performing-security-headers-audit` and `securing-github-actions-workflows` in the user-requested mukul975/anthropic-cybersecurity-skills repository. These skills were inspected and installed locally. No intrusive scanning was performed.

- Runtime scripts, styles, fonts and images are local.
- No evaluation functions, inline event handlers, or dynamic HTML insertion in the authored site script.
- Form fields are encoded into an email draft and never interpolated into page HTML.
- Query input for contact interests is allowlisted against the select options.
- Restrictive CSP on every page; local scripts plus a hash for page-specific JSON-LD.
- Explicit referrer policy; new-tab links use noopener/noreferrer.
- No backend, API credentials, tracking pixels, or analytics added.
- Browser-side demo credentials are intentionally public per user approval. The linked CRM demonstration is public and contains fictional data. Real access protection is outside this demo mechanism.
- Prefer GitHub's managed branch-based Pages deployment; no custom privileged workflow is needed for this static site.
- GitHub Pages header limitations: meta policy cannot set frame-ancestors, HTTP X-Frame-Options, X-Content-Type-Options, or Permissions-Policy. A configurable edge/hosting service is required to add them.
- Live HTTPS, domain validation, and response headers must be verified after DNS is connected; local checks do not establish their live state.
