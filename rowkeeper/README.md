# Rowkeeper

A private crochet pattern library. You add a pattern — a PDF, screenshots of an Instagram
carousel, a video clip, or pasted text — and it comes back as a checklist in US crochet
terms, one line per row or round, that you cross off as you work.

Nothing is public. There are no feeds, forums or sharing.

## What it does

- **Takes patterns in four ways:** a PDF (including scanned ones, up to 60 pages),
  up to 60 screenshots or photos in order, a video clip plus its captions, or pasted text.
- **Multi-slide posts:** every slide of an Instagram carousel can be added at once and put
  in order. Long posts are read in batches and joined into one pattern, with no repeated rows.
- **US terms:** UK and Australian patterns are converted (UK dc → sc, UK tr → dc, and so on),
  and the pattern says what was converted.
- **Row by row:** ranges like "Rnds 5–9" are split into separate lines so each can be
  crossed off. Stitch counts stay with their row.
- **Amigurumi steps:** stuffing, safety eyes, embroidery, sewing and finishing get their own
  lines, in the order the pattern does them. Short pieces made twice are written out twice
  ("Ear (1 of 2)"), and joining pieces goes in an Assembly section.
- **Materials and credit:** every pattern has a Materials section (hook, yarn, gauge, size,
  notions) and a Pattern credit section (designer, handle, shop, link, copyright notice).
  Both can be edited by hand when the source didn't say.
- **Abbreviations:** the ones used in the pattern, with meanings filled in from a standard
  US list, plus the rest of the common list for reference.
- **While you crochet:** a marker for the row you're on, "Go to my row", "Keep screen on",
  "Explain this row" for a confusing step, and "Fix wording" to correct a line.

## How it runs today

Rowkeeper is one HTML file: [`app/rowkeeper.html`](app/rowkeeper.html). It is published as a
private page on a claude.ai account, which provides the three things the page cannot do on
its own:

| What the page needs | Where it comes from today |
| --- | --- |
| Translating a pattern | Claude, through the page's `sample` capability |
| Storing patterns and progress | The page's private `db` storage, owner-only |
| Keeping the original PDF, photos or video | The page's `assets` storage |

Because of that, **opening this file straight from GitHub or from your desktop will not work
as an app.** With no claude.ai account behind it, it shows the built-in example pattern and
says that saving and translating are unavailable. This repository is a backup of the code
and the starting point for a standalone version.

None of your patterns, uploads or progress live in this repository. They stay in the
private storage of the published page.

## Repository layout

    app/rowkeeper.html   the whole app: markup, styles and code in one file
    docs/roadmap.md      what a standalone version would need
    README.md            this file

## Updating

Replace `app/rowkeeper.html` with the newer file and commit. GitHub keeps every earlier
version, so nothing is lost.

## Credit and copyright

Patterns added to Rowkeeper stay the work of the designers who wrote them. The Pattern
credit section exists to keep each designer's name, handle, shop and copyright notice
attached to their pattern. Rowkeeper is for using patterns you bought or were given
privately — it has no way to share or publish them.
