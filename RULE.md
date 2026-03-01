# Project Rules — Art Follicle Landing

## Stack

- **HTML/CSS/JS** — plain vanilla, no frameworks, no build tools
- Single page: `index.html` → `src/css/style.css` → `src/js/app.js`
- All JS wrapped in one IIFE inside `app.js`

## CSS

- CSS variables only — never hardcode colors or sizes
- Light theme vars in `:root`, dark theme in `:root[data-theme="dark"]`
- Primary color: `#842bff` (light) / `#b865f7` (dark)
- Font: `"TildaSans"`, fallback `"Arial"`, `sans-serif`
- Base font size: `17px`, weight `450`

## JS

- One IIFE wrapping all logic in `app.js`
- Initialize via `initApp()` — called on `DOMContentLoaded` or immediately if DOM is ready
- Use `trackEvent(name, params)` for GA4 events
- Use `trackFacebookEvent(name, params)` for Facebook Pixel events — checks consent before sending
- No jQuery, no external libraries unless already in the project

## Analytics & Consent

- Google Consent Mode v2 is active — all storage denied by default
- Facebook Pixel consent revoked by default — granted only on "Accept All"
- Never send analytics events without checking consent first
- Do not add new tracking pixels or scripts without updating the consent flow

## Images

- Use `.webp` format stored in `assets/images/webp/`
- Lazy-load offscreen images (`loading="lazy"`)
- Always set `alt` attributes

## SEO

- One `<h1>` per page
- `<title>` and `<meta name="description">` must be filled
- Canonical URL must match the live domain: `https://transplantbusiness.com/`
- `sitemap.xml` and `robots.txt` must stay in sync with page changes

## Git

- Commit messages in English, imperative mood (`Fix`, `Add`, `Update`)
- Do not commit build artifacts, `.DS_Store`, or editor configs
- Main branch is `main`

## General

- No TypeScript, no bundlers, no preprocessors
- Keep HTML semantic — use proper heading hierarchy
- Mobile-first responsive design
- Do not introduce new dependencies without explicit approval
