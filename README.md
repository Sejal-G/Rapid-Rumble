# Rapid-Rumble
The repository contains all the source code for the interactive 2-player educational game "Rapid Rumble", which can be played over browser. 

Act as an expert frontend web developer. I want to build a turn-based multiplayer web game inspired by the board game "Rapid Rumble" that I can host for free on GitHub Pages. The game must support 2 players playing together over the internet.

Please write the complete code for this game using a single-file structure (or separated index.html, styles.css, and script.js files) using pure vanilla HTML5, CSS3, and JavaScript. 

To keep the deployment free and simple for GitHub Pages without a complex backend server, use a free public WebRTC signaling broker or a free serverless multiplayer tool (like PeerJS or Supabase Realtime) so two friends can connect via a shared room link.

### Game Mechanics to Include:
1. Room Creation: A player can click "Create Game" which generates a unique room link to send to a friend. The friend opens the link to click "Join Game".
2. Game Deck: 
   - A digital deck of Category Cards (e.g., Animals, Things, Culture, Science, Nature).
   - A digital deck of Letter Cards (A to Z).
3. Gameplay Flow:
   - Each player starts with a hand of 7 random Letter Cards shown on their screen.
   - When a round starts, a Category Card is drawn and displayed to both players.
   - A visual 60-second countdown timer starts.
   - Players must quickly type words that fit the category and start with one of the letters in their hand. 
   - If a player enters a valid word, that Letter Card is discarded from their hand.
   - The first player to get rid of all their Letter Cards (or the player with the fewest cards when the timer hits zero) wins the round.
4. Validation UI: Since automated word/category validation is hard without an advanced AI API, include a "Challenge/Accept" mechanic where the opposing player can see what word was typed and click "Approve" or "Reject" to keep the game honest, just like the real board game.

### Design & UI Requirements:
- Clean, modern, and mobile-friendly card-game layout.
- Use a playful, high-contrast color scheme (e.g., vibrant blues, yellows, and whites).
- Clear typography and smooth CSS transitions for drawing/discarding cards.
- A prominent visual countdown timer that turns red during the last 10 seconds.

Please provide the complete, copy-pasteable code files and brief instructions on how to set up the repository for GitHub Pages.

## GitHub Pages

The game is a static site; no build step or backend setup is required.
The site opens to a game catalogue with **Rapid Rumble** and **Taboo**. Select a game to create a room and invite a friend. Taboo gives each player two 60-second clue turns; the clue-giver sees the secret word and forbidden words, while their opponent accepts a correct guess or rejects it to skip. The player with the most accepted guesses wins. Invite links open the selected game directly; cards marked **Coming soon** are placeholders for future additions.

1. Keep `index.html` in the repository root, then commit and push it to `main`.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
4. Wait for the Pages deployment to finish, then open the published URL. Create a game and share the invite link with your friend; they open it and choose **Join**. Future pushes to `main` trigger another deployment.

Both players need an internet connection and a browser that supports WebRTC. PeerJS provides the signaling service; game data is exchanged peer-to-peer.

