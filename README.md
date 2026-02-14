# credit-risk-project# Credit Risk Analysis Project

This is my first end-to-end data analysis project using the **German Credit Dataset** (1,000 loan applicants).  
Goal: Predict whether a loan applicant is likely to default (bad credit risk) or not.

### What I Did
- Explored the data in **Excel** → calculated default rates by loan purpose, amount, duration, age, housing, etc.
- Used **SQL** (MySQL) → segmented risk groups and found high-risk combinations (e.g. long duration + certain purposes)
- Built a **logistic regression model** in Python (scikit-learn)
  - Original model: ~75.5% accuracy, caught ~41% of defaults
  - Tried class-balanced version: accuracy dropped to ~68%, but caught **63%** of defaults (much better at finding bad loans)
- Fixed convergence issues by scaling features (StandardScaler)
- Visualized **feature importance** (coefficients) → top drivers of default risk

### Key Findings
- **Strongest risk factor**: Longer loan duration (higher coef = much more likely to default)
- **Strong protective factors**: Older age, owning a home, high checking account balance
- Surprising: Unknown/no checking account linked to lower risk (possibly older/established people)
- Riskier purposes: education, repairs, larger credit amounts

### Files in this repo
- `credit_risk_analysis.ipynb` → full notebook with code, EDA, SQL, models, and plots
- `feature_importance_plot.png` → screenshot of top features by impact

### What I Learned
Handling class imbalance is important in credit risk (accuracy isn't the only metric).  
Interpreting coefficients helps understand business drivers.  
Debugging (like convergence warnings) is part of real work.
