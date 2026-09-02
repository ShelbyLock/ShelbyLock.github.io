# Qianying Liao — personal website

Source for [shelbylock.github.io](https://shelbylock.github.io), built with
[Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme.

## Where the content lives

| What you want to change | File |
| --- | --- |
| Bio, photo, address on the front page | `_pages/about.md` |
| Publications | `_bibliography/papers.bib` |
| News items on the front page | `_news/` (one file per item) |
| Name, site URL, favicon, footer | `_config.yml` |
| Social links (email, Scholar, LinkedIn, GitHub) | `_data/socials.yml` |
| Venue badge colours and links | `_data/venues.yml` |
| CV contents | `_data/cv.yml` |

Your profile photo is `assets/img/prof_pic.jpg` — replace the placeholder with a real
photo (square, roughly 800×800, JPG).

## Pages that are hidden until you fill them in

`_pages/service.md` and `_pages/teaching.md` have `nav: false` in their front matter, so
they are built but not shown in the navbar. Add your content and flip that to `nav: true`
to make them appear.

## Adding a publication

Append a BibTeX entry to `_bibliography/papers.bib`. Useful extra fields:

- `abbr` — the venue badge shown on the left (add a colour for it in `_data/venues.yml`)
- `selected = {true}` — also show this paper on the front page
- `abstract`, `arxiv`, `doi`, `html`, `pdf`, `code`, `slides` — render as buttons
- `bibtex_show = {true}` — show the "Bib" button

## Previewing locally

With Docker:

```bash
docker compose up --build
```

Then open <http://localhost:8080>. The site rebuilds when you edit a file.

## Deploying

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site and
pushes the result to the `gh-pages` branch. In the repository's
**Settings → Pages**, set the source to the `gh-pages` branch, root folder.

## Licence

The al-folio theme is MIT licensed — see `LICENSE`. Site content © Qianying Liao.
