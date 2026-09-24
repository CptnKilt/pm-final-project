# Competitive Analysis & Journey Map (Module 2)

## Responses
- **Role, who are you solving for? (the specific user segment or profile):** The Stranded Devotee: A heavy, long-tenured viewer who knows film well and still opens the app often, but increasingly leaves without watching anything.
- **Goal, what is this user ultimately trying to achieve?:** Find something new that fits their taste as a person, not the "more of the same genre" the algorithm offers.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** Priya scrolls for twenty minutes through 15,000 titles, closes the app, and puts on a DVD. Marcus watches one action film and is shown three more action sequels. This is the hook's warning in progress: loyal viewers who haven't left yet but have stopped discovering on the platform.
- **External tools, the outside platforms or tools the user is forced to use:** Physical media they already own. Priya puts on a DVD. It isn't a discovery tool. It's a way to avoid choosing at all.
None documented for Marcus. He says he misses having a human curator but doesn't mention a replacement. Adding one here would be invented.
- **The process, the 3 to 5 manual steps the user takes to get the job done:** 1. Open the app with the intent to watch. Priya has been a heavy viewer for 14 years, so she's still coming back.
2. Browse the home rows. Priya scrolls for about twenty minutes across a catalog of roughly 15,000 titles.
3. Check the personalized row. Marcus finds that "Because you watched" offers three more action sequels after one action film (BUG-1091).
4. Abandon the session. The app closes without anything being watched.
5. Fall back to something familiar outside the app. Priya watches a DVD.
- **Core frustration, the exact moment the process feels most “broken”:** The process feels most broken at step 3 turning into step 4. The personalized row is the one place the platform claims to know this viewer, and it returns more of the same genre. For Marcus, that is the point where the app stops being worth the effort: "I'm not a genre, I'm a person." After that there's nothing left to try, so the session ends.
- **The evidence, a specific quote or behavior from the research that proves this:** Priya (UXR-01): "I open the app, scroll for like twenty minutes, and close it without watching anything… I ended up going back to a DVD."

Marcus (UXR-02): "It recommended three more action sequels because I watched one."

BUG-1091 (High): Recommendations surface near-duplicate titles from the same franchise, and users flag them as repetitive.
- **Your journey map, a shareable link, or the map file you committed (e.g. journey-map.html):** https://github.com/CptnKilt/pm-final-project/blob/main/02-discovery/spotlight-future-state-journey.md
