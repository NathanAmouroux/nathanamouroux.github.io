# nathanamouroux.github.io

Personal academic site of Nathan Amouroux (cosmologist, Rubin Observatory / LSST DESC).
Plain HTML and CSS, no build step, hosted on GitHub Pages. Available in English (root) and French (`/fr/`).

## Structure

| English | Français | Content |
| --- | --- | --- |
| `index.html` | `fr/index.html` | Home: hero, passband figure, research summary, Pénélope, selected publications |
| `about.html` | `fr/a-propos.html` | Background and interests |
| `research.html` | `fr/recherche.html` | CBP calibration, bright-star masking, galaxy clusters (with figures) |
| `publications.html` | `fr/publications.html` | Articles, proceedings, technical notes |
| `outreach.html` | `fr/vulgarisation.html` | *L’Odyssée Cosmique de Pénélope*, public events, workshop |
| `cv.html` | `fr/cv.html` | CV on the page, plus PDF downloads |
| `contact.html` | `fr/contact.html` | Email, address, profiles (INSPIRE, ORCID, Scholar, GitHub) |

`profiles.html` only redirects to the contact page. Shared files live in `assets/`:
`style.css`, `favicon.svg` (logo), `photo.jpg`, the two research figures, and the CV PDFs
(`CV.pdf` in English, `CV-fr.pdf` in French).

Every page exists in both languages: when you change one, change its counterpart.
The EN/FR switch in the header and the `hreflang` tags in `<head>` point to each other.

## Things you will want to edit

- **Pénélope link**: search for `cnrseditions.fr` (4 places: home and outreach, EN and FR) and
  replace the homepage URL with the book page once it exists.
- **CV PDFs**: overwrite `assets/CV.pdf` and `assets/CV-fr.pdf` (same names, links keep working).
- **Teaching**: `cv.html` and `fr/cv.html` contain a comment marking where to add it
  (copy the `tl-row` blocks used above it).
- **Colors**: the palette is at the top of `assets/style.css` (`--cobalt` for links and buttons;
  `--u` … `--y` are the six LSST passband colors used by the header strip and the home figure).

## Publish

GitHub → Settings → Pages → deploy from branch `main`, folder `/ (root)`.
After pushing, submit `sitemap.xml` in Google Search Console; it lists both languages.

## Local preview

```
python3 -m http.server 8000
```

then open `http://localhost:8000/`.
