# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1 — Now (0-3 months)
*Quick wins. Ship with existing capabilities.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
|Create golden data record set correctly processed royalty statements|The Contract|H|
|Create royalty formula for reconciliation and test|The Bet|H|
|Create golden data record set correctly reconciled royalty statements|The Contract|H|

### Horizon 2 — Next (3-9 months)
*Bets. Requires new capabilities or integrations.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| Create MVP that manages the workflow of reconciling the royalty statements| The Bet| M |
|Reconciled royalty statement redlines and correction | The Guardrails| M|

### Horizon 3 — Bet (9-18 months)
*Moonshots. High uncertainty, high potential.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
|Analysis of corrected royalty statements |The Moat |  L |
|Monthly agentic workflow review|The Guardrails|M|

## Board Pitch

Thesis (1 sentence): We are transforming commercial land reconciliation from a manual back-office bottleneck into a strategic negotiation asset by automating the extraction of unstructured royalty statements to feed our deterministic financial workflows.

The case:

Why now: The shift from brittle, template-based OCR to multimodal LLMs means we can finally extract structured financial data from adversarial, unstructured operator statements with high fidelity and without sustaining massive IT overhead.
What's defensible: The reconciliation math is a commodity; our moat is the proprietary joint venture (JV) agreements. As the system parses and corrects operator data, we build a compounding intelligence asset that reveals competitor activity on our leases—giving us an encroachment defense and negotiation leverage that generic ERP or accounting vendors cannot replicate.
The economics: We plan to capture value through outcome-based pricing per successful reconciliation, but our unit economics are currently unvalidated. Because parsing complex 50-page statements is token-intensive, calculating the exact Total AI COGS per unit against our golden dataset is a mandatory engineering gate in Horizon 1 before we finalize the business model.
The risks:

Trust / failure modes: The catastrophic failure mode is a hallucinated extraction leading to a massive overpayment or compliance breach. We mitigate this with strict architectural boundaries: probabilistic AI is restricted strictly to unstructured data extraction, while the royalty formula application is handled by deterministic code. We are measuring against a 500-row golden dataset, forcing human-in-the-loop (HITL) for any extraction under 90% confidence, and hard-stopping any auto-escalation over $500K.
Scale / governance: At 10x scale, the primary risk is unchecked autonomy and dataset drift. We are enforcing strict agent boundaries (e.g., the system can auto-draft an operator email but cannot send without a human), and establishing a monthly Land Analyst audit cadence to ensure the "Recursive Learning" loop doesn't inject localized bias into the golden dataset.
Competitive: The single biggest execution risk is not the model, but data access. If the vendor for the proprietary CS Land system refuses schema access and we cannot establish a reliable, cost-effective ingestion pipeline within the first 6 weeks of Horizon 2, we trigger our kill criteria and walk away.
The ask: $150,000 and 2 engineers for a 6-month time horizon to deliver the MVP. This funds the creation of the 500-row golden dataset, the locking of the deterministic formulas, and the validation of the unstructured parsing workflow. If funded, this team will be exclusively ring-fenced from standard IT sustainment tasks.

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

**Now:**
