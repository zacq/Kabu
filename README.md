# Simon Kabu — landing page

Static site, no build step. `support.js` loads React/ReactDOM from a CDN at
runtime and boots the page client-side — Netlify just needs to serve these
files as-is.

## Files
- `index.html` — the page (Claude Design canvas format, rendered by `support.js`)
- `support.js` — the render runtime
- `img/` — the 13 photos used on the page
- `netlify.toml` — publish config + caching headers

## Deploy to Netlify

**Drag-and-drop (fastest):** go to [app.netlify.com/drop](https://app.netlify.com/drop)
and drag this `site` folder onto the page. Done — you get a live URL immediately.

**Netlify CLI:**
```
npm install -g netlify-cli
cd site
netlify deploy --prod
```

**Git-based:** push this folder to a repo, then in Netlify: New site from Git →
select the repo → build command: (leave empty) → publish directory: `.` (or
wherever this folder sits in the repo) → Deploy.

## Before this goes fully public
Two things in the page are placeholders, each marked with an HTML comment in
`index.html` — search for `[PLACEHOLDER]`:
- The stat row in the Story section (countries/years/trips/community size)
- The three testimonial quotes in the Community section

Replace both with real numbers/quotes before sharing this as the final site
rather than a pitch draft.

## Hero video
`img/hero.jpeg` is the current hero background. Once the animated loop is
generated (WaveSpeed Seedance 2.5), drop the `.mp4` into `img/` and swap the
hero `<img>` (and the closing-footer `<img>`, which reuses the same photo)
for the two-stacked-`<video>`-with-crossfade pattern.
