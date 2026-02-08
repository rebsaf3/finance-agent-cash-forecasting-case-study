# 06 Validation Rules And Gap Report
Validation happens before calculation.

Validation checks
1. Missing required fields
2. Stale inputs based on last updated timestamps when available
3. Duplicate entries
4. Date gaps across forecast horizon
5. Outliers vs recent history using simple thresholds
6. Total mismatches across sources when reconciliation keys exist

Gap report output
Missing inputs by category
Impact statement
Minimum next action required
Proceed or stop recommendation

A missing opening balance is a hard stop unless explicitly approved for a partial run.
