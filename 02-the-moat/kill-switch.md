# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Frontier AI model on SnowFlake that does the document parsing into a strucutred format. The propreitary corrections made to ingest the invoices properly will be lost if the vendor is changed to one like in Databricks| M | Keep the data in two different vector databases, i.e. the competitor space, Databricks to derisk this  |
| **Abstraction** | Direct API calls to Snowflake, exposing interdepndencies | M  | Change to an MCP model such that existing flow does not break |
| **Routing** | Enterprise AI determines that SnowFlake Cortex AI gets too costly, they turn it off| M | have hot standby setup for Databricks |
| **Eval** | Have golden set of records for known invoices processing the inputs correctly. | M | Automate the testing using golden record set|

## Portability Score
<!-- Ready / Partial / Locked -->

## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? -->

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
