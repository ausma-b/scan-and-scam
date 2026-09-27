# Scan & Scam

A 5-minute classroom game for fraud and cybercrime students. The lecturer projects it on the big screen and drives it; the class calls out the answers.

The scenario: your group is auditing the ID scanning technology used in Queensland Safe Night Precincts. Every scan checks a patron's name, date of birth and photo against a database of people with banning orders. The class maps how offenders could target that system, then recommends how to stop them.

**Play it:** [(https://ausma-b.github.io/scan-and-scam/)]

## The three stages

| Stage | What the class does | Time |
| --- | --- | --- |
| 1. What does the scanner log? | Sort 10 data cards into "logged" and "not logged" | 90 s |
| 2. Spin the Threat Wheel | 3 spins, 3 multiple-choice questions each | 2 min 30 s |
| 3. Audit report: prevention | Write a preventative strategy per threat, then copy the report out | 90 s (guide only) |

Maximum score is 190: 100 for the card sort, 90 for the nine questions.

## Presenter keys

| Key | Action |
| --- | --- |
| `Space` | Next / continue |
| `P` | Pause or resume the timer |
| `R` | Restart (press `R` again to confirm) |
| `M` | Sound on or off (off by default) |
| `1`–`4` or `A`–`D` | Answer the question on screen |

Timers never advance the game on their own: when one runs out you get "Time's up!" with a Continue button and an "Add 30 seconds" button.

## Running it

It's one self-contained HTML file. Open `index.html` in Chrome, Edge or Safari, or host it anywhere that serves static files. No build step, no server, no dependencies, no data leaves the browser. The only thing it fetches is the Google Fonts stylesheet; without a connection it falls back to system fonts and everything still works.

Built for a projector at 1920x1080 and scaled to fit whatever screen it's on, so it also works on a laptop.

## Editing the content

Every card, scenario, question, hint, timing and rank sits in one `gameContent` object near the top of the `<script>` block in `index.html`. Change the words there without touching the game logic. Some things you may want to change:

- `timings` — seconds per stage, and how much "Add 30 seconds" adds.
- `stage1.cards` — the 10 cards; `logged: true` puts a card in the answer key for the scanner bin.
- `stage2.scenarios` — the six wheel segments. Each has a title, a story, three questions with four options, the index of the correct option, an explanation, and three hint words for Stage 3.
- `stage2.shuffleOptions` — set to `false` to keep options in the order you wrote them.
- `ranks` — the end-screen titles and the score share each one needs.

## Credits and licence

Artwork is original inline SVG. Every venue name is invented; no real business names or logos appear.

Add a licence here if you want others to reuse it (MIT is the usual choice for teaching material).
