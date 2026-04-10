# OpenYap Command Center

Single-pane-of-glass dashboard for the Webcor Concrete PE team on LACC South Hall (Job #11088.70).

Aggregates live data from every sheet the team tracks:

- **Embeds** — LACC Embed Tracker (Detailed Tracker)
- **Tools** — Tools Tracker (Assets, Transfers, Foremen)
- **ACP Coordination** — ACP Vertical Bar (Table B Locations, Pile Types)
- **Submittals & RFIs** — Submittal/RFI Tracker (RFI Log, Gap Analysis)
- **Concrete Takeoff** — CUP Pour Tracker (Pour Takeoff)
- **Concrete Ordered** — Order Log
- **Live Pours** — embeds the cup-dashboard manager view

Plus:
- **Alfred sidebar** — playful AI assistant (MiniMax M2.7) that knows every loaded sheet and can answer "where do I check X?" with sheet/tab citations
- **Blackjack** — for downtime
- Dark + Light themes

## Stack
- Single-file HTML, no build step
- Tailwind via CDN
- Google gviz JSON for sheet reads (no auth — sheets are public)
- Firebase Realtime DB for live pour state
- MiniMax API for Alfred chat

## Local dev
```
open index.html
```
or serve via any static server:
```
python3 -m http.server -d ~/openyap-cc 8080
```

## Deploy
GitHub Pages from `main` branch root → `https://dyap123.github.io/openyap-cc/`

## Keyboard shortcuts
- `R` — refresh all sheets
- `T` — toggle theme
- `?` or `/` — toggle Alfred
- `B` — toggle blackjack
