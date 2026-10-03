---
name: match-preview
description: Write a data-driven preview of an upcoming football or Swedish ice hockey match using BetBuilders AI's model probabilities, xG form and team statistics. Use when the user asks for a match preview, who is likely to win, or how two teams compare before a game.
---

# Match preview

Build a short, well-sourced preview of one match with the BetBuilders AI tools.

1. **Find the match.** If the user named teams but no match id, call `find_matches` with the sport and the team names. If several matches fit, pick the next scheduled one unless the user gave a date.
2. **Get the forecast.** Call `get_match_prediction` for the match. Note the win/draw/loss probabilities (hockey: after 60 minutes and including overtime), expected goals and the two or three most likely scores.
3. **Get the context.** Call `get_match_analysis` for form (last five, oldest first), the xG trend for each team, table position and the key players.
4. **Write the preview** in the user's language, in this order:
   - one sentence with the model's lean and how strong it is
   - form and xG trend for each team, with the numbers
   - two or three key players or matchups
   - the most likely scores and the expected total goals
   - the betbuilders.ai link from the tool result for the full analysis
5. Describe probabilities as model estimates, not certainties. Don't recommend stakes or bets.

If the user asks a what-if question ("without their top scorer"), call `simulate_match` with the change and compare the scenario with the baseline instead of guessing.
