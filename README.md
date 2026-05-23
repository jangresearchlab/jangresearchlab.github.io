# Jang Lab Website

Source code for the [Jang Lab website](https://jangresearchlab.github.io), hosted on GitHub Pages.

## Overview

This is a single-file static website (`index.html`) with no dependencies on Jekyll, Ruby, or any build tools. All four pages (Home, Research, People, Publications) are rendered client-side via vanilla HTML, CSS, and JavaScript.

## Repository Structure

```
index.html          # The entire website
README.md           # This file
assets/
  img/
    logo.png
    lab_setup.jpg
    photo_AJ.jpg
    publication_preview/
      *.jpeg
  pdf/
    *.pdf
```

## Editing the Website

Everything lives in `index.html`. Common updates:

**Add a publication** — find the relevant year block in the Publications section and copy an existing `<li class="pub-item">` block, updating the title, authors, journal, and links.

**Add a lab member** — in the People section, copy an existing `<div class="member-card">` block. Replace the placeholder silhouette with an `<img>` tag once a photo is available:
```html
<!-- Placeholder (no photo yet) -->
<div class="m-photo-placeholder">...</div>

<!-- Replace with this once you have a photo -->
<img class="m-photo" src="assets/img/photo_NAME.jpg" alt="Full Name" />
```

**Update a member bio** — edit the text inside `<p class="m-bio">...</p>`.

**Update research projects** — find the relevant `<div class="project-card">` block in the Research section.

## Deployment

Push any changes to the `main` branch. GitHub Pages will serve the updated site automatically within a minute or two. No build step required.

Make sure GitHub Pages is configured to deploy from the **root of the `main` branch** (Settings → Pages → Source).

## Assets

- Images are stored in `assets/img/`
- PDFs are stored in `assets/pdf/`
- Publication preview images are in `assets/img/publication_preview/`

When adding new files, reference them in `index.html` using relative paths (e.g. `assets/img/photo_name.jpg`).
