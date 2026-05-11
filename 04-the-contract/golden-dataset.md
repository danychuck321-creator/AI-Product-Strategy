# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 |Reconciliation of new operator and or new well on leased lands, but not currently in the system | Med Risk: System warning that operator and or new well are not in the system, thereby cannot reconcile | N | rule |
| 2 |Incorrect parsing of critical royalty data into structured format such as Total royalties owed, incorrect agreement factors, or wells stated |High Risk: Correctly parsed information from royalty statement | N | rule / LLM |
| 3 |System analytics usage highlights low usage of ~30%, with negative internal sentiment captured through the feedback form |Poor system usage highlighting a need to work on either change management or the system is outputting a correct reconciliation | N | rule / LLM |
| 4 |System reconciles a royalty statement incorrectly, where it is a false positive. | High Risk: Doubecheck royalty statements are correct| N | rule / LLM |
| 5 | | | N | rule / LLM |




Dataset health
- Total: 4
- Edge cases: 0 (0.0%)
- Judge mix: 25% rule / 25% LLM / 50% both


**Adversarial rows included:** __
**Coverage gaps identified by partner:**

## Confidence UX Design

**Approach:** human-in-loop trigger / show uncertainty

**Confident (>90%):** _(not set)_

**Uncertain (50-90%):** _(not set)_

**Not confident (<50%):** Don't process a low confidence scored Royalty statement as it is the basis for the reconciliation process

**User control surface:** 

- Users see AI reasoning / drivers
- Users correct & override outputs
- Corrections feed back into the model / dataset
- Users adjust the confidence threshold _(not yet)_



## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
