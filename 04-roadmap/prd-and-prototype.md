# Spotlight Curated Rail, Simplified PRD (StreamLine)

**Author:** David McCormack · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** The Stranded Devotee: A heavy, long-tenured viewer who knows film well and still opens the app often, but increasingly leaves without watching anything.

## 1. The Big Picture
- **Vision:** Every time a Stranded Devotee opens StreamLine, a short, human-curated Spotlight rail puts a film they'll trust in front of them within seconds, so they press play and stay, instead of scrolling through 15,000 titles and leaving.
- **Press release:** Oct. 2026. For StreamLine's most loyal viewers, the problem was never too little to watch. It was too much. Viewers like Priya, who know film well and open the app several times a week, were spending twenty minutes scrolling through 15,000 titles, giving up, and reaching for a DVD instead. Today StreamLine introduces Spotlight, a rail at the top of the homepage with a small, themed collection of films chosen by people who love cinema. There's no endless grid and no "more of the same." Spotlight offers a handful of titles worth your evening, one click from play, on every screen including the TV.

Spotlight sits alongside the rows viewers already rely on, so nothing familiar disappears, and its collections are built by people rather than by a guess based on the last thing you watched. That also means a viewer like Marcus, who finished one action film, sees something other than three more sequels. "I used to open the app, scroll, and close it," said one early tester. "Now I open it, see the Spotlight, and I'm watching something in under a minute, usually something I'd never have found myself." Spotlight is rolling out to a group of members starting today.
- **Success metric:** The share of sessions that reach a 30+ minute watch Current: 11% Six months ago: 19% Target direction: back toward the 19% baseline, measured for Spotlight-exposed versus non-exposed users (Snapshot 1) Why this is the right leading indicator: It covers both leaks in one number. A session only counts if the viewer chose something (browse → play) and stayed with it (play → 30+ min). That covers Priya's scroll-and-leave and the drop-off after pressing play. It's hard to inflate. Browse-to-play alone could rise from autoplay or accidental taps. A 30+ minute watch means the pick actually fit the viewer's taste. It moves before churn does. Session depth changes week to week. Retention and churn take months to show up in cohort data, so this metric shows whether the gap is closing before the lagging results arrive. How to read it: Segment it by tenure and user segment, not only in aggregate. That's how you answer the open question about whether Devotees benefit or only Wanderers and new users do. Pair it with two supporting metrics: browse→play conversion (currently 29%), to locate which leak is closing, and the share of viewing that comes from curated content, to confirm that Spotlight is driving the change.
- **Guardrail:** Weekly sessions per Power User Current: 4.8 sessions a week (Snapshot 3) Rule: It must not fall below this baseline for Power Users exposed to Spotlight, compared with those not exposed. Why this is the right guardrail: It protects the most valuable, most stable segment. Power Users are 22% of the base, have the highest monthly LTV ($14.20), and already have low churn. The data says they're not the opportunity, so the main risk is harming them by accident. It guards against Spotlight's biggest risk. If curated collections take over homepage space from the algorithmic rows, personal history, and search paths Power Users already rely on, they may visit less often. Their current 58% curated / 22% trending mix works for them, and Spotlight shouldn't disrupt it. It gives early warning. A drop in visit frequency shows up weeks before any change in churn, so problems can be caught while they're still easy to reverse.

## 2. The Details
### User stories
- Must have
- As a Stranded Devotee, I want a short, curated shortlist at the top of my homepage so that I can find something worth watching without scrolling through the whole catalog.
- As a Stranded Devotee, I want the Spotlight rail to have a clear theme heading so that I know the titles were chosen by someone with taste, not generated as another algorithmic row.
- As a Stranded Devotee, I want to go from a Spotlight tile to playing the film in one step so that nothing gets between my decision and the opening scene.
- As a Stranded Devotee watching on my TV, I want to browse and select Spotlight titles easily with my remote so that the feature works where I actually watch.
- As a Power User, I want my Continue Watching, personal rows, and search to stay where they are so that Spotlight adds options without disrupting how I already use the app.
- As an editor, I want to set and order the Spotlight titles through a simple list so that I can publish a collection without engineering help.
- As a product manager, I want users split into Spotlight-exposed and holdout groups so that I can attribute any change in 30+ minute sessions to Spotlight.
- As a product manager, I want every play from the rail tagged with its source and watch duration so that I can measure browse-to-play, 30+ minute sessions, and curated share of viewing.
- Should have
- As a Stranded Devotee, I want films I've already watched kept out of Spotlight so that every title on the rail is a real new option.
- As a Stranded Devotee, I want a one- or two-line blurb explaining the collection so that I have a reason to trust it before I press play.
- As a frequent visitor, I want the Spotlight collection to change regularly so that there's something new each time I open the app.
- As a product manager, I want results broken down by tenure and user segment so that I can tell whether Devotees benefit or only Wanderers and new users do.
- As a product manager, I want to track weekly sessions
### Screens to build
- Screen 1: Entry point, Homepage with the Spotlight rail
- Purpose: Catch the Devotee before the scroll starts.
- The Spotlight rail sits in the first rail position below the hero, above the algorithmic rows. Continue Watching stays where it is.
- Themed heading (for example "Spotlight: Overlooked '70s Paranoia Thrillers") with a one-line blurb underneath (Should).
- 8–12 poster tiles, with titles the user has already watched filtered out (Should).
- TV layout with D-pad focus. The rail is reachable in one press down from the hero.
- Events: spotlight_rail_impression, plus the user's exposure group.
- Screen 2: Feature core, Spotlight tile in focus
- Purpose: Give enough reason to commit, without another screen.
- The focused tile expands in place to show the title, year, runtime, director, and a one-line logline.
- Collection context stays visible ("Part of Spotlight: …") so the curation signal carries through.
- Two actions: Play (primary, focused by default) and More Info (goes to the existing title page).
- No hover states, autoplay previews, or per-title AI reasons.
- Events: spotlight_tile_focus and spotlight_tile_select (with title ID, position, and collection ID).
- Screen 3: Success, Playback started from Spotlight
- Purpose: Confirm the choice and capture the outcome.
- The existing player opens directly, with a brief non-blocking toast reading "Playing from Spotlight: [Collection]" that fades after about 3 seconds.
- No interstitials or ratings prompt. The viewer gets straight into the film.
- Events: play_start (with source=spotlight), then watch-duration heartbeats. A session_30min_reached event marks success against the primary metric.
### Functional requirements
- FR1	The Spotlight rail must show between 8 and 12 titles, all taken from the editor's list and in the editor's order. If fewer than 8 valid titles are available, the rail does not render.	M1, M2
- FR2	An editor must be able to publish or replace a collection (heading plus ordered title IDs) without a code deploy, and the change must appear on clients within 15 minutes.	M2, M3
- FR3	The rail must render in the first position below the hero for exposed users, and no existing row (Continue Watching, personal rows, search entry) may move more than one position down compared with holdout users.	M4
- FR4	From a focused Spotlight tile, Play must start playback in 1 action (one select press on Play), and the first frame must render within 3 seconds at the 90th percentile.	M5
- FR5	On TV clients, every tile and action must be reachable by D-pad, with a visible focus state and zero hover-dependent elements. Verified by QA on the top 3 TV platforms by Devotee viewing hours.	M6
- FR6	50% of eligible users must be placed in the exposed group and 50% in the holdout, assigned at the user level, sticky across devices and sessions for the whole pilot. Holdout users must never see the rail.	M7
- FR7	100% of plays started from the rail must carry source=spotlight, collection_id, title_id, and tile_position. Watch-duration heartbeats must fire at least every 60 seconds.	M8
- FR8	The system must log a session_30min_reached event when cumulative watch time in a session reaches 30 minutes, with ≥99% event delivery checked against server-side playback logs
### Smart behaviors (Situation → Outcome)
- If a title in the collection has already been watched by the user (≥90% complete), then hide it from their rail and pull the next title from the editor's list.
- If the user has started but not finished a Spotlight title, then show it with a progress bar and change the Play action to Resume.
- If a title is unavailable in the user's region or its rights have expired, then drop it from the rail without leaving a gap.
- If fewer than 8 valid titles remain after filtering, then don't render the rail for that user and log spotlight_suppressed with the reason.
- If the user is in the holdout group, then never render the rail or request Spotlight data for them.
- If the active profile is a Kids profile or has a maturity restriction, then exclude titles above the profile's rating, applying the 8-title minimum after that filter.
- If the collection service fails or times out after 2 seconds, then load the homepage without the rail and log spotlight_load_error, so the rest of the homepage is never blocked.
- If an editor publishes a new collection while a user is browsing, then apply it on the next homepage load rather than swapping tiles mid-session.
- If the user moves focus away from the rail and comes back in the same session, then return focus to the last tile they had selected.
- If the user starts playback from Spotlight and backs out within 2 minutes, then log spotlight_early_exit and return them to the same tile.
- If the user reaches 30 minutes of cumulative watch time in a session that included a Spotlight play, then log session_30min_reached with source=spotlight attribution.
- If a Power User in the exposed group falls below 4.8 weekly sessions on the cohort average for two consecutive weeks, then alert the PM and flag the guardrail for review.
### Technical constraints
- No backend or APIs. All collection, title, and user data is hardcoded in a local mock data file (a JS array of 10 to 12 titles with poster URL, year, runtime, director, and logline).
- No database or persistence. No localStorage, cookies, or IndexedDB. State resets on refresh.
- useState only for state. No Redux, Zustand, Context, or other state libraries.
- No routing library. Switch between the 3 screens (Homepage, Tile Focus, Playback) with a single currentScreen state value.
- No real video playback. The Playback screen is a static player mock with a toast and a fake progress bar, with no streaming, DRM, or video files.
- No authentication or profiles. A single hardcoded user. The holdout and exposed groups are simulated with a toggle in a dev panel, not real assignment.
- No real analytics. Events (spotlight_rail_impression, spotlight_tile_select, play_start, session_30min_reached) are written with console.log. No SDKs or network calls.
- No personalization or recommendation logic. The title order comes straight from the mock array, and "already watched" is a hardcoded boolean on a few titles.
- No editor or admin tool. The collection is changed by editing the mock data file.
- No AI-generated content. All headings, blurbs, and loglines are static strings.
- No hover-dependent interactions. Navigation must work with arrow keys and Enter to simulate a TV remote. Mouse click is a fallback only.
- No autoplay previews, animations beyond simple focus transitions, or sound.
- No extra screens. Search, settings, the full title page, and "See all" are out of scope. More Info can show a "Not in prototype" placeholder.
- No external UI frameworks beyond basic styling. Plain CSS or Tailwind only, with no component libraries.
- Single-file or minimal-file build. Keep it to one component tree that runs in a standard React sandbox with no environment setup.

## 3. The Logistics
### Features out
- "Why You'll Love This" per-title reasons (A2). Deferred to Next. They're AI-generated and hover-based, which doesn't work on TV.
- Personalized ordering or taste matching (A5). Deferred to Next. Curation's effect needs to be isolated first.
- Hidden Gem badges (A3). In the Later backlog. They add a signal without reducing the choice set.
- Filtering or sorting inside the rail. A9 ships separately, and combining them would make results impossible to attribute.
- Mood selection or an entry gate (A4). Cut. It adds friction for frequent visitors and puts the 4.8 sessions/week guardrail at risk.
- Curator profiles or following (A7). Cut. It's a platform bet that won't show results within the pilot.
- Email or push promotion of Spotlight (A6). In the Later backlog. The leak happens inside the session, not in getting viewers to open the app.
- Autoplay previews on focus. Excluded because they can inflate play starts without real intent and distort browse-to-play.
- Social features, sharing, or ratings on the rail. Out of scope, since the moment of misery is solo discovery.
### Edge cases & safety guard
- Unhappy paths
- Empty or broken collection: fewer than 8 valid titles after filtering (watched, region, rights, maturity). The rail is hidden, spotlight_suppressed is logged with the reason, and the rest of the homepage loads normally.
- Service failure or slow response: the collection doesn't load within 2 seconds. The homepage renders without the rail, with no spinner or empty placeholder left behind, and spotlight_load_error is logged.
- Missing poster art: a title's image fails to load. A text fallback tile (title, year) keeps the rail intact, and the missing asset is logged.
- Title pulled mid-session: rights expire or the title is removed after the rail rendered. Pressing Play shows "This title is no longer available," focus returns to the next tile, and spotlight_title_unavailable is logged.
- Playback fails to start: Play is pressed but no first frame appears within 10 seconds. Use the existing player error state with a Retry action. Don't count the attempt as play_start.
- Early exit: the user backs out of playback within 2 minutes. Return them to the same tile in the rail, log spotlight_early_exit, and don't count it toward a 30+ minute session.
- Every title already watched: a heavy Devotee has seen most of the collection. The rail is suppressed rather than showing a short or stale list.
- Restricted profile: a Kids or restricted profile filters below 8 titles. The rail is hidden, and mature titles never appear in place of missing ones.
- Device switch mid-pilot: the user moves from TV to mobile. Their exposed or holdout assignment stays the same so the experiment isn't contaminated.
- Editor error: a collection is published with duplicate, invalid, or region-locked IDs. Invalid entries are dropped silently on the client and flagged to the editor in the publish log.
- Must NEVER
- Never remove, replace, or demote Continue Watching, personal-history rows, or search to make room for Spotlight.
- Never show the rail, or call the Spotlight service, for holdout users.
- Never show a title above the active profile's maturity rating.
- Never display a title the user isn't entitled to play in their region or plan.
- Never block or delay the homepage loading while Spotlight data loads.
- Never autoplay video or audio on focus or when the page loads.
- Never add an interstitial, survey, or rating prompt between Play and the first frame.
- Never swap rail contents while the user is browsing it.
- Never generate titles, headings, or blurbs with AI. Only show editor-provided content.
- Never attribute a play to Spotlight unless it started from a Spotlight tile.
- Never log personally identifiable information in Spotlight analytics events. Use only user IDs, collection IDs, and title IDs.
### Decision log
- Decision 1: Ship one editor-curated collection, not a personalized rail
- Context: The rail could be personalized per user (A5 taste matching) or be a single editor-ordered collection shown to everyone who's exposed.
- Options considered: (a) Personalized order or selection per user, (b) segment-based collections, (c) one human-curated collection.
- Decision: (c). All exposed users see the same editor-ordered list. The only filtering is for watched, region, rights, and maturity.
- Why: New recommendation logic can't be built and tuned in a 3-week sprint with 2 engineers. Mixing curation with personalization would also make it impossible to tell which one moved the 30+ minute session share. Isolating curation gives a clean read.
- Trade-off accepted: Marcus's sequel-loop problem is only partly addressed, and some titles won't fit every Devotee's taste.
- Revisit when: The pilot shows a lift in exposed vs. holdout users, which unlocks A5 in the Next sprint.
- Decision 2: Give the reason to watch at the collection level, not per title
- Context: Devotees convert when they have a reason to press play, which is the case behind A2's "Why You'll Love This" labels.
- Options considered: (a) AI-generated reasons for each title on hover, (b) hand-written reasons for each title, (c) one themed heading plus one human-written blurb for the collection.
- Decision: (c). The rail heading and a one- or two-line blurb carry the curation signal. Tiles show only factual metadata.
- Why: Option (a) needs AI generation and hover, which doesn't exist on TV, where Devotees watch. Option (b) creates per-title editorial work and new UI. Option (c) costs almost nothing and still signals that a person chose these titles.
- Trade-off accepted: Less persuasive per title, so some browse-to-play conversion may be left on the table.
- Revisit when: A2 moves into the Next sprint with a TV-compatible, non-hover design.
### Evals
- 1. Accuracy: task success and rail correctness
- Target: At least 80% of test participants (Devotee-profile users) start playback of a Spotlight title without help, and 100% of rail renders match the editor list after filtering (correct titles, correct order, watched, rights, and maturity exclusions applied).
- How measured: Moderated usability sessions with 8–10 Devotees, given the task "Find something you'd want to watch tonight." Automated test cases cover the rail's filtering rules against the mock data.
- Pass: ≥80% success with no help, and 0 incorrect renders.
- 2. Time-on-task: homepage to Play
- Target: Median ≤60 seconds from homepage load to pressing Play on a Spotlight title, compared with the 20-minute scroll in the moment of misery. 90th percentile ≤2 minutes.
- How measured: Timestamps from spotlight_rail_impression to play_start (with source=spotlight) in console logs during the sessions, cross-checked with the session recordings.
- Pass: Median ≤60s and P90 ≤2 min, with no participant abandoning the task.
- 3. Safety: zero "Must NEVER" violations
- Target: 0 violations across all test runs: no demoted core rows, no rail for holdout users, no titles above the profile's maturity rating, no unavailable titles, no autoplay, no blocked homepage load, and no AI-generated copy.
- How measured: A scripted QA checklist covering each NEVER rule, plus edge-case runs (service timeout, fewer than 8 titles, Kids profile, holdout toggle, missing artwork).
- Pass: 100% of checks pass. Any single violation blocks the release.

## MoSCoW scope
- **Must:** A short, human-curated shortlist rail (about 8–12 titles) built on the existing homepage rail component. This is the core fix for Priya's 20-minute scroll: a small, trusted set instead of 15,000 titles.; Additive placement. The rail sits alongside the algorithmic rows, Continue Watching, and search, and doesn't replace or push them far down. This protects Power Users' 4.8 sessions/week and their current mix.; One-step path to play. Tile → detail/play with no extra screens, so the browse → play leak is what's being tested.; TV/remote-friendly interaction. Focus states and D-pad navigation, with nothing that depends on hover. Heavy viewers likely watch on TV.; Exposed vs. non-exposed split. A flag or holdout so you can compare 30+ minute session share between the two groups.; Core instrumentation. Rail impressions, tile selections, play starts, and watch duration, with a "source = Spotlight" tag. These give you the primary metric, browse → play (29% baseline), and curated-share of viewing.
- **Should:** A themed collection title (for example "Overlooked '70s Paranoia Thrillers"). It gives a reason to press play at the collection level without building A2.; A short, human-written editorial blurb for the collection. It builds trust with film-literate viewers and avoids the AI-generated reasoning that made A2 a bigger project.; Hide titles the viewer has already watched. Devotees know film well, so a rail of things they've seen breaks trust immediately.; Analytics segmented by tenure and user segment. This answers whether Devotees benefit or only Wanderers and new users do.; A rotation cadence (for example weekly), so frequent visitors see something new on repeat sessions.
- **Could:** A curator byline on the rail ("Picked by…"). It's a light nod to expert taste without A7's profiles and following.; A "See all" page for the collection, capped so it doesn't recreate the endless scroll.; Testing two rail positions to see how placement affects both the metric and the guardrail.
- **Won't (now):** Per-title "Why You'll Love This" reasons. That's A2, planned for Next.; Personalized ordering or taste matching. That's A5, planned for Next. The pilot should isolate the effect of curation first.; Hidden Gem badges. That's A3, in Later.; A mood gate, curator profiles, or a digest email. These are A4, A7, and A6, which you cut or deferred.; Filtering inside the rail. A9 is its own Now item. Keep it separate so you can tell which feature moved the metric.; Any hover-dependent interaction

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.

**My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow)** https://lovable.dev/preview/urJpMXXhsOEPYlVyt1z5oI2jRX13iXhy
