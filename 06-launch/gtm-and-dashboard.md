# GTM Launch Plan, StreamLine (B2C)

| Field | Value |
|---|---|
| Feature | Spotlight Curated Rail |
| Goal | Engagement |
| Launch tier | S, Minimal |

## Goal & Audience
- **Goal:** Engagement, The Stranded Devotee is already a long-tenured, paying subscriber who opens the app often. The problem is that their visits stop producing viewing, and your primary metric (empty-session rate) is a pure engagement measure: are existing users getting value from the sessions they already start?
- **Target audience:** The Stranded Devotee: a heavy, long-tenured viewer who knows film well and opens the app often, but increasingly leaves without watching anything. For targeting, all of these must hold:  Tenure ≥ 12 months. ≥ 4 sessions/week over the prior 8 weeks. Empty-session rate in the top quartile for the base. Empty-session rate up ≥ 10pp versus the 8 weeks before that.

## Launch Tier
- **S, Minimal**, The Spotlight Curated Rail is a single in-product change aimed at existing, long-tenured subscribers, not a new product, pricing change or acquisition push, so there's no external audience to win over. Its first release is a 28-day A/B test limited to one mobile segment, with half of those users seeing the curated version, which calls for in-app placement and internal enablement rather than press, paid media or broad marketing. If the test wins and the rail rolls out to the wider base, a follow-on launch could step up to Medium.

## Channels
1. **Owned: In-app placement**
2. **Owned: In-app messaging**
3. **Owned: Help center + member support**

## Enablement & Assets
What each team needs

Support (frontline agents)

Awareness of the test: some members will see a different Spotlight list from friends or family on another account. Agents need to know this is expected, not a bug.
A neutral answer during the test: "We're testing new homepage features, so rails can differ between accounts." Agents shouldn't volunteer that one arm is human-curated, since that would leak the variant.
Bug triage path: how to spot and escalate real issues (rail missing, fewer than 10 titles, already-watched titles appearing) to the product team, because these directly affect the test's validity checks.
After rollout: a plain explanation of what Spotlight is, how often it refreshes, and why a title disappeared.

CS / member retention

Who the persona is: Stranded Devotees are high-tenure, high-value members drifting toward churn. CS should know Spotlight is the intended fix, so they can point at-risk members to it after rollout.
Readout timing: when results land (28 days plus analysis), so they don't promise anything before the decision.

Internal partners (not customer-facing)

Curator / editorial: the weekly cadence (30 ranked titles, delivered before the Monday refresh), the eligible-title rules, and the no-peeking rule on algorithmic picks.
Data / analytics: the pre-registered metric definitions and readout owner, so the analysis matches the brief.
Assets to build

During the test

Support FAQ and macro: the neutral "testing new features" answer, plus the expected-behavior notes.
Escalation runbook: bug symptoms, how to tag tickets, and who owns fixes.
Internal one-pager: what's being tested, who's in it, the dates, and what not to say externally.
Curator playbook: weekly deadlines, list format and selection rules.

After a winning readout (rollout)

Help center article: "What is Spotlight?" (channel 3)
Updated support macros: a member-facing explanation, now allowed to mention curation if you choose to promote it (channel 3)
In-app coach mark and "New this week" refresh badge: copy and design (channel 2)
CS talking points: how to suggest Spotlight to members showing signs of disengagement, after confirming they aren't in the holdout (channel 3)

## Ownership, Budget & Timeline
- **Ownership & budget:** Product Manager : owns the GTM plan, the experiment brief, the go/no-go decision at readout, and post-launch metrics. No extra budget.
Editorial Curator: owns the weekly 30-title ranked list and the curator playbook. Budget needed: 40 hrs/week × $20/hr = $800/week. Weeks −2 to 12 = 14 weeks = $11,200, approved by VP of Marketing by Week −4. Funding beyond Week 12 is decided at the Week 12 review. If the test is killed at Week 5, spend stops at $5,600 (Weeks −2 to 4). If funding isn't approved by Week −4, the test start moves back week for week.
Engineering Lead: owns the rail build, the segment-wide algorithmic top-30, the already-watched filter and rail-seen event logging. Also owns coach-mark view/dismiss logging and exposing the member's test arm in the support tool. No extra budget; uses existing team capacity.
Data Analyst: owns the eligibility count, segment baseline, sample size recalculation, sample ratio checks and the readout analysis. No extra budget.
Product Designer: owns the rail layout within the existing card template, plus the coach mark and refresh badge design. No extra budget.
Support Operations Lead: owns the support FAQ, macros and escalation runbook, and briefs frontline agents. Also owns tagging support contacts that mention Spotlight. No extra budget.
Member Retention / CS Lead: owns the CS talking points and steering at-risk members toward Spotlight. No extra budget.
Content Writer: owns the help center article and the internal one-pager. No extra budget.

Deferred to the Medium follow-on (gated on a winning Week 12 review): subscriber email and film communities, including building a Letterboxd / subreddit presence.
- **Timeline:** Phase 1: Beta (the A/B test)

Week −4: VP of Marketing approves curator budget; PM confirms curator is hired.

Weeks −2 to 0, pre-launch prep:
Data Analyst: eligibility count, segment baseline, sample size recalculation.
Engineering Lead: build the rail, filter and logging.
Editorial Curator: deliver the first 30-title list.
Support Operations Lead: brief agents on the test FAQ and escalation runbook.
Content Writer: internal one-pager.
Product Manager: go/no-go on test start.

Weeks 1–4, test runs (starts on a Monday, 28 days):
In-app rail only; no email or community promotion.
Editorial Curator: weekly list before each Monday refresh.
Data Analyst: daily sample ratio and rail-rendering checks.

Days 7, 14 and 21: harm check by the Data Analyst. If watch minutes are down more than 5% vs. the comparator, the PM stops the test within 24 hours.

Week 5, readout:
Data Analyst: full analysis against the pre-registered rule.
Product Manager: ship / iterate / kill / inconclusive decision.

Phase 2: Launch moment (only if the test ships)

Week 6, rollout prep:
Content Writer: help center article.
Support Operations Lead: update macros; set up Spotlight contact tagging.
Product Designer: final coach mark and badge copy and design.
Engineering Lead: build and QA coach mark, badge and logging; expose test arm in support tool.
Member Retention / CS Lead: brief CS on talking points and the holdout check.

Week 7, launch:
Engineering Lead: roll the curated rail out to all Stranded Devotees on mobile, keeping a 10% holdout on today's homepage. Coach mark and refresh badge go live with the rail.
Content Writer: publish the help center article.
Support Operations Lead: updated macros go live.

Phase 3: Post-launch

Weeks 8–11, monitor:
Data Analyst: weekly empty-session rate (rail-seen and all sessions), 30+ minute rate and watch minutes, rollout vs. holdout; plus coach-mark dismiss rate and rail-seen sessions following a coach-mark view.
Support Operations Lead: track Spotlight-tagged contacts, complaints and help-article views.

Week 12, post-launch review:
Product Manager: confirm whether the rail beats today's homepage, then decide whether to expand to Casual Browsers and other platforms, which would be a Medium-sized follow-on launch.
Editorial Curator: confirm the curation cadence is sustainable at full scale.

## Success Metrics
- **Metrics:** Comparator: Phase 1 = the algorithmic-rail arm. Phases 2–3 = the 10% holdout. For the holdout, "rail-seen" means slot 2 rendered on screen, whatever occupies it.

Rail-seen empty-session rate (primary): sessions with slot 2 on screen that end with no play or under 2 minutes played. Success: ≥ 2pp lower than the comparator, two-sided p < 0.05. Sample sized for 80% power to detect 2pp.

All-session empty-session rate (guardrail): must improve in the same direction as the primary. If it doesn't, treat the result as cannibalization, not success.

30+ minute session rate: share of rail-seen sessions reaching a 30+ minute watch. Success: lower bound of the 95% CI on the difference ≥ −1pp.

Watch minutes per user (cancelled users count as zero): ≥ −2% (CI lower bound) = eligible to ship. Between −2% and −5% = don't ship; iterate. Below −5% at any weekly check, in the test or after rollout = stop.
- **Bad signal to watch for:** Signal	Trigger	Checked	Owner → action Choose but not choose well	Primary improves ≥2pp, but the 30+ min rate CI includes 0	Weekly	Curator reviews rail titles abandoned under 10 min and tightens the list Cannibalization	Rail plays rise, but the all-session empty rate CI includes 0	Weekly	PM: iterate on list content or slot Watch minutes falling	Below −2%: iterate. Below −5%: pause	Weekly (test and Phase 3)	Analyst flags; PM decides within 24 hrs Novelty fade	Final-week effect is under 50% of week-1 effect	At readout, by refresh week	PM: extend the test before shipping Ticket spike	Spotlight-tagged tickets reach 2× the Week −1 baseline, or any already-watched-title report	Daily during the test, weekly after	Support Ops escalates; Engineering checks the filter
- **Likely post-launch decision:** Most likely: Iterate — keep the curated rail for Stranded Devotees, but refine it before expanding.  A rail versus today's homepage should reduce empty sessions, since it gives stuck users a short list where there was none. The weaker link is the 30+ minute rate: a single list for the whole segment will suit some Devotees and miss others, so expect more titles started without a matching rise in sustained watching. That pattern points to improving the list, not killing the rail. The natural next step is to test the deferred roadmap items that address fit, such as the Personalized Spotlight Queue (A5) or Why You'll Love This labels (A2), before expanding to Casual Browsers as a Medium launch.  A clean expand decision would need all three success metrics to hit. A kill would need watch minutes to drop or empty sessions not to move at all, which is less likely given how directly the rail targets the problem.
