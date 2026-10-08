# econ5200-lab05-risk-model
Diagnosing a Flawed Risk Model — VaR, Expected Shortfall & Monte Carlo
Objective
I evaluated a risk model that used a normal-distribution assumption and checked whether it understated portfolio tail risk.
Methodology
- Compared normal, historical, and Student-t approaches for VaR and Expected Shortfall.
- Fitted a Student-t distribution with df = 4.58.
- Used antithetic variates to reduce Monte Carlo standard error.
- Used the risk_metrics.py module with calculate_var, calculate_es, and mc_var, and ran its self-tests.
- Used an AI-generated VaR backtest, revised the prompt, and checked the result against my own count.
Key Findings
- The normal 99% VaR understated historical VaR by 12.7%, or $40,393 on the portfolio.
- The normal 99% VaR was breached on 1.71% of days, which is higher than expected for a 99% VaR.
- The Student-t model captured the heavier tail behavior with a fitted df of 4.58.
- Antithetic variates reduced Monte Carlo standard error by 1.26x.
