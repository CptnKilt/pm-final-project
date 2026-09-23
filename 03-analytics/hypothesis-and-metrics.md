# Hypothesis & Success Metrics (Module 3)

## Pre-work · Hypothesis check
- **Role , who you are solving for (from M2):** A 52-year-old long-time subscriber who cancelled last year and now watches films picked by a competitor.
- **Goal , what this user is ultimately trying to achieve:** Good evenings without the work of searching for them. Inferred from "quality of my evenings went down" and from him watching both of the two weekly picks
- **Friction / moment of misery , the specific pain blocking their goal:** The catalog turned into a "warehouse." As the volume went up, nothing helped him find what was worth his time, so he switched to a service that sends him two hand-picked films a week.
- **Current workaround , the external tool or manual process they rely on (M2):** Using another streaming service
- **Problem Hook , your one-sentence framing of the business crisis (M1):** StreamLine is losing its most valuable users — not gradually demoting them to passive players, but losing them from the platform altogether — because it stopped telling them what's worth watching, and by the time users start solving that problem elsewhere, they're not reliably coming back at all.
- **Value Proposition , the outcome your initiative promised to deliver (M1):** For high-engagement, taste-driven viewers who used to treat StreamLine as a discovery authority and now only use it to press play on titles they found elsewhere, we will build StreamLine Spotlight: a dedicated, human-curated space inside the app — bounded collections, named curators, real editorial point of view — that restores the feeling of a trusted guide inside a platform built for scale, without shrinking the mass-market library that funds it because the window to own the "trusted taste" position is closing. Every month StreamLine waits, specialized competitors get further ahead in owning that narrative with exactly the segment StreamLine can least afford to lose — and repositioning against an entrenched competitor always costs more than establishing the position first.

## Read your data snapshots
- **Does the funnel data confirm your M2 friction point, or does it tell a different story? Note where the numbers align with the qualitative pain you found and where they diverge.:** The funnel partially confirms my M2 friction. The drop from browsing to playing, where roughly 60% of browsers never press play, and the 7-point fall in searched-then-played both fit a discovery problem: users can't find something worth their time. The 21% DAU decline is consistent with my hook that high-value users are leaving. But the data diverges in two ways. First, the steepest drop is after play starts: 62% of starts never reach 30 minutes. That points to a problem with the quality of picks, not only with finding them. Second, the 23% fall in session length shows remaining users are also disengaging, which complicates my claim that users are leaving rather than becoming passive. There is also a scope limit. This data is mobile-only and covers only active users, while my persona is a churned, likely TV-based viewer. I need churn and cohort data by segment and device before treating this as confirmation
- **Do the retention patterns align with the workaround your M2 persona used to find content? Note what the Mo. 0→1 drop suggests about the onboarding experience your persona described as frustrating.:** Retention aligns with my persona's workaround. He left for a service that pushes two curated films a week, and the Spotlight cohorts, which get a similar bounded, curated experience, retain better at every point measured. The gap over the Full Library grows from 11 points at Month 1 to 18 at Month 3, which suggests curation builds a lasting habit rather than a one-time bump. The Month 0→1 drop is still the largest leak for every cohort (21–26 points even with Spotlight), which suggests new users meet the "warehouse" problem before they have enough history for recommendations to help. That points toward making curated picks the centre of onboarding. Two limits: my persona was a lapsed long-time subscriber, not a new user, so these cohorts don't show whether Spotlight would win back users like him. And the Spotlight cohorts are winter sign-ups, so seasonality could explain part of the lift.
- **Does the LTV gap and the content mix (61% trending for Wanderers) confirm the moment of misery your persona described? Note which segment your persona is in and whether the data confirms their pain.:** The content mix supports the "warehouse" moment of misery. Wanderers get 61% of their viewing from trending, the default when nothing tells them what is worth watching, and they show the largest churn improvement when exposed to Spotlight (22 points). My persona, though, fits the Power User profile: taste-driven, high-engagement and curation-first (58% curated). This segment is described as low-churn, yet my persona churned. That suggests either survivorship bias (lapsed Power Users aren't counted) or that he drifted into Wanderer-like behavior before cancelling. So the data confirms the pain, but mainly for Wanderers, not for the segment my persona represents. A rough estimate (share × churn reduction × LTV) puts Wanderers ahead of Casual Browsers in revenue protected, though the churn baseline and exposure method aren't stated. This challenges my hook's focus on "most valuable" users: Spotlight's strongest case may be as a guide for the undecided mass market, which is larger in total impact.
- **Does the low adoption confirm your persona is burdened by tools they don’t use? Note whether the low scheduling adoption (42%) for coordinators matches your M2 moment of misery.:** _(not filled in)_
- **Does the workflow data match the manual process or hack you documented in M2? Note whether the specific drop-offs or time gaps explain why your persona avoids the digital tool.:** _(not filled in)_
- **Look at the CSAT heatmap. Which specific cell most directly maps to your persona’s friction? Note how the NPS trend justifies the urgency of your M1 Problem Hook.:** _(not filled in)_

## Step 3 · Craft your hypothesis
- **Qualitative evidence (from M2) , quote the specific friction / moment of misery for your persona:** UXR-04, long-time subscriber (52), cancelled: He described the catalog as having "became a warehouse" and said the "quality of my evenings went down." As the library grew, nothing helped him find what was worth his time, so he moved to a competitor that sends two hand-picked films a week. He watches both.
- **Quantitative evidence (from M3) , name the metric or data point that confirms the pain; cite the number:** Primary: Wanderers (41% of the base) get 61% of their viewing from Trending and only 18% from Curated. When exposed to Spotlight, their churn drops by 22 points compared with non-exposed Wanderers, the largest improvement of any segment (Snapshot 3). With no guide to what's worth watching, users default to Trending and drift away. Once they get a curated guide, they stay.

Supporting: Spotlight cohorts retain better, and the gap widens over time: +11 points at Month 1 and +18 points at Month 3 (Dec 52% vs. Nov 34%) (Snapshot 2). Before Spotlight, discovery was also weakening: content searched then played fell from 41% to 34%, and 30+ minute sessions fell from 19% to 11% (Snapshot 1).
- **Persona , role, goal, and the friction you confirmed in the reconciliation steps:** Persona: A 52-year-old long-time subscriber who cancelled and now watches the two films a week hand-picked by a competitor (UXR-04).

Role: A taste-driven viewer who wants a trusted guide to what's worth watching. His profile resembles a Power User (58% curated viewing). The data shows the same need most strongly among Wanderers, 41% of the base, who have no guide and default to Trending.

Goal: Good evenings without the work of searching for them.

Confirmed friction: As the catalog grew, it "became a warehouse" with nothing pointing to what's worth watching. Users fall back on Trending, engage less, and leave. The data confirms this:

Wanderers get 61% of their viewing from Trending, and their churn drops 22 points with Spotlight.
Spotlight cohorts retain 18 points better by Month 3.
Searched-then-played fell from 41% to 34%.

What changed from M2: The friction holds, but the segment shifted. The strongest evidence comes from undecided, mass-market users, not only taste-driven ones like the persona. Lapsed Power Users aren't visible in the M3 data.
- **Problem you are solving , one sentence describing the specific friction this initiative removes:** Viewers can't tell what's worth their time in an ever-growing catalog, so they fall back on Trending, drift away, and leave.
- **Strategic outcome , what behaviour change do you expect, and how does it map to retention / revenue / churn?:** Behavior change: Viewers stop defaulting to Trending and start their evenings from a small set of curated picks. Wanderers shift from 18% toward Casual-level curated viewing (~31%) and come back more often than once a week, building a weekly habit around the picks, as the persona did with his two-a-week service.

How it maps:

Retention: Spotlight cohorts reach 52% by Month 3, compared with 34% for Full Library (+18 points). The target is to hold or widen that gap and cut the Month 0→1 drop by putting curated picks into onboarding.
Churn: −22 points for Wanderers and −14 points for Casual Browsers when exposed to Spotlight. These two segments are 78% of the base.
Revenue: A rough estimate (segment share × churn reduction × monthly revenue per user) gives about $135 protected per 100 users per month, roughly 12% of monthly revenue. About 56% comes from Wanderers and 44% from Casual Browsers.

Leading indicators: Wanderers' curated share of viewing, sessions per week, and Month 1 retention for new cohorts.
- **Primary success metric (initiative signal) , the leading indicator that tells you the gap is closing:** Primary success metric: Wanderers' curated share of viewing, meaning the % of Wanderer play-starts that come from Spotlight or curated collections instead of Trending.

Baseline: 18% (Snapshot 3)
Target: 31% within two quarters, which is the Casual Browser level
Why it's leading: It measures the friction directly. Users who start from a trusted pick instead of defaulting to Trending are the ones Snapshot 3 shows churning 22 points less. It moves weeks before churn or retention numbers can.
- **Guardrail metric (product signal) , the metric that must NOT drop; it protects your existing base:** Guardrail metric: Power User sessions per week

Baseline: 4.8× (Snapshot 3)
Threshold: Must not fall below about 4.6× (a drop of more than 5%)
Why this one: Power Users are 22% of the base but about 29% of revenue, and they have the highest LTV ($14.20). They already churn little and rely on curation (58%). The risk is that reshaping the app around Spotlight for Wanderers disrupts how your best users already find and watch content. If their frequency slips, Spotlight is winning the mass market at the expense of your most valuable segment.
- **Decision window , how much time or data before you scale, pivot, or kill? minimum threshold to proceed?:** Decision window: 12 weeks. Run a randomized test with Wanderers split into Spotlight-exposed and control groups. That fixes the self-selection and seasonality problems in the Snapshot 2–3 data, and 12 weeks gives two new-user cohorts time to show Month 1 retention.

Minimum threshold to proceed (all three must hold):

Wanderers' curated share of viewing is ≥25% (baseline 18%, final target 31%)
Month 1 retention for exposed cohorts is ≥10 points above control
Power User sessions per week stay ≥4.6×

Scale: All three are met. Roll Spotlight out to all Wanderers and Casual Browsers, and make curated picks part of onboarding.

Pivot:

If curated share rises but retention lift is under 5 points, people are clicking but not staying. Rework curation quality and depth.
If the Power User guardrail is breached, change where Spotlight sits in the app rather than dropping it.

Kill: At week 12, curated share has moved less than 3 points (still ≤21%) and there's no retention lift. Wanderers aren't taking the guide.
- **Draft your full hypothesis sentence , one to three sentences; quote the metric, name the persona, name the outcome:** Based on UXR-04's description of the catalog as a "warehouse" and the Snapshot 3 finding that Wanderers churn 22 points less when exposed to Spotlight, I believe that giving viewers a trusted, curated guide to what's worth watching, for guidance-starved users like the 52-year-old lapsed subscriber and the Wanderers who default to Trending, will reduce churn and lift Month 1 retention by at least 10 points. Success will be measured by raising Wanderers' curated share of viewing from 18% to 31% (with ≥25% as the minimum to proceed). I will protect Power User sessions per week (no lower than 4.6×, from 4.8×) and will make a go/no-go decision after a 12-week controlled test.
