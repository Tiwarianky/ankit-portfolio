# Ankit Tiwari — Portfolio

A single-page developer portfolio for Ankit Tiwari, Java Developer (Spring Boot · REST APIs · MySQL). The design uses a terminal/API theme — a hero styled like a shell session, skills laid out as a schema table, experience as a commit log, and projects as API endpoints — to reflect the backend-developer subject matter.

## Live structure

Everything lives in one file: `index.html` (HTML, CSS, and JS inline, no build step, no dependencies besides Google Fonts).

| Section | ID | What it shows |
|---|---|---|
| Nav | — | Logo, section links, availability status, mobile menu |
| Hero | `#hero` (header) | Terminal-style intro, name, role, links to projects / email / GitHub |
| About | `#about` | Summary + key stats |
| Skills | `#skills` | Tech stack as a schema table |
| Experience | `#experience` | Internship, shown as a commit log |
| Projects | `#projects` | Project write-ups, shown as API endpoints |
| Education | `#education` | Degree + certifications |
| Contact | `#contact` (footer) | Email, phone, location, social links |

## Running it locally

No build tools required. Either:

- Double-click `index.html` to open it directly in a browser, or
- Serve it locally:
  ```bash
  python3 -m http.server 8000
  # then open http://localhost:8000
  ```

## Deploying it

Any static host works since it's a single HTML file:

- **GitHub Pages** — push to a repo, enable Pages on the `main` branch (or a `docs/` folder), done.
- **Netlify / Vercel** — drag-and-drop the file (or connect the repo) for a live URL in seconds.

## Customizing

- **Colors, fonts, spacing** — all defined as CSS variables at the top of the `<style>` block (`--paper`, `--ink`, `--amber`, `--teal`, etc.) — change them once and the whole page updates.
- **Content** — text lives directly in the HTML under each section's `id`; update in place.
- **Adding a resume download** — host `Ankit_Tiwari_Resume.docx` (or a PDF export of it) somewhere public (GitHub repo, Google Drive with link sharing, etc.) and add a link/button in the hero's `.hero-links` block, e.g.:
  ```html
  <a class="btn btn-ghost" href="/resume.pdf" download>Download résumé</a>
  ```

## Browser support

Uses standard CSS (grid, custom properties, `backdrop-filter`) and vanilla JS (`IntersectionObserver` for scroll-reveal, feature-detected). Works in all current major browsers. Reduced-motion preference is respected — animations are disabled automatically for users who have that OS setting on.

## Credits

Fonts: [Inter](https://fonts.google.com/specimen/Inter) and [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts.
