# Bot in the Room

A multiplayer party game: everyone answers the same prompt, one answer is secretly written by AI (OpenAI). Spot the bot, or get mistaken for it.

- Single static `index.html`, no build step, no server. Host it anywhere (GitHub Pages).
- Multiplayer over WebRTC via PeerJS; the host's browser holds the game state.
- Host can paste an OpenAI API key (kept in their browser only) for a live AI bot; otherwise the bot uses pre-written answers.

Run locally: `python3 -m http.server` in this folder, then open http://localhost:8000.
