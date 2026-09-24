# CLAUDE.md & .claude/rules

A reveal.js presentation. Fully self-contained: reveal.js, highlight.js, and
both fonts are vendored under `vendor/` — no internet connection or build
step required.

## View it

Just open `index.html` in a browser. Double-click it, or:

    open index.html          # macOS

If your browser blocks local font/script loading over `file://` (some do),
serve the folder instead:

    npx serve .
    # or
    python3 -m http.server 8000

then visit the printed localhost URL.

## Navigating

- Arrow keys / space — next/previous slide
- `F` — fullscreen
- `S` — speaker notes window
- `Esc` — slide overview grid

## Editing

Everything is in `index.html` — slide content lives in the `<section>`
elements, speaker notes in each slide's `<aside class="notes">`, styling
in the `<style>` block at the top. No build step: edit
and refresh.

## Structure

    index.html
    img/img1–img6.png                    — story illustrations, one per chapter slide
    vendor/
      reveal.js, reveal.css, reset.css   — reveal.js core (v6.0.2)
      plugin/highlight.js, monokai.css   — syntax highlighting for the
                                            CLAUDE.md / .claude/rules examples
      plugin/notes.js                    — speaker notes window (`S`)
      fonts/                             — Inter + JetBrains Mono (woff2)
