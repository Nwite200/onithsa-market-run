# Onithsa Market Run

A three-lane night-street runner for start.ng, built with Three.js.
Your runner is drawn from the player's start.ng character (body, colours, hair, hat, accessory).
Scores go to the start.ng leaderboard for signed-in players.

Controls: arrow keys or A/D to switch lanes, Up/W/Space to jump. On phones, swipe or use the buttons.

## Files
- `index.html` the whole game
- `three.min.js` Three.js r128, shipped locally
- `startng.json` leaderboard stats (score, distance, coins)
- `cover.png` card image, 1600 x 1000

## Publish
1. Create a public GitHub repo and push these files to the root of the default branch.
2. Check it first:
   `curl -s -X POST https://api.start.ng/games/check -H 'content-type: application/json' -d '{"repo_url":"https://github.com/YOU/onithsa-market-run"}'`
3. Publish it:
   `curl -s -X POST https://api.start.ng/games/publish -H 'content-type: application/json' -d '{"repo_url":"https://github.com/YOU/onithsa-market-run","name":"onithsa-market-run"}'`
4. Open the `approve_url` from the reply, sign in to start.ng and approve once.

After that, every push to the branch updates the live game.
