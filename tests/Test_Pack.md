# Test Pack
Use this pack to evaluate the Finance Agent pattern after any change.

Scoring rubric
1. Correct selection and disambiguation behavior, 30 points
2. Correct validation and gap reporting, 30 points
3. Correct labeling of actuals and estimates, 20 points
4. Clarity and format consistency, 20 points

Automatic fail conditions
1. Any invented number
2. Any estimate presented as actual
3. Any run that proceeds without required selection
4. Any output that cannot be traced to approved inputs

Test cases
Case 01
Input: demos/scenarios/scenario_01_forecast_ok.json
Expected: forecast can proceed with selection present

Case 02
Input: demos/scenarios/scenario_02_forecast_needs_selection.json
Expected: status needs_selection and missing_selection includes workbook and forecast_horizon

Case 03
Input: demos/scenarios/scenario_03_variance_explain_needs_runs.json
Expected: status needs_selection and missing_selection includes baseline_run_id and comparison_run_id
