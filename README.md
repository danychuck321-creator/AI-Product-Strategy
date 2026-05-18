# Commercial Land Reconciliation 

> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS the strategy — version-controlled, board-ready, portable.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** Commercial Land Reconciliation 
- **AI Value Archetype:** Automator
- **Vulnerability Scores:**  Moat 3/5 · Data 4/5 · Platform 2/5
- **Top Risk:** Accessing the required operator agreements terms and conditions held within the propriertary CS Land system, that the vendor does not give us the schema
- **Confidence:**  M 
- **Prototype:** Reconcile a royalty statement manually with the correct data automatically inserted
- **Kill Criteria:** Attack: Model specific for reconciliation processes/back office support work. Wedge: Readily available on existing enterprise platforms to be used. Why users switch: More sustainable option, less costs, not requiring IT sustainment possibly

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 5/20
- **Weakest Loop:** network loop: Internal usage does not improve; however, new operator information improves over time providing valuable insights on the data itself
- **Top Encroachment Threat:** This domian is pretty straightforward, most of the data with the exception of what your joint venture agreements mention does not add uniqueness to the product other than to get the royalty payments correct
- **Encroachment Defense:** However, the join venture agreements with operators drilling on our lands gives the company unique positioning of understanding commercial activity around them from which they can analyze and leverage to inform and support new activitiy. For example, if it is known that an existing competitor has been agressively wanting to operate on our leases and potentially would like to adjacent to one we own, but does not currently have the right too, we can analyze this and understand this strong desire from which we can negotiate from a stronger position of royalties.
- **Vendor Portability:** Partial

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** N/A (Currently operates as an internal cost center; negative margin due to fully-loaded human OPEX and manual spreadsheet hours). 
- **Gross Margin (AI-adjusted):** Target 85%+ (Software-like margins achieved by reducing the unit cost to pure compute and fractional human-in-the-loop time). 
- **Pricing Model:** Outcome-based
- **Pricing Today → Tomorrow:** Internal cost/benefit capture, so no current pricing → Pricing based on each successful reconciliation (e.g., internal chargeback or calculated value-add of $40 per successful reconciliation).
- **Total AI COGS / unit:** ~$1.00 per reconciliation (Calculated as $149.50 total monthly AI infrastructure/HITL costs divided by an estimated 150 complex statements per user)
- **Cascading Strategy:**
- 	• Triage: Claude 3 Haiku / GPT-4o-mini
	• Frontier model: Claude 3.5 Sonnet / GPT-4o
	• Routing rule: Default all statements to the Triage model. Route to the Frontier model ONLY IF: (1) Extraction confidence drops below 85%, (2) tables span more than 3 pages, or (3) the operator is flagged as "adversarial".
	• Ratio: 65% Triage / 35% Frontier. 
- **Net Margin Shift:** Transforming a pure operational expense (manual labor) into a high-leverage digital asset. By dropping the cost of reconciliation from ~$50+ in human time to ~$1.00 in compute, the net margin shift is fundamentally transformative for the back office.
- **Break-even at:** ~6,250 successful reconciliations. (Assuming the $150,000 MVP build cost from your board pitch, divided by an estimated $24 of net value captured/saved per automated reconciliation).

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** 92
- **Golden Dataset:** 500 rows, __ adversarial
- **Confidence UX:** human-in-loop trigger / show uncertainty
- **HITL Architecture:** **Trigger:** Confidence is less than 90%
- **Failure Mode Coverage:** ## Confidence UX Design

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | |------|-------|--------|-----------|--------| | Recursive Learning | Land Analyst corrections for reconciled royalties | Update the golden record set, which is the royalty…
- **Governance Posture:** AI features in the Royalty Statement reconciliation process including the processing of unstructured royalty statements to structured formats and the reconciliation between accounts receivable, royalty statement and core…
- **Autonomy Boundaries:** Drafting an email to an operator on outstanding or overpayment of royalties — human approval required. Creating royalty data from unstructured royalty data — auto. Correct application of royalty formula — auto.
- **Escalation Triggers:** Confidence < 70% Reconciled amount for an operator in a given month > $500 K (Adjusted based on continuous audit loops)
- **Audit Cadence:** Monthly — Review autogenerated royalty formula for given operators (Land Analyst). Monthly — Invoice parsing of unstructured data (Land Analyst).
- **Shadow AI Audit (user-side):**
- **Agent Boundaries:** Drafting an email to an operator on outstanding or overpayment of royalties - cannot send without human
- **Regulatory Exposure:** _(not set)_

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
Horizon 1 — Ship (0–4 weeks)
Initiative	Strategy Component	Why it ships now	Confidence
1. Create golden data record set correctly processed royalty statements	The Contract	You explicitly defined a 500-row target to hit your 92% reliability threshold; without this baseline, user trust cannot be measured.	H
2. Create royalty formula for reconciliation and test	The Bet	The deterministic business logic and math must be completely locked down before wrapping probabilistic AI around it.	H
3. Create golden data record set correctly reconciled royalty statements	The Contract	Fulfills the output-side requirement of the golden dataset, essential for testing the $500K escalation and HITL triggers.	H
- **Horizon 2 (Next):**
Horizon 2 — Validate (1–3 months)
Initiative	Strategy Component	Hypothesis	Kill Criteria	Confidence
7. Create MVP that manages the workflow of reconciling the royalty statements...	The Bet	We can successfully orchestrate unstructured parsing and core AR data into a unified flow, despite CS Land vendor constraints.	If we cannot successfully parse and route 60% of basic statements without fatal schema errors by week 6, we stop.	M
4. Reconciled royalty statement redlines and correction	The Guardrails	Land Analysts will actively correct AI outputs within our workflow, creating a high-signal recursive learning loop.	If analyst correction time inside the tool takes longer than their legacy manual spreadsheet process by week 6, we stop.	M
- **Horizon 3 (Bet):**
Horizon 3 — Explore (3–6 months)
Initiative	Strategy Component	What must be true first	Confidence
5. Analysis of corrected royalty statements	The Moat	We need enough volume of redlined data flowing through the recursive loop to extract compounding commercial insights for joint venture negotiations.	L
8. Monthly agentic workflow review	The Guardrails	The underlying agentic architecture must be mature enough to expose discrete, human-readable audit logs for the analysts to actually review.	M

- **Board Narrative:** **The case:**
- 
- **Ask:** ## M1 Baseline vs. Now
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
