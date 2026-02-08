# 09 Testing And Evaluation
Finance agents must be testable.

Test pack coverage should include
1. Forecast run with complete inputs
2. Forecast run blocked by missing selection
3. Forecast run blocked by missing opening balance
4. Forecast run with stale actuals flagged
5. Variance explanation between runs
6. Outlier detection and reporting

Automatic fail conditions
1. Any invented number
2. Any estimate presented as actual
3. Any targeted action taken without required selection
4. Any output that cannot be traced to approved inputs
