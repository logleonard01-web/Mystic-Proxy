# Mystic Hub — Standalone Proxy Bundle

Self-contained static site bundling Ultraviolet + bare-mux + Epoxy (wisp),
preconfigured to the Wisp server: `wss://orbitweb.org/campus/`.

## Run locally

Any static file server works, as long as it serves `sw.js` at the root.

```bash
npx serve .
# or
python3 -m http.server 8080
```

Open http://localhost:8080 and type a URL.

## Deploy

Upload the entire folder to any static host (Cloudflare Pages, Netlify,
Vercel, GitHub Pages, your own server). The service worker must be served
from the site root.

## Change the Wisp endpoint

Edit the `wisp:` value inside `index.html`.

## Files
- `index.html` — UI with URL bar and proxied iframe
- `sw.js` — Ultraviolet service worker
- `uv/` — Ultraviolet runtime
- `bare-mux/` — transport multiplexer
- `epoxy/` — Wisp transport
- `assets/mystic-logo.webp` — branding
