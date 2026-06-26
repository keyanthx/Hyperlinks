# Hyperlinks

An interactive web essay exploring the history, structure, and future of
hyperlinks. By Keyan Thanner.

The whole project is a single self-contained `index.html` (text, images, and
logic are inlined). The only local dependencies are the typefaces in `fonts/`;
`html2canvas` is loaded at runtime from a CDN.

```
.
├── index.html      # the entire site
├── .nojekyll       # tells GitHub Pages to serve files as-is (no Jekyll build)
└── fonts/          # self-hosted typefaces (see fonts/LICENSE.txt)
```

> **Font note:** `fonts/NarkissAsaf-*-TRIAL.otf` are **trial** versions from
> [Fontef](https://fontef.com). Trial licenses usually do not permit public/
> production web use or redistribution. Confirm you hold a license before
> publishing, or remove those two files and the matching `@font-face` blocks in
> `index.html` (the design falls back to Tinos automatically). Tinos and Overpass
> Mono are SIL OFL and free to host.

## Publish on GitHub Pages

1. Create a new, empty repository on [github.com](https://github.com/new)
   (e.g. `hyperlinks`). Don't add a README/license there — this folder has them.

2. From inside this folder, push it up:

   ```bash
   git init
   git add .
   git commit -m "Initial commit: Hyperlinks web essay"
   git branch -M main
   git remote add origin https://github.com/<USER>/<REPO>.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Source: "Deploy from a branch" → Branch:
   `main` / `(root)` → Save.**

4. After ~1 minute the site is live at `https://<USER>.github.io/<REPO>/`.
   (All asset paths are relative, so any repository name works.)

## Test locally first

```bash
python3 -m http.server 8000
# open http://localhost:8000/
```

Use a local server rather than opening the file directly (`file://`) so the
fonts and the html2canvas CDN load the same way they will in production.
