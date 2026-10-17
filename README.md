# ibwt — site

Public site of ibwt, live at **https://inbloodwetrust.ai**.

Every push to `main` is deployed to production automatically (Vercel). There is no build step: the files in this folder are served as they are.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole site: markup, styles and scripts in one file |
| `og-image.png` | Link-preview cover, 1200×630 |
| `favicon.ico`, `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `site.webmanifest` | Browser and phone icons |

## Rules of the house

- The name is always lowercase: **ibwt**, never IBWT — also in titles and at the start of a sentence. Keep it out of labels that are uppercased by CSS (`.label`).
- Verticals always go in this order: **Pathology → Radiology → Clinics**.
- Design system: violet `#683EF3`, ink `#14121F`, Geist / Geist Mono / Source Serif 4, square corners, structure by lines rather than cards. Colours are tokens in the `:root` block at the top of `index.html`, with a dark-theme copy below it.
- The page must work at phone width (about 375 px) without horizontal scrolling.

## Contact form

The form in `#contact` posts from the visitor's browser to FormSubmit, which emails the message to the site owner. The recipient address is base64-encoded in the script on purpose; leave it as it is. FormSubmit refuses server-to-server requests, so the form cannot go through a backend function.

## Preview locally

Open `index.html` in a browser, or run `python3 -m http.server` in this folder and open http://localhost:8000.
