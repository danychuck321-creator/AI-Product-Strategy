# Cost Curve & Pricing Strategy

Leader: Reconciliation of Royalty Statements
_____
Filler: Analytics report on compliance sliced in many different ways, i.e. by operator, location, producing type
_____
Killer: Business Intelligence layer that seeks commercial opportunities (revise contracts, sell or purchase) land based on drilling activitiy 
_____
Killer usage 20% 
_____
Bundle or add-on
Killer would be an add-on because it is a seperate tool entirely and deters from the core functionality of reconciling royalty statements
_____
70% rule: if Killer usage is <70%, it is probably an add-on.

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $35.00|Frontier model usage: Assuming ~20k input tokens/statement for dense, multi-page financial tables. Accounts for high-cost visual/OCR token usage. |
| Inference (cascading/triage) |$4.50 |Fast/cheap model usage: Initial document classification, simple data extraction (dates, operator names), and routing logic. |
| Infrastructure |$18.00 | Vector database indexing (for the JV agreement RAG pipeline), LangGraph/orchestration compute, and secure API gateways.|
| Data/storage |$7.00 |Blob storage for original unstructured PDFs, structured JSON outputs, and embedding storage for the Golden Dataset. |
| Human-in-the-loop |$85.00 |Internal cost representation: Assuming 15% of statements trigger the <90% confidence threshold, requiring ~10 minutes of manual Land Analyst correction time. |
| **Total AI COGS** |$149.50 |This is your baseline COGS per seat to benchmark against your outcome-based pricing model. |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

Triage model: Claude 3 Haiku / GPT-4o-mini
Frontier model: Claude 3.5 Sonnet / GPT-4o
Routing rule: All inbound statements pass through the Triage model first. Route to the Frontier model ONLY IF:

The Triage model's extraction confidence score drops below 85%.

The document contains nested, unstructured royalty tables spanning more than 3 pages.

The operator is flagged in the system as "adversarial" or uses heavily non-standard/handwritten statement formats.
Expected cascade ratio: 65% Triage / 35% Frontier (This ratio is critical; if the Frontier model handles more than 40% of the volume, your inference costs will begin to destroy the gross margin of your outcome-based pricing).

## Pricing Model

**Current pricing:** Internal cost/benefit capture, so no current pricing
**Proposed AI pricing:** Pricing based on each successful reconciliation
**Model:** Outcome-based

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x |10% |switch to competing models that are not as |
| Heaviest segment doubles |none |outcome based, so each successful reconciled royalty statemetn correlates with processing a respective statement |
| Model provider raises prices 50% |~10% | Transition to another LLM that can read and parse the invoice data|

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
