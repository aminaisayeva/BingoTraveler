# BingoTraveler

Make your own bingo card and share it with friends — a travel buddy and a little bingo moment.

It's a single self-contained `index.html`. No build step, no server, no accounts. Just open the file (or host it anywhere static, e.g. GitHub Pages) and go.

## Two screens

1. **Creator** — fill in a title and the 24 squares (center is a free space), then hit **Create share link**. You get a link to send to friends.
2. **Player** — whoever opens the link enters their name and taps squares as things happen. Five in a row (or a column, or a diagonal) → BINGO 🎉.

## How nothing gets lost across sessions

- **The card lives in the share link.** The title + squares are encoded into the link's `#play=...` part. Open it on any phone or laptop and the card rebuilds itself — there's no database to lose.
- **Each player's progress is saved in their own browser** (`localStorage`), tied to that specific card. Close the tab, come back later, your marked squares and name are still there.
- **The creator's draft auto-saves** locally while you're filling it out, so you won't lose work mid-edit.

> Because progress is per-browser, everyone plays their own copy. There's no shared leaderboard — that would need a backend, which this intentionally avoids to stay simple and accessible.
