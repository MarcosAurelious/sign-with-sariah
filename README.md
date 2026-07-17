# Sign with Sariah — Website

A one-page site for Sariah's notary public business: video hero, soft pink & gold styling, and an Instagram link.

## Files

```
index.html    the entire site — HTML, CSS, JS, and all images/video embedded inside it
.nojekyll     empty file that tells GitHub Pages to skip Jekyll processing (required — see note below)
```

**`index.html` is fully self-contained** (~4.5 MB). The photo, illustration, and video are compressed and embedded directly inside the file as data, so this one file is the whole website — no separate assets folder needed, and nothing breaks if you move it, rename it, or send it to someone else.

**Always include `.nojekyll` in the repo root next to `index.html`.** GitHub Pages runs a Jekyll build by default, which can mishandle a very large single-line file like this one and serve a blank or stale page. The empty `.nojekyll` file tells GitHub Pages to skip that build step and serve the files exactly as uploaded.

**When updating `index.html` later, always replace it by delete + re-upload — never edit it with GitHub's inline pencil/edit icon.** The file is one dense block of code, and GitHub's web editor can silently truncate or corrupt it on save (this happened once already — if the file in the repo is ever just a few bytes, that's what happened; delete it and re-upload fresh).

## How to view it

Open `index.html` in a browser (double-click it, or right-click → Open With → your browser). No build step, server, or internet connection required — it also works offline except for the Google Fonts, which need internet to load (the page still works fine without them, just with fallback fonts).

## How to publish it (GitHub Pages)

1. In the repo, make sure **both** `index.html` and `.nojekyll` are sitting at the root (not in a subfolder).
2. Go to **Settings → Pages**.
3. Under "Build and deployment," set **Source** to `Deploy from a branch`.
4. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
5. Wait 1–2 minutes, then visit:
   ```
   https://<your-username>.github.io/sign-with-sariah/
   ```
6. If it still looks stale, hard-refresh (`Ctrl+Shift+R` / `Cmd+Shift+R`) or open the URL in a private/incognito window — browsers cache pages aggressively.

### Other hosting options
Any static host works since it's a single HTML file with no build step:
- **Netlify / Vercel** — drag `index.html` into their dashboard.
- **Squarespace/Wix, etc.** — these don't usually accept raw HTML uploads directly; use a static host like the ones above and point a custom domain at it instead.

## Things to double-check before launch

- **Services list** — the six service cards (General Notarization, Loan Signings, Mobile Notary, Real Estate Docs, After-Hours Signings, Apostille Guidance) are placeholder copy. Confirm these match what Sariah actually offers.
- **Credentials row** in the About section ("State Commissioned," "Loan Signing Certified," etc.) — swap in her real certifications and state.
- **Service area** — copy is intentionally generic ("mobile notary," "wherever your signing needs to happen"). Add a specific city/region if she wants one called out.
- **Instagram link** — currently points to `https://instagram.com/signwithsariah`. Confirm that's correct.
- **Booking flow** — the "Book an appointment" and "DM on Instagram" buttons currently link to Instagram. If Sariah wants a contact form, phone number, or booking tool (e.g. Calendly) instead, that can be swapped in.

## Editing

Everything lives in `index.html`:
- Text content is in the HTML body (search for section names like `id="services"`, `id="about"`, etc.).
- Colors, fonts, and spacing are CSS variables at the top of the `<style>` block (`--cream`, `--blush`, `--rose`, `--gold`, etc.) — change those to retheme the whole site at once.
- For any text/CSS edits, download the file, edit it locally in a plain text editor, then re-upload the whole file (delete + upload) rather than editing on GitHub directly.
