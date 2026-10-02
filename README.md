# second thought

A writing assistant prototype that asks the writer to pause and reflect before relying on AI.

**Live demo:** https://xiwang16.github.io/second-thought/

- [Modern](https://xiwang16.github.io/second-thought/) (`index.html`, default)
- [Retro](https://xiwang16.github.io/second-thought/retro.html) (`retro.html`, typewriter style)

Both are static pages rendered by `support.js` (loads React from unpkg). No build step is needed.

## Run locally

Serve the folder over HTTP, e.g. `python3 -m http.server`, then open http://localhost:8000. (Opening the file directly may fail because the runtime fetches the page source.)

## Notes

- Progress is saved in the browser's localStorage, separately for each visitor and device.
- Fonts load from Google Fonts and jsDelivr, so the pages need an internet connection for those fonts.
- Assistant replies are scripted. Live AI replies need an API key, which must not be committed to a public repository. Route requests through a small serverless function (for example on Cloudflare Workers or Vercel) instead.
