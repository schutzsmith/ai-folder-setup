# Project: Briefd

## What it does
A web app for freelancers to create and send project proposals. Users fill out a form, and the app generates a clean, shareable proposal page with a unique link they can send to clients.

## Stack
- Frontend: Next.js 15 (App Router), plain CSS modules
- Backend: Next.js API routes
- Database: Supabase (Postgres)
- Hosting: Vercel

## Conventions
- Use the App Router — no pages/ directory
- Server components by default; only use "use client" when needed
- CSS modules only — no Tailwind, no styled-components
- All Supabase queries go through /lib/db.ts, never query directly in components
- Environment variables prefixed NEXT_PUBLIC_ for client, unprefixed for server

## Never
- Don't switch from App Router to Pages Router
- Don't add an ORM (Prisma, Drizzle) — we're using raw Supabase queries
- Don't rewrite working pages to add features — add incrementally
- Don't change auth logic without discussing it first

## Current focus
Build the proposal creation form — client name, project title, scope (textarea), price, and timeline. On submit, save to Supabase and redirect to the shareable proposal page at /p/[id].
