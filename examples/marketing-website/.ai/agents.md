# Project: Harlow Advisory

## What it does
Marketing website for a boutique HR consulting firm. Showcases services, team, and case studies. Primary goal is to get visitors to book a discovery call via a contact form.

## Stack
- Frontend: Astro with plain CSS
- Backend: None (static site)
- Database: None
- Hosting: Netlify (auto-deploys from GitHub on push to main)

## Conventions
- One .astro file per page in /src/pages
- Reusable sections live in /src/components
- All colors and type sizes defined as CSS custom properties in /src/styles/tokens.css
- Images go in /public/images, optimized before adding (max 200kb)
- No JavaScript unless absolutely necessary — this is a static marketing site

## Never
- Don't add a JS framework — Astro's .astro components are enough
- Don't add animations that could affect page load score
- Don't change the contact form without testing it sends correctly first
- Don't rewrite sections that are already approved — only touch what's in the task

## Current focus
Add a Case Studies section to the homepage — three cards with a client industry, one-line outcome, and a "Read more" link. Content is in /src/content/case-studies/.
