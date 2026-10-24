# Glorious Morning Consulting

**Data Analysis · Research · Visualization**

A small independent practice with a big worldview.

---

## Site Structure

```
├── index.html          — Home
├── services.html       — Services
├── work.html           — Selected Work
├── about.html          — About
├── contact.html        — Contact
├── css/style.css       — Main stylesheet (design system)
├── js/main.js          — Minimal JS (nav toggle, active link)
├── assets/images/
│   ├── emblem.svg          — SVG mark (globe + books + sunburst)
│   ├── emblem-sunburst.png — Full engraved emblem with gold sunburst
│   └── emblem-books.png    — Antique globe on stacked books
└── resources/images/   — Source moodboards and reference images
```

## Local Preview

Open any `.html` file directly in a browser, or serve the root directory with a local server:

```bash
# Python (from repo root)
python -m http.server 8000
# Then visit http://localhost:8000
```

## Deployment (GitHub Pages)

1. Push the repository to GitHub.
2. In **Settings → Pages**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. The site will be available at `https://johbry17.github.io/Glorious-Morning-Consulting/`.
4. The `.nojekyll` file in the repo root prevents Jekyll processing.

## Required Configuration Before Launch

The following items need to be supplied or activated by the founder before the site is fully operational:

### 1. Email address (`contact.html`)
Find the comment block marked `PLACEHOLDER` and replace:
```html
<p><em style="color: var(--muted);">[Email address — to be configured]</em></p>
```
with:
```html
<p><a href="mailto:hello@yourdomain.com">hello@yourdomain.com</a></p>
```
Consider using a masked/alias address (e.g., SimpleLogin, Apple Hide My Email, or a custom domain alias).

### 2. Formspree endpoint (`contact.html`)
Find the comment block marked `FORM ACTIVATION INSTRUCTIONS` and:
1. Create a free form at [formspree.io](https://formspree.io)
2. Replace `YOUR_FORM_ID` in the form's `action` attribute
3. Remove the `<div class="form-notice">` block
4. Remove the `disabled` attribute from the submit button

### 3. Canonical URL / og:url metadata
Once the domain is confirmed, add `<meta property="og:url" content="https://your-domain.com">` to each page's `<head>`.

### 4. Custom domain (optional)
To use a custom domain with GitHub Pages, add a `CNAME` file to the repo root containing your domain name (e.g., `gloriousmorning.consulting`), then configure your DNS accordingly.

## Design System

**Typography:** Playfair Display (display/headlines) + Inter (body) via Google Fonts

**Palette:**
| Token | Hex | Use |
|---|---|---|
| `--navy` | `#11263a` | Primary dark, nav, headings |
| `--teal` | `#44697a` | Links, labels, secondary accents |
| `--sage` | `#5c6e43` | Geospatial/nature tag |
| `--gold` | `#cf9d47` | Sunburst, decorative accents |
| `--terracotta` | `#a55935` | CTA buttons |
| `--cream` | `#dbcfb9` | Borders, subtle backgrounds |
| `--parchment` | `#f5f0e8` | Section backgrounds |

**Brand character:** Scholarly, worldly, competence-first. Personality in the margins.

## Notes

- No tracking scripts, analytics, or third-party services (except Google Fonts CDN and Formspree when activated).
- All project links point to real live URLs; verify them before launch.
- The emblem PNG images are large — consider compressing them with a tool like [Squoosh](https://squoosh.app/) before launch.
- "Consultations available in the afternoon, by appointment." is a real branding quirk, not a service claim.

