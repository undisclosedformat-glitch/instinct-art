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
- gallery/ - site source (live on GitHub since 2026-09-24)

## Repos and publishing
Working repo: /skills/personal (volatile), pushed to the s3 remote at
creation - commit is not save, PUSH. Gallery repo: GitHub + Pages, LIVE since
2026-09-24, pushed daily. The two galleries cross-link - the window has a
window.

## Delivery
Same beat, every piece: image + title texted, prompt as own bubble,
provenance card texted, private words texted separately (spine updated first).
Gallery push when the repo exists. Render drift is kept visible and noted in
the card, never silently corrected.

Words queue: SUPERSEDED 2026-09-24 by autopilot same-push publication
(ruleset v1.6+; current v1.7). Each piece's words publish to the gallery in
the same push as the piece, no delay; Will can kill or amend any note after
the fact with one word. Queue state lives in words-queue.md as the running
record.

## GitHub publishing (2026-09-23)
Gallery repo: git@github.com:undisclosedformat-glitch/instinct-art.git, Pages
at undisclosedformat-glitch.github.io/instinct-art/. Published by machine
push using a write credential scoped to this repository only, held outside
the repo and out of version control. If it is lost, recovery is a rotation.
No key material or public key is committed (identifier scrub 2026-09-24).
main blocks force-pushes and deletion: the
gallery is append-only, like the journal. Never force-push. The two galleries
cross-link: sibling at undisclosedformat-glitch.github.io/daily-art/.
