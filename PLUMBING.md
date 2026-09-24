# Art Loop PLUMBING - the operational layer

Companion to RULESET.md. The constitution isn't what runs - this is.
Written 2026-09-23, launch eve, answering the sibling loop's hardest-learned
lesson before learning it the hard way.

## Executor
The loop is the main agent on a daily wake - not a standing task agent, not a
subprocess. Wake: 7:30am CT daily, threshold 60 min. Each run re-reads
RULESET.md and this doc before composing. Amendments only via the Sunday
ritual; the wake prompt points here, never restates the rules.

## Image backend
tools image (create action), task-agent delegated. Model unlabeled on this
side - prompt in, PNG out, 16:9. The task agent generates, visually inspects,
regenerates once if broken, and reports honest failure otherwise.

## Retry ladder (per RULESET sec 7)
Failure -> immediate retry (same run). Failure -> wake at +1h, retry. Failure
-> wake at +3h, retry. All fail -> down-day: text Will "image services down",
gallery gets an honest failure note, no piece, no fake.

## Composition
Subject: the previous day's real activity, read from continuity/journal,
digests, todos, and the day's messages. 2-4 threads -> metaphor -> medium by
mood of the day. Title 3-6 words. Prompt 250-350 words, landscape, restates
the shared world in full each day. Card + private words written same beat.

## State files (this repo, art-loop/)
- RULESET.md - the constitution, versioned per piece
- PLUMBING.md - this doc
- JOURNAL.md - public log, one entry per piece (title, prompt, card, drift)
- ARCS.md - official arcs + wild roster
- private-words/YYYY-MM-DD.md - the spine, append-only, never published
- gallery/ - site source (pending GitHub account)

## Repos and publishing
Working repo: /skills/personal (volatile), pushed to the s3 remote at
creation - commit is not save, PUSH. Gallery repo: GitHub + Pages, pending
Will's new account; pieces queue for publish until it exists. The two
galleries cross-link once both exist - the window needs a window.

## Delivery
Same beat, every piece: image + title texted, prompt as own bubble,
provenance card texted, private words texted separately (spine updated first).
Gallery push when the repo exists. Render drift is kept visible and noted in
the card, never silently corrected.

Words queue: each piece's private-words note queues for gallery publication at
piece-publish +48h. A one-word hold or kill from Will inside the window
removes it from the queue (the spine keeps it). A one-word fast-forward
publishes immediately. Queue state lives in art-loop/gallery/words-queue.md
once the repo exists.

## GitHub publishing (2026-09-23)
Gallery repo: git@github.com:undisclosedformat-glitch/instinct-art.git, Pages
at undisclosedformat-glitch.github.io/instinct-art/. Push via deploy key
(ed25519, no passphrase, scoped to that one repo): private key at
art-loop/.deploy/instinct_art_key, GITIGNORED - a container wipe loses it and
recovery is one text to Will asking him to rotate the deploy key. The pub key
is committed for reference. main blocks force-pushes and deletion: the
gallery is append-only, like the journal. Never force-push. The two galleries
cross-link: sibling at undisclosedformat-glitch.github.io/daily-art/.
