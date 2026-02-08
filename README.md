```markdown
# Finance Agent Case Study: Cash Forecasting and Treasury Operations
A practical case study showing how a Finance Agent can support treasury workflows with reliable, auditable outputs that do not guess, do not invent numbers, and enforce selection and disambiguation before any targeted action.

This repo is written for end users and stakeholders first.
Treasury, FP and A, finance leaders, and business partners who need faster answers without losing control of accuracy.

This repo is public safe.
No tenant identifiers.
No internal urls.
No secrets.
No proprietary financials.
Examples are sanitized and illustrative only.

## What this case study demonstrates
This case study demonstrates a governed Finance Agent pattern for cash forecasting and treasury support.

You will see
1. Clear purpose and scope that prevents feature sprawl
2. Approved source boundaries so answers are grounded
3. Deterministic calculation behavior that is repeatable
4. Selection and disambiguation gates that stop wrong target work
5. Validation and gap reporting instead of guessing
6. Structured run logs that make outputs auditable
7. Scenarios and a test pack that prove the behavior

## What the Finance Agent does and does not do
What it does
1. Retrieves approved finance inputs from designated lists and spreadsheets
2. Validates inputs before calculations to catch missing, stale, or inconsistent data
3. Produces a cash forecast output in a consistent, reviewable format
4. Distinguishes actuals vs forecasts and labels estimates explicitly
5. Explains variance drivers using source grounded evidence
6. Produces run logs showing what inputs and assumptions were used

What it does not do
1. It does not fabricate numbers when a value is missing
2. It does not override finance owned assumptions without explicit instruction
3. It does not execute payments, move money, or perform bank actions
4. It does not change source data unless explicitly authorized and targeted
5. It does not provide tax or legal advice

## The core rule: no guessing in finance
If a required value is missing or ambiguous, the agent does not invent it.
It flags the gap, explains the impact, and requests the minimum next step required to proceed safely.

That is the difference between a forecasting assistant and a risk generator.

## How the Finance Agent works at a high level
Step 1: Intake the request
Examples
Generate weekly cash forecast through next Friday
Summarize upcoming outflows this week
Explain why the forecast changed since last run

Step 2: Confirm scope through selection and disambiguation
The agent confirms or requests selection for any required identifiers.
Forecast horizon and date range
Entity, account scope, or workbook selection if relevant
Business day calendar assumptions if relevant

Step 3: Retrieve approved inputs
Typical input groups
Opening balances
Actuals
Known scheduled inflows
Known scheduled outflows
Payroll and recurring payments
Debt and interest schedules
One time adjustments

Step 4: Validate inputs
Checks include
Missing values
Stale data
Duplicate entries
Date gaps
Outliers vs recent history
Inconsistent totals across sources

If validation fails, the agent produces a gap report and stops unless explicit instruction allows a limited run.

Step 5: Produce forecast output
A consistent table that includes
Date
Beginning balance
Inflows
Outflows
Net change
Ending balance
Actual vs forecast indicator
Confidence notes

Step 6: Explain variance drivers
When comparing runs, drivers are grouped and traced.
New actuals posted
Timing changes
New scheduled items
Removed items
Assumption updates
One time adjustments

Step 7: Output and run log
Every run produces a structured log for review and testing.

## Two minute proof path
1. Read docs/01_Executive_Summary.md
2. Read docs/04_Data_Sources_And_Field_Map.md
3. Read docs/06_Validation_Rules_And_Gap_Report.md
4. Open demos/scenarios/scenario_02_forecast_needs_selection.json
5. Review a recorded run log in demos/runs

## Repo layout
docs
Narrative case study content written for end users

demos
Scenarios and recorded run logs

examples
Sanitized example outputs

tests
Test pack and scoring rubric

governance
Change control and change log

redaction
Public repo checklist

## Testing and quality control
See tests/Test_Pack.md.

Automatic fail conditions include
1. Any invented number
2. Any estimate presented as actual
3. Any targeted action taken without required selection
4. Any output that cannot be traced to approved inputs

## Operations and change control
See governance/Change_Control.md and governance/Change_Log.md.

Any change to assumptions, formulas, routing, or sources requires
A documented change request
Review by a finance owner
Test pack run
Change log entry
Rollback capability

## Engagement and inquiry prompts
1. What is the single most valuable forecast output for your team
2. What are the approved sources for balances, actuals, and schedules
3. Which values are allowed to be estimated and who owns those assumptions
4. What identifiers must be selected before a run, entity, account, workbook
5. What does a passing forecast run look like for your risk tolerance
6. Who owns assumption updates and on what cadence

## License
MIT
