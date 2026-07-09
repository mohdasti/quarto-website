# Mohammad Dastgheib — Personal Website

[![Website](https://img.shields.io/badge/Website-mdastgheib.com-e63946?style=flat-square)](https://mdastgheib.com)
[![Built with Quarto](https://img.shields.io/badge/Built%20with-Quarto-4B8BBE?style=flat-square)](https://quarto.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

Academic portfolio site for a PhD Candidate in Cognitive Neuroscience at UC Riverside. The site presents dissertation research on physical effort and perceptual decision-making in aging, adjacent XR/HCI work, case studies, publications, and skills—built with [Quarto](https://quarto.org/) and deployed on Netlify.

**Live site:** [mdastgheib.com](https://mdastgheib.com)

## Features

- **Narrative research page** — Four-stage dissertation arc with paradigm schematic, per-figure takeaways, and a visually distinct appendix lane for adjacent XR/HCI work
- **Skills page** — Methods, modeling, signal processing, and computation tied to the research program (not a generic résumé)
- **Portfolio** — Filterable case studies (dual-task program, XR interaction, surgical monitoring, EEG thesis)
- **Publications** — Peer-reviewed articles, conference presentations, and in-preparation manuscripts
- **35mm film gallery** — Personal photography with an in-page viewer
- **Dark mode** — Theme-aware styling across pages
- **Search, TOC, and lightbox** — Site search, page navigation, and figure lightboxes where enabled
- **Academic profiles** — Google Scholar, ORCID, GitHub, and LinkedIn in the footer

## Built with

- [Quarto](https://quarto.org/) — static site generation from `.qmd` sources
- Custom CSS — `assets/css/` (main, research-skills, photography, publications, index)
- [Netlify](https://www.netlify.com/) — hosting and continuous deployment (`docs/` publish directory)
- Font Awesome and Academicons — icons and academic branding

## Project structure

```
quarto-website/
├── _quarto.yml              # Site config, navbar, theme, analytics
├── _publish.yml             # Netlify publish settings
├── home.qmd                 # Homepage → docs/index.html
├── photography.qmd          # 35mm film + digital edits gallery
├── cv.qmd                   # CV page
├── about/                   # About page
├── research/                # Narrative dissertation research page
├── skills/                  # Methods and technical skills
├── portfolio/               # Case study listing
├── publications/            # Publications hub + article subpages
├── projects/                # Individual case studies and demos
├── assets/css/              # Stylesheets
├── images/                  # Site images (incl. images/research/ figures)
├── photography/             # Film and digital photo assets
├── docs/                    # Rendered site output (deployed to Netlify)
└── CV/                      # CV source files
```

## Getting started

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) (1.4+ recommended)
- Git

Optional: Node.js 14+ if you use the npm scripts or Netlify Quarto plugin locally.

### Local development

```bash
git clone https://github.com/mohdasti/quarto-website.git
cd quarto-website

# Live preview with file watching
npm run dev
# or: quarto preview --watch

# One-off preview
npm run serve

# Full site build → docs/
npm run build
# or: quarto render

# Clean rebuild
npm run clean
```

Render a single page while editing:

```bash
quarto render research/research.qmd
quarto render photography.qmd
```

## Customization

### Site-wide settings

Edit `_quarto.yml` for the navbar, footer, theme (light/dark), Google Analytics, and global HTML format options.

### Styling

| File | Role |
|------|------|
| `assets/css/main.css` | Global layout, navbar, footer, NIH funding band |
| `assets/css/research-skills.css` | Research, Skills, Publications, About |
| `assets/css/photography.css` | Film gallery and in-page viewer |
| `assets/css/index.css` | Homepage hero and metrics |
| `assets/css/publications.css` | Publications listing |

Palette: navy `#1d3557`, blue `#457b9d`, teal `#a8dadc`, accent `#e63946`.

### Content

- Page copy lives in `.qmd` files at the paths listed above
- Add case studies under `projects/` and list them in `portfolio/portfolio.qmd`
- Research figures go in `images/research/` (referenced from `research/research.qmd`)
- Film photos go in `photography/`

### Deployment

- Output directory: `docs/` (configured in `_quarto.yml`)
- Netlify settings in `_publish.yml`
- Pushes to `main` trigger automatic builds when connected to Netlify

## License

MIT — see [LICENSE](LICENSE).

## Author

**Mohammad Dastgheib**

- Website: [mdastgheib.com](https://mdastgheib.com)
- Email: m.dastgheib@gmail.com
- LinkedIn: [linkedin.com/in/mdastgheib](https://linkedin.com/in/mdastgheib)
- GitHub: [github.com/mohdasti](https://github.com/mohdasti)
- Google Scholar: [scholar.google.com/citations?user=SNVpHcUAAAAJ](https://scholar.google.com/citations?user=SNVpHcUAAAAJ)
- ORCID: [0000-0001-7684-3731](https://orcid.org/0000-0001-7684-3731)

## Contributing

Issues and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.
