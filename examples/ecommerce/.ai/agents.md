# Project: Woven & Co.

## What it does
An online store selling handmade textile goods — throws, cushions, and wall hangings. Small catalog (~40 products), direct-to-consumer, ships in the US only.

## Stack
- Frontend: Shopify (Dawn theme, customized via theme editor + custom Liquid sections)
- Backend: Shopify (orders, inventory, fulfillment all managed in Shopify admin)
- Database: Shopify (no external database)
- Hosting: Shopify

## Conventions
- Custom code goes in /sections (new Liquid sections) or /snippets (reusable partials)
- Use CSS custom properties for all colors and spacing — defined in base.css
- JavaScript should be vanilla — no jQuery, no build step
- Never edit dawn's core files directly — override via CSS or wrap in a new section

## Never
- Don't install apps without checking if it can be done with custom Liquid first
- Don't touch checkout customization — that's Shopify Plus only
- Don't modify theme.liquid directly unless there's no other way
- Don't add anything that slows down page load — we care a lot about Core Web Vitals

## Current focus
Build a custom "Shop by Material" section for the homepage — a grid of material swatches (wool, cotton, linen, jute) that link to collection pages filtered by that material tag.
