# second thought

A writing assistant prototype that asks the writer to pause and reflect before relying on AI.

- `index.html`: Modern style (default)
- `retro.html`: Retro typewriter style

Both are static pages rendered by `support.js` (loads React from unpkg). No build step is needed.

## Run locally
Serve the folder over HTTP, e.g. `python3 -m http.server`, then open http://localhost:8000. (Opening the file directly may fail because the runtime fetches the page source.)

## Host free on GitHub Pages
1. Create a repository and push the contents of this folder to the `main` branch.
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Save. The site goes live at `https://<username>.github.io/<repo>/` within a minute or two.

## Notes
- Progress is saved in the browser's localStorage, separately for each visitor and device.
- Fonts load from Google Fonts and jsDelivr, so the pages need an internet connection for those fonts.
- Assistant replies are scripted. Live AI replies need an API key, which must not be committed to a public repository. Route requests through a small serverless function (for example on Cloudflare Workers or Vercel) instead.
