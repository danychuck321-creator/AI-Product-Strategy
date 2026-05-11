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
**Not confident (<50%):** Don't process a low confidence scored Royalty statement as it is the basis for the reconciliation process

**User control surface:** 

- Users see AI reasoning / drivers
- Users correct & override outputs
- Corrections feed back into the model / dataset
- Users adjust the confidence threshold _(not yet)_

  ## Confidence UX Design

**Approach:** show uncertainty / human-in-loop trigger
**Uncertain (50-90%):** Show areas of the reconciled royalty statement that may be incorrect and request that user checks manually.

**User control surface:** 

- Users see AI reasoning / drivers
- Users correct & override outputs
- Corrections feed back into the model / dataset
- Users adjust the confidence threshold _(not yet)_


## Confidence UX Design

**Approach:** show uncertainty
**Confident (>90%):** High reconciliation of royalty statement confidence

**User control surface:** 

- Users see AI reasoning / drivers
- Users adjust the confidence threshold _(not yet)_
- Users correct & override outputs _(not yet)_
- Corrections feed back into the model / dataset _(not yet)_



## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | 92 | Monthly timed when new invoices come in (asynchronous to actual production needs, mid month) - 50 unique invoices/operators - LLM as a judge | <90 → route to human review queue |
| Hallucination rate | <1% | Monthly timed when new invoices come in (asynchronous to actual production needs, mid month) - 50 invoices - false positives of reconciled invoices for month end | >1% → auto-rollback to last good model |
| Latency (p95) | <5mins | Can be viewed as a batch job reconciled process done within a day at most. | >1 hour → page on-call |
| Drift velocity | <0.5% / month | 3 month rolling accuracy trend as the cadence for new invoices to come in is monthly | > 1% / month → trigger gold-set audit |

## HITL Architecture

**Trigger:** Confidence is less than 90%

**Reviewer:** Commercial Land Analyst in India

**Feedback loop:** Reviewer corrections feedback into the model that parses the unstructured invoice data into structured data

