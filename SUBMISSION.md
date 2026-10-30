# Handshake submission: Create a Multiplayer Game

**Project title:** Bot in the Room

**Cover image:** `cover.png` (1200×630)

**Project link:** _(the GitHub Pages URL once published)_

**Project description:**

Bot in the Room is a party game you play on your phone, with an AI hiding among the players. Each round, everyone gets the same silly prompt, like "the worst possible name for a pet goldfish," and types a short answer. Meanwhile, OpenAI quietly writes an answer of its own. All the answers appear anonymously, and everyone votes on which one the bot wrote. You get +2 for catching the bot and +1 every time someone mistakes *your* answer for the AI's. Being bot-like is a strategy.

The twist is Sneaky mode. The bot reads what your group wrote in earlier rounds and copies its length, capitalization, punctuation and sense of humor. The longer you play, the harder it is to tell the humans from the machine. A running "Humans vs Bot" score decides who wins overall, and the final screen hands out awards for Best Detective and Most Bot-like Human.

How it works:
- The host opens a room and friends join with a 4-letter code, a QR code or an invite link. Up to 12 players, no sign-up, no app to install.
- It's fully multiplayer in real time over peer-to-peer WebRTC (PeerJS). The host's browser referees the game, so there's no game server to run.
- The bot's answers come from the OpenAI Chat Completions API. The host's key stays in the host's browser and is never sent to other players. Without a key, the bot falls back to pre-written answers so the game always works.
- Edge cases are handled: players who drop and reconnect keep their seat and score, latecomers join at the next round, timers keep the game moving if someone goes quiet, you can't vote for your own answer, names are made unique, the host can remove players, and if OpenAI is slow or errors out, the bot falls back instead of stalling the round.

Built for game nights, video calls and classrooms. It's a fun way to sharpen a skill everyone now needs: telling human writing from AI writing.
