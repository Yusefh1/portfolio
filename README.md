# Yusef Hamad — Portfolio

Personal portfolio site. Single static page, no build step, no dependencies.

**Live:** https://Yusefh1.github.io/portfolio/

## Files

```
portfolio/
├── index.html            # the entire site (HTML + CSS + JS inline)
├── resume.pdf            # downloadable resume
├── resume-preview.png    # image shown in the Resume section
└── README.md
```

## Deploying to GitHub Pages

1. Create a public repo named `portfolio`
2. Push these files to it
3. On the repo page: **Settings → Pages**
4. Under **Source**, choose **Deploy from a branch**
5. Branch: `main`, folder: `/ (root)` → **Save**
6. Wait about a minute, then open `https://Yusefh1.github.io/portfolio/`

## Updating the resume

Replace `resume.pdf`, then regenerate the preview image so the two stay in sync:

```bash
# macOS — convert the first page of the PDF to PNG
sips -s format png resume.pdf --out resume-preview.png
```

Commit both files and push.

## Editing content

Everything lives in `index.html`. Section order:
hero → about → projects → skills → experience → resume → contact.

Colors and fonts are CSS custom properties at the top of the `<style>` block,
so changing the palette means editing the values under `:root`.

## Adding a photo

The hero currently uses a forecast chart rather than a headshot. To add a photo,
drop `headshot.jpg` into this folder and swap it into the hero grid in place of
the `.chart-card` block.
