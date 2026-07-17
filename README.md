# Sign with Sariah — Website

A one-page site for Sariah's notary public business, built as a single static HTML file with a video hero, soft pink & gold styling, and an Instagram link.

## Files

```
index.html    the entire site — HTML, CSS, JS, and all images/video embedded inside it
assets/       original source files (kept for reference/editing only — not used by index.html)
```

**`index.html` is fully self-contained.** The photo, illustration, and video are embedded directly in the file as data, so you only need this one file — no separate `assets` folder required, and no broken images if you move it, rename it, or send it to someone else. (This does make the file large, about 10 MB, since the video is embedded as text.)

## How to view it

Just open `index.html` in a browser (double-click it, or right-click → Open With → your browser). No build step, server, or internet connection required — it also works offline except for the Google Fonts, which need internet to load (the page still works fine without them, just with fallback fonts).

## How to publish it (GitHub Pages)

This repo (`sign-with-sariah`) only needs **`index.html`** — nothing else. Delete `hero.mp4`, `illustration.png`, and `photo.jpg` from the repo root if they're still there; they're leftover from an earlier version and aren't used anymore.

1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment," set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
4. Wait a minute or two — GitHub will publish the site at:
   ```
   https://<your-username>.github.io/sign-with-sariah/
   ```
5. Any time you upload a new `index.html` to replace the old one, the live site updates automatically within a minute or so.

### Other hosting options
Any static host works since it's a single HTML file with no build step:
- **Netlify / Vercel** — drag `index.html` into their dashboard.
- **Squarespace/Wix, etc.** — these don't usually accept raw HTML uploads directly; use a static host like the ones above and point a custom domain at it instead.

## Things to double-check before launch

- **Services list** — the six service cards (General Notarization, Loan Signings, Mobile Notary, Real Estate Docs, After-Hours Signings, Apostille Guidance) are placeholder copy. Confirm these match what Sariah actually offers, and remove/edit any that don't apply.
- **Credentials row** in the About section ("State Commissioned," "Loan Signing Certified," etc.) — swap in her real certifications and state.
- **Service area** — the copy is intentionally generic ("mobile notary," "wherever your signing needs to happen"). Add a specific city/region if she wants one called out.
- **Instagram link** — currently points to `https://instagram.com/signwithsariah`. Confirm that's correct.
- **Booking flow** — the "Book an appointment" and "DM on Instagram" buttons currently just link to Instagram. If Sariah wants a contact form, phone number, or booking tool (e.g. Calendly) instead, that can be swapped in.

## Editing

Everything lives in `index.html`:
- Text content is in the HTML body (search for section names like `id="services"`, `id="about"`, etc.).
- Colors, fonts, and spacing are all defined as CSS variables at the top of the `<style>` block (`--cream`, `--blush`, `--rose`, `--gold`, etc.) — change those to retheme the whole site at once.
