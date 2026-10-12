<p align="center">
  <a href="https://contender.davishiggins.com"><img src="assets/hero.svg" width="100%" alt="Contender: prop analysis that shows its work. Animated cover with the Contender mark beside an analysis card where the last ten games rise against the line and hit-rate rings fill." /></a>
</p>

<h1 align="center">Contender</h1>

<p align="center"><strong>NBA player-prop analysis that shows its work and keeps its evidence.</strong></p>

<p align="center">
  <a href="https://contender.davishiggins.com"><img src="assets/btn-open.svg" height="44" alt="Open Contender" /></a>&nbsp;
  <a href="https://www.higginsd.com/work/contender"><img src="assets/btn-case.svg" height="44" alt="Case study" /></a>&nbsp;
  <a href="https://davishiggins.com"><img src="assets/btn-dh.svg" height="44" alt="Davis Higgins" /></a>
</p>

<p align="center"><sub>Live product · NBA · Designed and built by Davis Higgins</sub></p>

---

## See it in motion

<p align="center">
  <img src="assets/demo.gif" width="880" alt="Screen recording of the live Contender product page: scrolling to a historical replay for a points prop, then expanding the full game-by-game data." />
</p>

<p align="center"><sub>Real capture of the public product page at contender.davishiggins.com. Player photo blurred. <a href="assets/demo.png">Static frame</a></sub></p>

## What it does

- **One prop, every relevant layer.** Pick a player, a scheduled game, and a market, then enter your own line. The projection, margin against the line, recent form, hit rates, matchup context, reasons, and risks all land on one screen.
- **Results that don't drift.** Every saved analysis is a snapshot. Reopen one and you see exactly what Contender said, and historical replays are graded with misses left visible.
- **Parlays without hidden assumptions.** Build two- to four-leg parlays, see a combined view of the legs, and get flagged when legs depend on each other or contradict one another.

## Why I built it

Most prop tools hand over a pick and hide everything behind it. A bare number can't be checked, and when it misses there's no record of what the tool actually said.

I built Contender as an analysis tool rather than a pick service. Transparency is the product: every number traces to its source, every estimate says what kind of estimate it is, and nothing gets quietly rewritten after the game.

## What I built

I designed and built Contender end to end. It grew out of Propify, my earlier NBA analytics project, into a full rebuild.

- Product and visual design across the marketing site, analyzer, history, and parlay builder
- The data platform that collects and versions NBA schedules and results
- The analysis engine and the services that run it
- Accounts, plans, and billing
- Methodology pages that explain every metric in plain language

<details>
<summary><strong>How it's put together</strong></summary>

<br />

```mermaid
flowchart TB
    U[Player, game,<br/>market, and line] --> W[Contender web app]
    W --> S[Analysis services]
    D[Versioned NBA data] --> S
    S --> R[Finished analysis<br/>saved as a snapshot]
    R --> H[History and parlays]
```

| Decision | Why |
|---|---|
| **Every result is a snapshot** | An analysis is saved exactly as it was produced, along with the data behind it. Old results are never silently recomputed, and a replay can't see games that happened later. |
| **Every number says what it is** | Observed stats, projections, and estimates are labeled differently, so users always know how much weight a number deserves. |
| **Analysis stays on the server** | The browser only shows finished results. Requests are authenticated, and usage is counted fairly even when a connection retries. |

</details>

## Screens

<table>
  <tr>
    <td width="62%"><img src="assets/screenshot-home.png" alt="Contender homepage: 'See the numbers behind every pick' headline beside the Contender logo." /></td>
    <td rowspan="2" width="38%" align="center"><img src="assets/screenshot-mobile.png" width="300" alt="Contender parlay analysis page on a phone: 'Combined probability without hidden assumptions'." /></td>
  </tr>
  <tr>
    <td><img src="assets/screenshot-replay.png" alt="A historical replay: Over 30.5 points with a 36.0 projection and the last ten games charted against the line." /></td>
  </tr>
</table>

<sub>Homepage · Historical replay with evidence (player photo blurred) · Parlay analysis on mobile</sub>

## Technology

| Layer | Technology |
|---|---|
| Web app | Next.js, TypeScript, Tailwind CSS |
| Services | Python |
| Data | Postgres (Supabase) |
| Accounts and billing | Clerk, Stripe |
| Hosting | Vercel |

---

<p align="center">
  <a href="https://contender.davishiggins.com"><img src="assets/btn-open.svg" height="44" alt="Open Contender" /></a>&nbsp;
  <a href="https://github.com/DavisHiggins"><img src="assets/btn-more.svg" height="44" alt="More of my work" /></a>
</p>

<p align="center"><sub>© 2026 Davis Higgins. All rights reserved. Contender and its logo belong to Davis Higgins. NBA team and player names are used descriptively.</sub></p>
