# Site DNA

What every Codesavory web page shares, so the Lasya studio site, Hearth, Kinema and whatever comes next read as one family while each keeps its own flair. `DESIGN.md` sets the tokens and the voice; this page sets how a page is put together with them. Owner, 27 Oct 2026: "the DNA across all the pages are tied even though they have their own flare".

## What a product may own, and what it may not

| A product owns | Every product shares |
|---|---|
| Its hero media (a render, a reel, a live canvas) | The page skeleton below: header, hero, bands, footer |
| Its mark and wordmark | The type roles and the sizes in this page |
| Its one accent moment (usually the serif flourish) | One accent per page, the same ember in both themes |
| An app layer of extra tokens (`apps/<name>/`) | The footer lines, in order |
| The words | The appearance switch, top right |

Never change the type scale, add a second accent colour, or restructure the footer to get flair. Flair comes from the media, the mark and the words.

## The skeleton

Every public page, in this order:

1. **Header.** Left: the product's mark and wordmark, linking home. Right: the credit to the parent (for a product, "by" plus the studio mark and name, linking to the studio site) and the appearance switch. Nothing else in the header of a landing page; app pages may add their stage tabs in the middle.
2. **Hero.** One headline with at most one serif flourish (`serif`, 400, `accent-text`), one lead line, one primary button (`brand` pill), optionally one quiet text link beside it. Then the hero media.
3. **Bands.** Each section is a band: a mono uppercase eyebrow (`label`), a title (`title-l`), the content, and optionally a `fine` note under it. Bands are separated by space (`space-8` on top), not by rules.
4. **Closing action.** The waitlist, "Start a project" or the next step, once.
5. **Footer.** The lines below.

## Fonts and type roles

| Element | Font and size | Colour |
|---|---|---|
| Product wordmark | `display`, `title-s`, its own weight and tracking | `ink` |
| Studio wordmark (Lasya) | `display` 600, 13px, letter spacing 0.32em, uppercase | `ink` |
| Page headline (h1) | `display-l`; `display-m` under 640px | `ink` |
| The flourish | `serif` 400 inside the headline, once per page | `accent-text` |
| Lead line | `body-l` | `ink-muted` |
| Eyebrow | `data` (mono), `label` size and tracking, uppercase | `ink-subtle` |
| Band title (h2) | `title-l` | `ink` |
| Card or row title | `display` 500 to 600, body size; `title-m` for headline facts | `ink` |
| Body | `body` or `body-s` in cards and rows | `ink-muted` |
| Fine print and method notes | `body-s` | `ink-subtle` |
| Status words (Running, In the works, Planned) | `data`, `label` size, uppercase | `ink-subtle` |
| Measured numbers (scores, timings) | `data-l` with tabular figures | `ink` |
| One countdown or score per screen | `dot` (Doto) | `ink` |

Geist for everything you read, Geist Mono for anything that measures, Instrument Serif only for the one flourish, Doto at most once. Fonts are self-hosted from the generated `tokens.css`.

## Sizing

- **Widths.** Marketing and landing pages use `content-wide`; reading pages (verify, docs, legal) cap at 720px. Running text stays near 65 characters.
- **Spacing.** Band top `space-8`; header padding `space-5`; cards `space-4` to `space-6` inside; gaps in grids `space-3` to `space-5`.
- **Radii.** Buttons, fields and switches are pills. Cards `radius-md`; hero panels and diagrams `radius-lg`; logo tiles `radius-sm`.
- **Icons.** Drawn on a 24 grid, 1.75 to 1.8 stroke, round caps and joins, `currentColor`. 22px in feature rows, 14px in the appearance switch, 44px on platform cards.
- **Logo tiles.** 40px (32px in dense rows) on `gray-0` in both themes, with a hairline, so a third party's colours read as designed.
- **Targets.** 44px for anything you press, except the appearance switch's 26px buttons inside a 32px pill.

## Formats

| Format | Example | Blocks, in order |
|---|---|---|
| Studio site | Lasya | Header with the studio wordmark and label, hero reel, work grid, paths, Info (Studio, Services, Contact), closing line, footer |
| Product landing | Kinema, Hearth | Header, hero with a real export, the experience, proof (measured numbers with the renders or clips behind them), how it connects, the tool or roadmap, the gallery if it exists, closing action, footer |
| Tool | kinema.codesavory.dev/try | App chrome: wordmark, stage tabs, undo and redo; no marketing |
| Interest page | /download | Hero, one card per platform with its own form, the platform that exists today as its own card, a plain note that the others are not built yet |
| Utility page | /verify | Hero, one drop target or form, the result card, a fine note |
| Admin | /admin | A status page (rule 55) |

## The recurring blocks

**The experience.** Five or six rows, each a small line icon, a title and one line. Numbers appear only if they were measured, and a `fine` note says where ("Measured on an Apple M4 in Chrome by the release checks"). Targets are labelled as targets.

**Proof.** A measured number never stands alone: show what produced it (the renders, a difference image) and one line of method. If a figure came from software used under a non-commercial licence, say so in the note and the footer.

**How it connects.** The product in the middle, what feeds it on the left, what it hands on to on the right, joined by hairline brackets. A filled dot is running today, a hollow dot is planned, with a legend line. Third-party marks are official logos on a logo tile, used only to say what the product works with; where a mark's owner forbids that use (Apple, Microsoft), draw a plain icon instead; where there is no logo, use a monogram tile.

**Status words.** Running, In the works, Planned. Never "Coming soon" without one next step (rule 32), and never a placeholder gallery or an invented number.

## About

The studio site carries the About: Lasya's Info block (Studio, Services, Contact) in two or three short facts each. Product pages do not repeat it; they credit the studio in the header and the footer and link to it. A product may add one line about who makes it in the closing section, never a team page or a manifesto.

## Footer

A hairline top, `body-s`, `ink-subtle`, in this order:

1. **Made by.** "<Product> is made by <Lasya Studios>, a Codesavory LLC company." The studio name links to its site. The studio site itself says "Lasya Studios, a Codesavory LLC company."
2. **Utility links**, right aligned on the same line where there is room: desktop apps, verify, contact.
3. **Privacy, as facts.** What is kept and what never leaves the device.
4. **Credits and trademarks.** Software thanks where the work is made with it (Lasya: "Special thanks to SideFX and Houdini ..."), then one line naming every third-party mark on the page and its owner, that logos only show compatibility, and that the product is not affiliated. Any non-commercial licence used for something shown on the page is named here.
5. **© year.**

## Theme

Both themes are designed on every public page. The appearance switch (a sun and a moon in a pill, `surface-sunk` with the active button raised) sits at the far right of the header. A new page follows the system until someone picks, then saves the pick per product (`<product>-theme` in local storage) and sets it before first paint from an inline script in the head. The canvas ground of a render stays dark in both themes.

## Checklist for a new page

- [ ] Header: mark and wordmark left; "by" credit and appearance switch right
- [ ] One headline, at most one flourish, one primary button
- [ ] Bands with mono eyebrows; space, not rules, between them
- [ ] Every number measured, with its method in a fine note
- [ ] Third-party marks on logo tiles, and named in the footer
- [ ] Footer lines 1 to 5, in order
- [ ] Both themes checked, and the phone layout at 390px
- [ ] No em dashes, en dashes or double hyphens anywhere
