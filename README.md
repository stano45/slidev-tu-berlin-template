# Slidev Template in the TU Berlin Style (unofficial)

> **Unofficial.** This is an independent project, not affiliated with or endorsed by Technische Universität Berlin.
> It contains no TU Berlin logos or official templates. See [NOTICE.md](NOTICE.md).

[Slidev](https://sli.dev) setup modelled on the TU Berlin presentation corporate design (blue-green gradient): TU colours, Arial, a gradient footer with slide numbers, and cover, section and content layouts.

## Start a new presentation

Click **Use this template** on GitHub, or:

```bash
gh repo create my-talk --private --template stano45/slidev-tu-berlin-template --clone
cd my-talk
npm install
npm run dev
```

Then edit `slides.md`: set `title` and `footer` in the first block, then replace the example slides.

## Adding the logo

No logo is included. If you are allowed to use the TU Berlin logo (see [NOTICE.md](NOTICE.md)), get it from TU Berlin and put it in `public/`:

| File                   | Used on                                       |
| ---------------------- | --------------------------------------------- |
| `public/logo.svg`      | Content and section slides (small, top right) |
| `public/logo-long.png` | Cover slide (long version, top right)         |

You can change the paths with `logo` and `logoLong` in the first block of `slides.md`. Missing files are simply not shown.

Keep repositories that contain TU Berlin logo files private.

## Commands

| Command          | What it does                                  |
| ---------------- | --------------------------------------------- |
| `npm run dev`    | Live preview at http://localhost:3030         |
| `npm run build`  | Static site in `dist/` (Netlify/Vercel ready) |
| `npm run export` | `slides-export.pdf` (uses Playwright)         |

Needs Node 22.12 or newer. Before the first export, run `npx playwright install chromium`.

## Layouts

| Layout    | Use                     | Markdown                                                      |
| --------- | ----------------------- | ------------------------------------------------------------- |
| `cover`   | Title slide             | `# Title`, then a subtitle paragraph                          |
| (default) | Title + bullets         | `# Title`, then content (centred below the title)             |
| `split`   | Text left, visual right | `# Title`, `::left::`, `::right::`; ratio via `cols: 3fr 2fr` |
| `section` | Full-gradient divider   | `# Section`, then a one-line description                      |

The `footer` from the first block appears on the cover and at the bottom of every content slide. To hide it on one slide, set `hideFooter: true`.

## Styling helpers (`style.css`)

- `<p class="takeaway">…</p>`: highlighted one-line takeaway
- `<table class="info-table">`: styled table; with `layout: split`, also set `class: table-split`
- `<div class="stat-grid">` + `<div class="stat-card"><div class="number">…</div><div class="label">…</div></div>`: KPI cards
- CSS variables: `--tu-rot`, `--tu-blau`, `--tu-gruen`, `--tu-dunkelgrau`, `--tu-hellgrau`

## Files

- `layouts/`: cover, default, split and section layouts
- `components/ContentFrame.vue`: logo and footer shared by the content layouts
- `components/Logo.vue`: logo image that hides itself when the file is missing
- `public/`: your images (and logo files, if you add them)

## License

The code in this repository is licensed under the [MIT License](LICENSE). This does not cover the TU Berlin name, logo or other TU Berlin material; see [NOTICE.md](NOTICE.md).
