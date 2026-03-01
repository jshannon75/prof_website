# Jerry Shannon — Quarto Website

A Quarto website recreating [jerry.shannons.us](http://jerry.shannons.us).

## Requirements

- [R](https://cran.r-project.org/) (>= 4.1) and [RStudio](https://posit.co/download/rstudio-desktop/) (>= 2022.07), **or**
- [Quarto CLI](https://quarto.org/docs/get-started/) standalone (>= 1.3)

No R packages are required unless you add R code chunks. Quarto is bundled with recent versions of RStudio.

## Getting Started

### Option A — RStudio

1. Open `jerry-shannon-quarto.Rproj` in RStudio.
2. Click **Render** (or press Ctrl/Cmd+Shift+K on `index.qmd`) to preview.
3. Use the **Build** tab → **Render Website** to build the full site.

### Option B — Terminal

```bash
# Preview with live reload
quarto preview

# Build for deployment (output goes to _site/)
quarto render
```

## Project Structure

```
jerry-shannon-quarto/
├── _quarto.yml                        # Site config, navbar, theme
├── styles.scss                        # Custom SCSS (colors, fonts)
├── index.qmd                          # Home page (trestles about template)
├── vita.qmd
├── research.qmd
├── teaching-philosophy.qmd
├── courses-ive-taught.qmd
├── links-for-grad-students.qmd
├── personal-links-and-research-tools.qmd
├── side-maps.qmd
├── contact.qmd
└── img/
    └── headshot.jpg                   # ← Add profile photo here
```

## Adding Your Photo

Place a headshot image at `img/headshot.jpg`. It will appear automatically
on the home page via the `trestles` about template.

## Deployment

The rendered `_site/` folder is a standard static website. Deploy it to:

- **Netlify**: drag and drop the `_site/` folder at [netlify.com/drop](https://app.netlify.com/drop)
- **GitHub Pages**: push to a `gh-pages` branch or use `quarto publish gh-pages`
- **Quarto Pub**: run `quarto publish quarto-pub`
- **Posit Connect**: run `quarto publish connect`
