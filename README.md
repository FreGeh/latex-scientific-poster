# Research poster template

An A0 portrait poster with optional KIT, HLRS, or custom branding.

| File | Purpose |
|---|---|
| `main.tex` | Entry point for the title, authors, brand, and shared layout options. |
| `content.tex` | Poster body, including section order, column weights, accents, and figure placements. |
| `figures.tex` | Editable TikZ figures for the sample poster. |
| `brands/` | Brand profiles, color palettes, and vector logo PDFs. |
| `poster.sty` | Page geometry, typography, branding, and layout commands. |
| `posterscaled.tex` | Optional A1 export from the compiled `main.pdf`. |

## Branding and layout

- Enable `\useposterbrand{kit}`, `\useposterbrand{hlrs}`, or `\useposterbrand{independent}` in `main.tex`. Leaving it commented gives the unbranded layout. Use `brands/independent.tex` as the starting point for a new profile.
- Set shared spacing and heading treatment with `\postersetup` in `main.tex`. Choose section accents in `content.tex`. Callouts inherit the current accent unless given a color.
- Each `posterrow` takes one relative weight per column. Use a row inside a section for a shared heading, or place sections inside columns for independent stacks.
