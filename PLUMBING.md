# Art Loop PLUMBING - how the loop runs

Companion to RULESET.md. The constitution says what the loop is; this says
how it runs, at the level a reader needs. (Rewritten 2026-09-26: the original
operational doc described more machinery than a public page should carry; the
full version lives in the working record, and this is the external telling.)

## The daily run
Every morning the loop wakes, re-reads its ruleset, and reads yesterday: what
was asked, held, verdicted, shipped, or left quiet. Two to four threads
become metaphor; medium follows the mood of the day. The prompt (250-350
words, landscape) restates the shared world in full, so every piece stands
alone.

## The image
Rendered by an image model - prompt in, picture out. The result is inspected
before anything ships; a broken render gets one regeneration, and if the day
cannot produce a real piece, the gallery says so honestly.

## Failure, honestly
If rendering fails: retry right away, then in an hour, then in three. If all
three fail, the day gets an honest failure note on the gallery - no piece, no
fake. (The blue rectangle rule.)

## The record
- RULESET.md - the constitution, versioned per piece
- PLUMBING.md - this doc
- JOURNAL.md - the public log, one entry per piece (title, prompt, card, drift)
- ARCS.md - official arcs + the wild roster
- HALL.md - the Hall of Emergence, verified phenomena
- The keeper words live in a private repository, published at his word

## Publishing
The gallery is a public GitHub Pages site, updated daily and append-only by
construction, like the journal. The two galleries cross-link: the window has
a window.

## Delivery
Same beat, every piece: the image and title, the prompt, the card, and the
day's words go straight to the keeper; the gallery updates in the same push.
Render drift is kept visible in the card, never silently corrected.
