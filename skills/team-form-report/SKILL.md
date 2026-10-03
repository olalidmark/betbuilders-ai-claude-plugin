---
name: team-form-report
description: Summarise how a football or Swedish ice hockey team is performing this season using BetBuilders AI's team statistics, xG trend, league ranks and recent results. Use when the user asks how a team is doing, whether its results are sustainable, or how it compares with the rest of the league.
---

# Team form report

Explain a team's season with numbers from the BetBuilders AI tools.

1. **Get the team.** Call `get_team_stats` with the sport and team name. Add `league` if the name is ambiguous across leagues.
2. **Check over- or under-performance.** Compare points with expected points (`points_minus_expected`) and goals with xG. A large positive gap suggests results above the underlying numbers; a large negative gap the opposite.
3. **Read the trend.** Use the xG form curve and its trend direction (rising, falling or stable) over the last matches, and the last-five form (listed oldest first).
4. **Place it in the league.** Use the league ranks for xG, xGA and xGD. Call `get_league_table` if the user wants the full table.
5. **Write the report** in the user's language: a one-line verdict, the numbers behind it, key players, the next match, and the betbuilders.ai team page link from the tool result.

Present all numbers as model and data estimates. Don't recommend bets.
