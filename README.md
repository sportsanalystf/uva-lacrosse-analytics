# UVA Women's Lacrosse Analytics — Game Intelligence System

> *Built from scratch in two months by someone who didn't know what lacrosse was.*

---

## The Story

In late 2025, Dean Oliver spoke at [CMSAC](https://www.cmsaconference.com/) and made an offhand observation: lacrosse should have its own dedicated dataset, and more people should be doing serious analysis on the sport. A few weeks later, an opportunity came knocking — a data analytics role supporting **Virginia Athletics Women's Lacrosse**.

I jumped at it. What I didn't know was what I was walking into.

The initial brief: *"Tell us something with the data. Momentum shifts. Impact of each play. Anything useful."*

When I asked where the data lived, I was handed PDFs of season stats and pointed to the NCAA website for play-by-play. No structured database. No tracking data. No established pipeline. I reached out to Zach Cippucci, founder of [Lacrosse Reference](https://www.lacrossereference.com/), to understand how others approach this space.

Two months later, this is what we built.

---

## The System: Three Deliverables

### 1. Opponent Scouting Report + Interactive Dashboard
Pre-game intelligence brief sent 24–48 hours before tip-off:
- Key player profiles with shot maps and assist networks
- Draw control vulnerability analysis
- Pre-game win probability model (feature-weighted logistic regression)
- Swing factor sensitivity analysis
- Specific game plan recommendations for coaches

**March 10, 2026 — Projection sent to coaching staff:**
> *"Virginia 12, Princeton 10. Close game decided by draws and first-half execution."*

### 2. Post-Game Analysis Package
Deep-dive delivered within 18 hours of final whistle:
- Win Probability Added (WPA) charted across every play (189 plays vs Princeton)
- Quarter-by-quarter momentum breakdowns
- Player influence scores
- Offensive/defensive performance grades with rationale
- Film room emphasis plan (5 clips to show, 3 to celebrate, 1 culture moment)

### 3. Player Intelligence Dashboard
Ongoing player performance tracking:
- Draw control trends by quarter
- Shot quality metrics (accuracy, conversion, zone tendencies)
- Impact scoring beyond box score stats
- Substitution and playing time analysis

---

## What Happened vs Princeton (March 11, 2026)

**Final: Virginia 12, Princeton 10** ✅

The prediction held. But it survived a 3-minute window at the end where:
- A Virginia goal was waved off (coach called timeout before)
- Kate Galica hit the post at 1:17 with the game at 11-10
- A free-position shot was stopped by Hughes

We were celebrating not just the win, but the prediction.

**What the scouting report called:**
- ✅ Draw dominance — predicted Galica would dominate Princeton's patchwork draw committee → **Final: 19-3 Virginia**
- ✅ Score early, build a cushion — "Princeton allowed 9-0 and 7-0 runs to start games" → Virginia led 3-2 after Q1
- ✅ Deny Dora's passing lanes — the key defensive priority → Princeton's offense was contained in Q3 (0 goals, 4 shots)
- ✅ Hughes NOT beatable by volume alone — "attack from wings, not top-center" → Virginia's Q3-Q4 ball movement unlocked the game
- ✅ Princeton is a Q4 team — warned about their late-game danger → They scored 4 in Q4, but Virginia answered 5

**What the halftime intervention flagged:**
Down 3-6 after a scoreless Q2, the analysis identified the root cause: Virginia was playing ISO lacrosse, shooting from the top of the arc into Hughes' comfort zone. The recommendation was ball movement, off-ball cuts, wing attacks. Q3: Virginia 4-0. 

---

## Files in This Repository

| File | Description |
|------|-------------|
| `princeton-scouting-dashboard.html` | Pre-game interactive scouting report |
| `UVA_vs_Princeton_Dashboard.html` | Post-game analysis dashboard |
| `Game_Preview_Vs_Princeton.pdf` | Full scouting brief (email) |
| `Post_Game_Vs_Princeton.pdf` | Full post-game analysis (email) |
| `Opponent_Scouting_Report.pdf` | Detailed Princeton opponent report |
| `UVA_vs_Princeton_PostGame_Analysis.md` | Structured post-game notes |
| `Report_Box_Score.pdf` | Official NCAA box score |

---

## Stack & Methods

- **Data sources**: NCAA play-by-play (scraped/parsed), official box scores, public game logs
- **Analysis**: Python (pandas, matplotlib, scipy), R (win probability modeling)
- **Dashboards**: D3.js, vanilla HTML/CSS/JS — single-file, email-attachable
- **Models**: Feature-weighted logistic regression (pre-game WPA), play-by-play WPA tracking
- **Visualization**: Shot maps, assist networks, momentum charts, player influence bars

---

## What's Next

This system needs to evolve beyond box score data. The next phase:

1. **Computer Vision on Hudl footage** — markerless pose estimation, player tracking, zone entry/exit detection
2. **Full analytics app** — coach-facing web application replacing email attachments
3. **Real-time in-game feed** — live WPA updates during games for on-bench decision support
4. **Expected Goals model** — building the xG framework for women's lacrosse that largely doesn't exist yet

---

## Connect

If you're working on lacrosse analytics — at any level, any team — I'd love to connect and learn what you're building.

**Faizan Khan**  
Data Analyst, Virginia Athletics (Baseball, Softball, Women's Lacrosse)  
M.S. Data Science, University of Virginia (Dec 2026)  
[LinkedIn](https://linkedin.com/in/faizankhan) | xdy6sg@virginia.edu

*"Lacrosse should have its own dataset." — Dean Oliver, CMSAC 2025*

---

*Data source: Official NCAA Box Score & Play-by-Play — Princeton at Virginia, 3/11/2026. All analysis prepared by Virginia Athletics Analytics Staff.*
