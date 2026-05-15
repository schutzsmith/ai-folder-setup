# Project: Spendr

## What it does
A personal expense tracking app for iOS and Android. Users can log expenses, set monthly budgets per category, and get a weekly summary notification.

## Stack
- Frontend: React Native (Expo)
- Backend: Supabase (auth + database)
- Database: Postgres via Supabase
- Hosting: App Store + Google Play (Expo EAS Build)

## Conventions
- All screens live in /app using Expo Router file-based routing
- Keep components in /components, one file per component
- Use Supabase client from /lib/supabase.ts — never import directly
- Styles use StyleSheet.create() — no inline styles
- All currency stored as integers (cents), formatted on display only

## Never
- Don't rewrite files I haven't asked you to touch
- Don't add new Expo packages without asking first — some conflict with EAS
- Don't change the Supabase schema without confirming with me
- Don't use any library that requires native code unless we've discussed it

## Current focus
Build the expense logging screen — form with amount, category picker, date, and optional note. Save to Supabase on submit.
