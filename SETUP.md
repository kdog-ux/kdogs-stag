# KDOG'S STAG — 90s Office Corporate Chaos

This folder contains a mobile-friendly invite prototype.

## What works now
- Full chronological stag itinerary
- 90s corporate/office visual design
- Pub crawl word cloud
- Employee of the Month voting UI
- Mobile responsive layout

## Important: making it genuinely LIVE
The included page is deliberately standalone, so it works immediately, but its word cloud and vote data are stored only in each visitor's browser.

For a shared live page where everyone's submissions appear for everyone else, connect the page to a realtime database such as Supabase (or another hosted realtime backend).

A production setup should:
1. Create a database table for `pub_suggestions`.
2. Create a table for `employee_votes`.
3. Enable realtime updates for `pub_suggestions`.
4. Add anti-spam/rate limiting and duplicate/abuse controls.
5. Put the resulting site on a static host such as Vercel, Netlify, GitHub Pages, or Cloudflare Pages.

I can adapt the code to whichever hosting/database account you use and wire the live word cloud to it.
