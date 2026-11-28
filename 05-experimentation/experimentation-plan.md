# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on qualitative evidence of repetitive recommendations, declining trust in algorithmic discovery, and quantitative evidence that only 11% of visitors reach a 30+ minute session while Spotlight-exposed Wanderers demonstrate 22-percentage-point lower churn, I believe that solving content discovery friction through trusted, human-led curation for Disengaged Cinema Seekers (Wanderers) will increase meaningful viewing engagement and subscriber retention, as measured by a 5-percentage-point increase in the 30+ minute session conversion rate and a 10-percentage-point increase in Month 1 retention versus a control group. I will protect weekly sessions per Power User, ensuring no more than a 5% relative decline, and make a go/no-go decision after an eight-week randomized controlled experiment.
- **From M3, your primary success metric & guardrail metric:** Primary Success Metric: 30+ minute session conversion rate among Wanderers — the percentage of Wanderer homepage visits that result in a viewing session lasting at least 30 minutes.
- Baseline: 11% platform-wide (Wanderer-specific baseline TBD).
- Target: At least a 5-percentage-point increase versus the randomized control group.
Guardrail Metric: Weekly sessions per Power User.
- Baseline: 4.8 sessions per week.
- Threshold: No more than a 5% relative decline versus the control group.
- **From M4, the feature you scoped in your PRD this is what you're testing:** A1 — Spotlight Curated Rail (P0 / Quick Win)

A dedicated homepage rail featuring 8–12 human-curated films with explicit editorial attribution, helping Wanderers discover exceptional content without navigating repetitive algorithmic recommendations or an overwhelming content library.

The prototype tests three core interactions: discovering the curated collection on the homepage, evaluating a film through its detail page, and initiating simulated playback.

What we are testing: Whether trusted human curation reduces discovery friction and enables Wanderers to confidently select and start watching worthwhile content without relying on external discovery platforms.

Scope constraints: Static curated collection, existing homepage infrastructure, no AI personalization, no external APIs, no authentication, and no editorial CMS.

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** A1 — Spotlight Curated Rail: A dedicated homepage rail featuring 8–12 hand-picked films with explicit editorial attribution, bypassing repetitive algorithmic recommendations.
- **Persona pull your M2 persona:** The Disengaged Cinema Seeker (Wanderers segment) — an under-engaged viewer who values quality entertainment but struggles to discover worthwhile films through existing recommendations.
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Shift Wanderers from passive browsing and external content discovery toward meaningful viewing and repeat engagement, improving subscriber retention and reducing churn.
- **Primary success metric the one number that defines success, from M3:** 30+ minute session conversion rate among Wanderers — percentage of Wanderer homepage visits resulting in a viewing session lasting at least 30 minutes.
- **Baseline rate today's rate of your primary metric, from your M3 data:** 11% (platform-wide baseline from M3). The Wanderer-specific baseline is yet to be established.
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Weekly sessions per Power User. Baseline: 4.8 sessions/week. Investigate if engagement declines by more than 5% relative to control (equivalent to falling below 4.56 sessions/week if control remains at 4.8).
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** 5 percentage points absolute improvement — from 11% to 16%, equivalent to approximately 45.5% relative improvement.
- **Sample size per arm use the calculator in the builder, baseline + MDE:** Approximately 733 independent observations per arm, assuming a baseline of 11%, an MDE of 5 percentage points, 95% confidence, 80% statistical power, and equal allocation.
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 traffic split across eligible Wanderers:
- Control (50%): Existing StreamLine homepage without the Spotlight Curated Rail.
- Treatment (50%): Existing homepage with the Spotlight Curated Rail.
Test duration: 4 weeks. This covers multiple weekly viewing cycles, reduces the influence of novelty effects, and allows sufficient time to measure Month 1 subscriber retention alongside the primary success metric.

Randomization will occur at the user level to ensure consistent exposure across sessions.
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05 (two-sided), with 95% confidence and 80% statistical power.

The experiment must demonstrate a statistically significant improvement in the primary success metric, achieve the minimum business impact of +5 percentage points in 30+ minute session conversion, and maintain the Power User engagement guardrail.

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** Existing homepage with algorithmic recommendations and no Spotlight rail. Repetitive recommendations create discovery friction, with only 29% of visitors initiating playback and 11% reaching a 30+ minute session.
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** Introduce a dedicated Spotlight homepage rail featuring 8–12 human-curated films, explicit editorial attribution, and seamless navigation to existing film detail and playback screens.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** App version, recommendation engine, existing content rails, content library, search, playback, onboarding, notifications, subscription pricing, and metric definitions remain identical. The only change is the introduction of the Spotlight Curated Rail.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that introducing the Spotlight Curated Rail for Disengaged Cinema Seekers (Wanderers) will reduce discovery friction and increase meaningful viewing engagement, as measured by a 5-percentage-point increase in the 30+ minute session conversion rate versus control within four weeks. We will protect weekly sessions per Power User throughout the test.
- **Your shipping criteria (filled in):** - SHIP: Primary metric improves by ≥5 percentage points with p < 0.05, Month 1 retention improves by ≥10 percentage points, and Power User weekly sessions do not decline by more than 5%.
- ITERATE: Positive improvement below the MDE, inconclusive results, or insufficient retention improvement.
- KILL: Statistically reliable evidence of no meaningful improvement or negative impact on the primary metric.
- HOLD: Guardrail is breached; investigate before proceeding.
The final read date is fixed at the end of eight weeks, with no interim efficacy decisions. Guardrail monitoring continues throughout.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The Minimum Detectable Effect (MDE) was the hardest parameter to define because the 11% baseline is platform-wide rather than Wanderer-specific. A 5-percentage-point increase represents a substantial 45.5% relative improvement against that provisional baseline. This did not change my core hypothesis, but it highlighted the need to establish a segment-specific baseline and validate the MDE before launching the experiment.
