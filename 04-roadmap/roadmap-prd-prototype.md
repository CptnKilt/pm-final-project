# Feature Roadmap, Module 4 · StreamLine Spotlight

**Team:** 2 engineers + 1 designer

## Strategic anchors
- **Persona:** The Stranded Devotee: A heavy, long-tenured viewer who knows film well and still opens the app often, but increasingly leaves without watching anything.
- **Primary metric:** Primary success metric: the share of sessions that reach a 30+ minute watch  Current: 11% Six months ago: 19% Target direction: back toward the 19% baseline, measured for Spotlight-exposed versus non-exposed users (Snapshot 1)  Why this is the right leading indicator:  It covers both leaks in one number. A session only counts if the viewer chose something (browse → play) and stayed with it (play → 30+ min). That covers Priya's scroll-and-leave and the drop-off after pressing play. It's hard to inflate. Browse-to-play alone could rise from autoplay or accidental taps. A 30+ minute watch means the pick actually fit the viewer's taste. It moves before churn does. Session depth changes week to week. Retention and churn take months to show up in cohort data, so this metric shows whether the gap is closing before the lagging results arrive.  How to read it:  Segment it by tenure and user segment, not only in aggregate. That's how you answer the open question about whether Devotees benefit or only Wanderers and new users do. Pair it with two supporting metrics: browse→play conversion (currently 29%), to locate which leak is closing, and the share of viewing that comes from curated content, to confirm that Spotlight is driving the change.
- **Moment of misery:** Priya scrolls for twenty minutes through 15,000 titles, closes the app, and puts on a DVD. Marcus watches one action film and is shown three more action sequels. This is the hook's warning in progress: loyal viewers who haven't left yet but have stopped discovering on the platform.
- **Guardrail:** Guardrail metric: weekly sessions per Power User  Current: 4.8 sessions a week (Snapshot 3) Rule: It must not fall below this baseline for Power Users exposed to Spotlight, compared with those not exposed.  Why this is the right guardrail:  It protects the most valuable, most stable segment. Power Users are 22% of the base, have the highest monthly LTV ($14.20), and already have low churn. The data says they're not the opportunity, so the main risk is harming them by accident. It guards against Spotlight's biggest risk. If curated collections take over homepage space from the algorithmic rows, personal history, and search paths Power Users already rely on, they may visit less often. Their current 58% curated / 22% trending mix works for them, and Spotlight shouldn't disrupt it. It gives early warning. A drop in visit frequency shows up weeks before any change in churn, so problems can be caught while they're still easy to reverse.

## Scoring
| Feature | Value | Effort | Quadrant | Decision | Rationale |
|---|---|---|---|---|---|
| A1 Spotlight Curated Rail | 5 | 2 | Quick Win | Now | It hits Priya's 20-minute scroll head-on by turning 15,000 titles into a short, trusted shortlist. It uses existing homepage rail infrastructure and is the thing the exposed/non-exposed split measures. |
| A2 'Why You'll Love This' Label | 4 | 3 | Major Project | Next | A stated reason is exactly what converts a Devotee from browse to play, and a play made for a reason is more likely to reach 30 minutes. As specced, though, the reasons are AI-generated and appear on hover, and there's no hover on TV, where heavy viewers likely watch. |
| A3 Hidden Gem Badge | 3 | 1 | Fill-In | Later | It speaks to a film-literate viewer tired of the obvious and counters Marcus's sameness problem. But a badge adds a signal without cutting down the choice set, so it won't move the metric alone. |
| A4 Mood-Based Entry Point | 2 | 3 | Time Sinker | Cut | A login gate adds friction for frequent visitors, putting the 4.8 sessions/week guardrail at risk, and it suits Wanderers more than Devotees who know film. It also needs a mood taxonomy for the whole catalog. |
| A5 Personalized Spotlight Queue | 5 | 4 | Major Project | Next | It's the only feature that fixes both Priya's paralysis and Marcus's sequel loop, because it matches on taste rather than genre. New recommendation logic that avoids "more of the same" won't be tuned well in 6 weeks. |
| A6 Spotlight Digest Email | 2 | 2 | Fill-In | Later | Devotees already open the app often. The leak happens inside the session, not in getting them there, so more opens don't fix the metric. |
| A7 Curator Profiles | 3 | 4 | Time Sinker | Cut | Devotees do trust expert taste, but following, profiles, and ongoing editorial work are a platform bet that won't show results in an 8-week pilot. A1 already delivers the curation value. |
| A8 Watch Party (Spotlight) | 1 | 5 | Time Sinker | Cut | Priya's problem is solo discovery, not social viewing. This is Sales-driven and months of sync, chat, and moderation work. |
| A9 Advanced Filter Engine | 5 | 2 | Quick Win | Later | Enables the user to refine their searching to help  them find what they are looking for instead of scrolling the entire catalog or serching for a specific movie title. |
| A10 Offline Download (Spotlight) | 1 | 5 | Time Sinker | Cut | It does nothing about the choice problem, offline viewing may not register as a measurable session, and per-title download rights and DRM make it months of work. |

## Roadmap
### NOW, 3-week sprint
- **A1 Spotlight Curated Rail**, It hits Priya's 20-minute scroll head-on by turning 15,000 titles into a short, trusted shortlist. It uses existing homepage rail infrastructure and is the thing the exposed/non-exposed split measures.

### NEXT, following 1-2 sprints
- **A2 'Why You'll Love This' Label**, A stated reason is exactly what converts a Devotee from browse to play, and a play made for a reason is more likely to reach 30 minutes. As specced, though, the reasons are AI-generated and appear on hover, and there's no hover on TV, where heavy viewers likely watch.
- **A5 Personalized Spotlight Queue**, It's the only feature that fixes both Priya's paralysis and Marcus's sequel loop, because it matches on taste rather than genre. New recommendation logic that avoids "more of the same" won't be tuned well in 6 weeks.

### LATER, backlog
- **A3 Hidden Gem Badge**, It speaks to a film-literate viewer tired of the obvious and counters Marcus's sameness problem. But a badge adds a signal without cutting down the choice set, so it won't move the metric alone.
- **A6 Spotlight Digest Email**, Devotees already open the app often. The leak happens inside the session, not in getting them there, so more opens don't fix the metric.
- **A9 Advanced Filter Engine**, Enables the user to refine their searching to help  them find what they are looking for instead of scrolling the entire catalog or serching for a specific movie title.

### ✂ Cut List
- **A4 Mood-Based Entry Point**, A login gate adds friction for frequent visitors, putting the 4.8 sessions/week guardrail at risk, and it suits Wanderers more than Devotees who know film. It also needs a mood taxonomy for the whole catalog.
- **A7 Curator Profiles**, Devotees do trust expert taste, but following, profiles, and ongoing editorial work are a platform bet that won't show results in an 8-week pilot. A1 already delivers the curation value.
- **A8 Watch Party (Spotlight)**, Priya's problem is solo discovery, not social viewing. This is Sales-driven and months of sync, chat, and moderation work.
- **A10 Offline Download (Spotlight)**, It does nothing about the choice problem, offline viewing may not register as a measurable session, and per-title download rights and DRM make it months of work.
