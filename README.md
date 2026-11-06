# By a Thread

One-touch arcade game. Points only come from near misses. Live at https://byathread.app

This repo is the website, served as static files by Cloudflare Pages. There's no build step.

| File | What it is |
|---|---|
| `index.html` | The whole game: HTML, CSS and JS in one file |
| `manifest.webmanifest`, `sw.js`, `icon-*.png` | Add-to-home-screen (PWA) and offline support |
| `og.png` | Link preview image (1200×630) |
| `privacy.html`, `terms.html`, `delete-data.html` | Legal pages, served at `/privacy`, `/terms` and `/delete-data` |
| `_headers` | Cloudflare caching and security headers |

The backend is Supabase project `lmxjieimbueowtcthfof`, in eu-west-3. All database access goes through RPC functions. The anon key in `index.html` is public by design, and row-level security blocks direct table access.

Deploying: push to `main`, and Cloudflare Pages publishes it within about a minute.
