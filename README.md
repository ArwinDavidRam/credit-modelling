# credit-modelling
Credit Modelling Project

**Data Engineering**: Loaded and integrated LendingClub loan data (~2.3M records) with U.S. macroeconomic indicators from World Bank. Applied censoring to late vintages to ensure 12-month default observability.

**Feature Engineering**: Implemented governance-friendly preprocessing including outlier clipping, nonlinear transformations (sqrt, log), imputation, scaling, and categorical handling.

**Model Development**: Trained and validated five PD models (Logistic Regression, LDA, Probit, Decision Tree, Random Forest) with hyperparameter tuning. Designed a custom composite ranking metric combining calibration and discrimination.

**Model Selection**: Selected top two models (Random Forest as Champion, LDA as Challenger) based on calibration (Brier, LogLoss, Avg_PD alignment) and AUC performance.

**Risk Parameter Estimation**: Computed loan-level PD, EAD (via amortization or outstanding principal), and LGD (adjusted for recoveries and settlements).

**Stress Testing and Expected Credit Loss (ECL)**: Designed and applied macroeconomic and borrower-level shocks across Baseline, Adverse, and Severe scenarios. Recomputed PD and 12-month ECL for each scenario.

**Portfolio Risk Simulation**: Performed Monte Carlo simulations (10,000 iterations) to estimate portfolio loss distribution; computed Value at Risk (VaR) and Conditional VaR (CVaR) at 95% and 99% confidence levels.

**Governance & Compliance**: Ensured IFRS 9/Basel alignment through reproducible pipelines, documented feature transformations, and scenario definitions.
