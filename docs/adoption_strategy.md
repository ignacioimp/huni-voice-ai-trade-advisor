# Customer adoption strategy

## Hypothesis

Natural voice interaction may reduce onboarding friction for SME customers who are unfamiliar with trade terminology. This hypothesis has not been validated. The objective is a more useful preliminary diagnostic, not simply more conversations.

## Proposed rollout

| Phase | Action | Exit condition |
| --- | --- | --- |
| Prototype | Run the five synthetic scenarios and safety checks | Critical accuracy and privacy checks pass; actual results recorded |
| Controlled pilot | With consent and appropriate platform terms, invite a small group of users or internal reviewers | Compare quality and friction against the existing onboarding process |
| Iteration | Review transcripts, correction patterns, incomplete fields and feedback; adjust one prompt or workflow variable at a time | Improvements confirmed in regression tests |
| Expansion | Segment by customer experience and use case; create short multilingual onboarding guides; plan appropriate human escalation | Quality, privacy and unit economics reviewed before expanding |

## Measurement framework

All metrics below are proposed, not actual results. Record sample size, date range, eligibility, missing observations and versions.

| Metric | Definition |
| --- | --- |
| Activation rate | Users who start a conversation / eligible users invited |
| Diagnostic completion | Started sessions with confirmed objective, essential facts and next step / started sessions |
| Time to value | Median time from session start to first useful recommended next step; report incomplete sessions separately |
| Field accuracy | Correctly extracted applicable fields / manually reviewed applicable fields; track missing and unsupported values separately |
| Critical error rate | Reviewed sessions with fabricated regulatory/cost claims, unsafe requests or false execution claims / reviewed sessions |
| Quality pass rate | Sessions meeting all applicable evaluation criteria / sessions with evaluable outcomes; report unknowns separately |
| Handoff readiness | Completed diagnostics that a human advisor judges sufficient to begin the next step / completed diagnostics reviewed |
| Customer effort | Post-session user rating and qualitative feedback on ease of use |

Compare with a manually measured baseline using similar customer types and task complexity; avoid attributing causality to voice alone. Track model/voice costs and latency before commercial deployment. A proposed release gate is zero critical errors observed in the reviewed synthetic suite, with all failures corrected and retested; this does not guarantee safety in production.

## Scalable enablement

Create repeatable onboarding scenarios, short demo videos, reusable prompt templates and a feedback loop. Track common reasons for abandonment, unclear questions and failed extraction. For regulated use cases, route decisions to qualified specialists. Review adoption by cohort and language rather than assuming one workflow fits all customers.
