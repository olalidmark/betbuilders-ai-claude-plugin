# BetBuilders AI for Claude

Model-based football and Swedish ice hockey analysis in Claude. Ask about a match and get BetBuilders AI's win, draw and loss probabilities, expected goals and most likely scores, read the match analysis with each team's xG trend, look up a team's season statistics, or run a what-if simulation in the Monte Carlo match simulator.

The plugin connects Claude to the BetBuilders AI MCP server at `https://www.betbuilders.ai/mcp` and adds two skills that turn the tool results into a match preview and a team form report. It works in Claude chat, Cowork and Claude Code.

## What you can ask

- "What does the model say about Arsenal vs Chelsea this weekend?"
- "Give me an analysis of Frölunda vs Brynäs – form, xG trend and key players."
- "Simulate Färjestad's next game without their starting goalie."
- "How likely is it that Liverpool win and both teams score?"
- "How is Malmö FF doing this season by expected goals?"
- "Show the Allsvenskan table with expected points."

## Coverage

40 football leagues and cups, including the Premier League, La Liga, Bundesliga, Serie A, Ligue 1, Champions League, Europa League, Allsvenskan and Eliteserien, plus SHL and HockeyAllsvenskan in ice hockey. Matches appear once the model has priced them, usually a few days before kick-off.

## What's included

- **MCP server** (`.mcp.json`): the remote BetBuilders AI server over HTTPS. No sign-in and no API key.
- **Tools** (served by the MCP server, all read-only): `find_matches`, `get_match_prediction`, `get_match_analysis`, `get_team_stats`, `simulate_match`, `combination_probability`, `get_league_table`, `search`, `fetch`.
- **Skills:** `match-preview` writes a data-driven preview of one match; `team-form-report` explains how a team is performing and whether its results match its underlying numbers.

## What the plugin sends and where

The plugin runs no local code. Claude calls one remote server, `https://www.betbuilders.ai/mcp`, operated by Football Analytics Sweden AB. Each call sends only the tool arguments: sport, league, team names, match id, date, language and any what-if choices such as a missing player. It does not send your name, email, account details or the rest of the conversation. Every tool only reads data; nothing is created, changed or sent elsewhere. Links in the answers point to betbuilders.ai and carry campaign tags (utm) so we can count visits from Claude.

BetBuilders AI is an analysis service. Probabilities are model estimates, not guarantees. The plugin shows no bookmaker odds and cannot place bets.

## Privacy Policy

See the [BetBuilders AI privacy policy](https://www.betbuilders.ai/integritetspolicy#english). In short: no account is needed, we receive only the tool arguments listed above, technical request logs are kept for operations for at most 30 days, and we never sell personal data. Contact: info@playmaker.ai.

## Support

Documentation and contact: [betbuilders.ai/support](https://www.betbuilders.ai/support#english). Terms of service: [betbuilders.ai/villkor](https://www.betbuilders.ai/villkor#english).

## License

MIT – see [LICENSE](LICENSE).
