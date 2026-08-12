# My Portfolio Website

A one-page personal portfolio built with plain HTML and CSS only —
no JavaScript, no frameworks, no build step.

## File structure

```
portfolio/
├── index.html          <- all page content (edit text here)
├── styles.css           <- all styling: colors, fonts, layout (one file)
├── assets/
│   ├── profile.jpg      <- YOUR photo goes here (replace this file)
│   ├── cv.pdf            <- YOUR CV PDF goes here (replace this file)
│   └── README.txt        <- notes about the two files above
└── README.md             <- this file
```

How the files connect:
- `index.html` loads the stylesheet via `<link rel="stylesheet" href="styles.css">`
- `index.html` loads Google Fonts and Font Awesome icons via `<link>` tags
  (both are CSS/font files only — no JavaScript involved)
- `index.html` loads your photo via `<img src="assets/profile.jpg">`
- `index.html` links to and previews your CV via `assets/cv.pdf`
  (used twice: once in an `<iframe>` for the on-page preview, once as a
  plain download link)

All paths are **relative** (no leading slash, no domain), so this works
both when you open `index.html` directly on your computer and after
it's published on GitHub Pages.

## How to edit

- **Text (name, bio, hobbies, links):** open `index.html` and change the
  words between the tags. Leave anything inside `< >` alone — just edit
  the visible text and the `href="..."` links.
- **Colors / fonts / spacing:** open `styles.css` and look at the
  `:root { ... }` block at the very top. Every color and font in the
  entire site is a variable there — change it once and it updates
  everywhere. For example, to change the accent color from teal to
  something else, just edit the `--accent` line.
- **Section order:** each section in `index.html` (`#about`, `#hobbies`,
  `#cv`, `#contact`) is a self-contained block — you can reorder, copy,
  or delete them freely, as long as you keep matching links in the navbar
  in sync.

## How to publish with GitHub Pages Like Me

1. Create a new GitHub repository named exactly:
   `yourusername.github.io` (replace `yourusername` with your actual
   GitHub username).
2. Upload these files/folders (`index.html`, `styles.css`, `assets/`)
   to the root of that repository — either by dragging them into the
   GitHub web UI, or with git:
   ```
   git init
   git add .
   git commit -m "Add portfolio site"
   git branch -M main
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```
3. Go to the repo's **Settings → Pages**, and under "Build and
   deployment" make sure the source is set to the `main` branch, root
   folder. (For a repo named `yourusername.github.io`, GitHub Pages is
   usually turned on automatically.)
4. After a minute or two, your site will be live at:
   `https://yourusername.github.io`

## Before you publish, remember to:

- [ ] Replace `assets/profile.jpg` with your real photo
- [ ] Replace `assets/cv.pdf` with your real CV
- [ ] Edit your name, bio, hobbies, and contact links in `index.html`
- [ ] Delete `assets/README.txt` (a note for you, not needed on the live site)
