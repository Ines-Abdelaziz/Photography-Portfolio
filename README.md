# Travel Photography Portfolio

A single-page photography portfolio site — hero intro, a horizontal draggable carousel per destination (Strasbourg, Paris, Luxembourg, Switzerland, Spain, Cologne), a click-to-enlarge lightbox, and a contact section. No build step, no dependencies — just static HTML/CSS/JS.

## Structure

```
index.html          the whole site (markup, styles, script)
images/<place>/thumb/   grid-size photos (~700px)
images/<place>/full/    lightbox-size photos (~1920px)
```

## Editing photos

Open `index.html` in a text editor and find the `MANIFEST` object near the bottom of the `<script>` tag. Each photo is one line, e.g.:

```
{"name": "strasbourg_014.jpg", "w": 1279, "h": 1920},
```

- **Remove a photo:** delete its line.
- **Reorder photos:** cut/paste lines up or down within a section.
- **Add a photo:** drop the file into both the `thumb/` and `full/` folder for that destination, then add a matching line.

No rebuild needed — just save and refresh.

## Hosting on GitHub Pages

1. Create a new repository on GitHub (public, no README/license needed — this folder already has one).
2. Push this folder's contents to the repo's `main` branch:
   ```
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git branch -M main
   git push -u origin main
   ```
3. On GitHub: go to the repo's **Settings → Pages**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`, then save.
4. Your site will be live in a minute or two at `https://<your-username>.github.io/<repo-name>/`.

## Notes

- All photos are already resized/compressed for web (thumb ~700px, full ~1920px), so the site loads reasonably fast despite the photo count.
- The email in the contact section is `ines.abdelaziz19@gmail.com` — edit it directly in `index.html` if that ever changes.
