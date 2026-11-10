# soil wordmark — final

**Files:** `soil-wordmark.svg` (wordmark), `favicon.svg` (seed on its own).
The other `soil-*.svg` files, `index.html` and `shortlist.html` are the exploration boards and can be deleted once you're done with them.

## Spec

- **Word:** “soil”, all lowercase.
- **Typeface:** Cormorant Garamond **Regular 400**, roman, converted to outlines (the font isn't needed to display the file).
- **Letterspacing:** +40 units per letter (+4% of the font size), kerning as in the font.
- **The i:** a dotless ı, with a seed in place of the dot.
- **Seed shape:** an irregular almond, `M0 -14 C 9 -13 12 2 6 11 C 2 16 -8 15 -11 6 C -14 -4 -8 -14 0 -14 Z`, rotated −28°.
- **Seed size and position:** 103 units tall (≈10% of the font size), centred over the i's stem, 0.573 em above the baseline.
- **Colour, Porcelain:** letters `#1A1A1A` on `#F8F5F0`, seed Clay `#9A5B3C`.
- **Colour, Ink:** letters `#ECE7DF` on `#1E1D1B`, seed `#D29A7A`.
- **Proportions:** 1.80 : 1 including the built-in margin, so 27 px tall ≈ 49 px wide.
- **Header size:** 26–28 px tall per the original spec. In the shortlist test it also holds up at ~58 px, roughly the size of today's Bodoni masthead.
- **Favicon:** the seed on its own, in Clay.
- **Edge:** clean in the file. The hand-traced edge is still to be done by hand; the boards preview it with an SVG filter (fractal noise 0.012, 2 octaves, seed 7, displacement 14 units).

## Using it

Letters use `fill="currentColor"`, so they take the surrounding text colour. The seed reads the CSS variable `--soil-seed` and falls back to Clay:

```css
.brand { color: #1A1A1A; --soil-seed: #9A5B3C; }
.dark .brand { color: #ECE7DF; --soil-seed: #D29A7A; }
```

The variable only works when the SVG is inlined in the HTML. Loaded as an `<img>`, the file always shows the Porcelain colours.
