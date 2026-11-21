# Research poster template

An A0 portrait poster with optional KIT, HLRS, or custom branding. Edit the title and authors in `main.tex` and the poster body in `content.tex`. 

For your own institution, copy [brands/template.tex](brands/template.tex), update the logo, affiliation, website, and palette, then select the new profile by filename in `main.tex`.

<a href="template-preview.png">
  <img src="template-preview.png" alt="A0 sample poster using the custom brand template" width="540">
</a>

| File | Purpose |
|---|---|
| `main.tex` | Entry point for the title, authors, brand, and shared layout options. |
| `content.tex` | Poster body, including section order, column weights, accents, and figure placements. |
| `figures.tex` | Editable TikZ figures for the sample poster. |
| `brands/` | Brand profiles, color palettes, and vector logo PDFs. |
| `poster.sty` | Page geometry, typography, branding, and layout commands. |
| `posterscaled.tex` | Optional A1 export from the compiled `main.pdf`. |

## Branding and layout

- Enable `\useposterbrand{kit}`, `\useposterbrand{hlrs}`, or `\useposterbrand{your-institute}` in `main.tex`. Leaving it commented gives the unbranded layout.
- Set shared spacing and heading treatment with `\postersetup` in `main.tex`. Choose section accents in `content.tex`. Callouts inherit the current accent unless given a color.
- Each `posterrow` takes one relative weight per column. Use a row inside a section for a shared heading, or place sections inside columns for independent stacks.

Font overrides belong in the brand profile. HLRS selects Overpass when it is installed and the poster is built with LuaLaTeX (`latexmk -lualatex main.tex`) or XeLaTeX. pdfLaTeX uses the base font.

## License and credits

The LaTeX code, original sample figures, and generic text wordmark are available under the [MIT License](LICENSE). 

KIT's research posters inspired the layout. [KIT poster templates](https://kit-cd.km.kit.edu/latex.php)

The KIT and HLRS logos remain subject to their respective owners’ rights. This project is independent of both institutions.
