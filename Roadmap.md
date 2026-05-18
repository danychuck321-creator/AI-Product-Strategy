Horizon 1 — Ship (0–4 weeks)
Initiative	Strategy Component	Why it ships now	Confidence
1. Create golden data record set correctly processed royalty statements	The Contract	You explicitly defined a 500-row target to hit your 92% reliability threshold; without this baseline, user trust cannot be measured.	H
2. Create royalty formula for reconciliation and test	The Bet	The deterministic business logic and math must be completely locked down before wrapping probabilistic AI around it.	H
3. Create golden data record set correctly reconciled royalty statements	The Contract	Fulfills the output-side requirement of the golden dataset, essential for testing the $500K escalation and HITL triggers.	H
Horizon 2 — Validate (1–3 months)
Initiative	Strategy Component	Hypothesis	Kill Criteria	Confidence
7. Create MVP that manages the workflow of reconciling the royalty statements...	The Bet	We can successfully orchestrate unstructured parsing and core AR data into a unified flow, despite CS Land vendor constraints.	If we cannot successfully parse and route 60% of basic statements without fatal schema errors by week 6, we stop.	M
4. Reconciled royalty statement redlines and correction	The Guardrails	Land Analysts will actively correct AI outputs within our workflow, creating a high-signal recursive learning loop.	If analyst correction time inside the tool takes longer than their legacy manual spreadsheet process by week 6, we stop.	M
Horizon 3 — Explore (3–6 months)
Initiative	Strategy Component	What must be true first	Confidence
5. Analysis of corrected royalty statements	The Moat	We need enough volume of redlined data flowing through the recursive loop to extract compounding commercial insights for joint venture negotiations.	L
8. Monthly agentic workflow review	The Guardrails	The underlying agentic architecture must be mature enough to expose discrete, human-readable audit logs for the analysts to actually review.	M
