# Sign with Sariah — Website

A one-page site for Sariah's notary public business, built as a single static HTML file with a video hero, soft pink & gold styling, and an Instagram link.

## Files

```
index.html          the whole site (HTML + CSS + JS in one file)
assets/
  hero.mp4           video used as the homepage opener
  photo.jpg          Sariah's photo, used in the About section
  illustration.png   the notary-desk illustration, used in the quote section
```

**Keep this folder structure intact.** `index.html` links to the images/video using relative paths like `assets/hero.mp4`, so if you move `index.html` you must bring the `assets` folder along with it, in the same location relative to the HTML file.

## How to view it

Just open `index.html` in a browser (double-click it, or right-click → Open With → your browser). No build step, server, or internet connection required — it also works offline except for the Google Fonts, which need internet to load (the page still works fine without them, just with fallback fonts).

## How to publish it

Any static host works since it's plain HTML/CSS/JS:
- **Netlify / Vercel** — drag the whole folder (`index.html` + `assets`) into their dashboard.
- **GitHub Pages** — push the folder to a repo and enable Pages.
- **Squarespace/Wix, etc.** — these usually don't accept raw HTML uploads directly; you'd want to rebuild the design in their editor, or use a plain static host like the ones above and point a custom domain at it.

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
