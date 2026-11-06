# Os Outtos Ottos

A catalog of famous namesakes for a kid named Otto: 63 Ottos, real and fictional, with search, category filters and a detail page for each one.

The whole site is a single file, `index.html`. No build step and no dependencies (fonts load from Google Fonts, with system fallbacks).

## Run locally

Open `index.html` in a browser. That's it.

## Publish on GitHub Pages

1. Create a public repository (e.g. `outtos-ottos`) and upload `index.html` and this `README.md`.
2. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, branch `main`, folder `/ (root)`, and save.
3. After a minute or two the site is live at `https://<your-username>.github.io/outtos-ottos/`.

## Editing the list

All data lives in the `OTTOS` array inside the `<script>` at the bottom of `index.html`. Each entry looks like this:

```js
{ id: "hahn", name: "Otto Hahn", years: "1879–1968", from: "Alemanha", cat: "cien",
  tag: "One-line summary",
  text: ["First paragraph.", "Second paragraph."],
  fact: "A fun fact.",
  wiki: "Wikipedia search term", yt: "YouTube search term" }
```

- `id`: lowercase letters, digits and hyphens only. It becomes the shareable link (`.../#hahn`).
- `cat`: one of `cien`, `hist`, `arte`, `musi`, `letr`, `espo`, `tela`, `ficc`, `curi`.
- `br: true` marks Brazilian Ottos (used by the "Só do Brasil" filter).

### Optional fields

| Field    | What it does |
|----------|--------------|
| `img`    | Photo shown on the detail page instead of the generated emblem. Either a full URL or a file in the repo, e.g. `img/hahn.jpg`. If the image fails to load, the emblem comes back. |
| `credit` | Credit line under the photo, e.g. `"Foto: Author / CC BY-SA 4.0"`. |
| `source` | Link for the credit (e.g. the Wikimedia Commons file page). |
| `video`  | A YouTube link (`watch?v=`, `youtu.be/` or `shorts/`). It is embedded on the detail page. |
| `site`   | Official website link. |

### Adding photos

Use images you have the right to publish. Wikimedia Commons is a good source: most files there are free to reuse **with attribution**.

1. Open the person's Wikipedia article, click the photo, then **More details** to reach the Commons file page.
2. Download the image into an `img/` folder in the repo (preferred), or copy the direct `upload.wikimedia.org` link.
3. Fill `img`, `credit` (author and license, as listed on the Commons page) and `source` (the Commons page URL).

Avoid images of cartoon or film characters: those are usually copyrighted.
