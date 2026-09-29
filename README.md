# Word Between Us

A mobile-first, two-player secret-word deduction game built for live remote play in a phone browser.

## What it does
- Create an 8-character room code.
- Share the invite link with another player.
- Each player gets a 9-letter rack and privately locks a 4–9 letter secret word.
- Both start at 12 points.
- Clues cost points; wrong guesses cost 1 point.
- Clue answers are generated automatically from the opponent's locally stored word.
- The round finishes after both players solve; higher remaining score wins.
- Basic local persistence helps recover from accidental reloads/reconnections.

## Fastest way to play
This is a static site: no build step and no server-side code.

### Option A — GitHub Pages
1. Create a new GitHub repository (for example `word-between-us`).
2. Upload `index.html` to the repository root.
3. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`.
4. Open the Pages URL on your phone.
5. Player 1 taps **Create a room**, then **Share invite**.
6. Player 2 opens the invite, enters their name, and taps **Join room**.

### Option B — Netlify Drop
Drag the `word-between-us` folder into Netlify Drop, open the generated HTTPS URL, and share it.

## Important technical note
Live multiplayer uses PeerJS/WebRTC, so the two browsers connect directly. The host should keep the game tab open. Mobile browsers may suspend connections while backgrounded; returning to the tab usually reconnects automatically.

## Privacy
The secret word is held in the player's own browser. The opponent receives only clue answers and guess results during normal play.

## Originality
This is an original implementation inspired by the general category of two-player secret-word deduction games. It does not reproduce another commercial game's card text, artwork, branded terminology, or exact rules.
