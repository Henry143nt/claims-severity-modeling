\# Claims Severity Modeling — P\&C Insurance



\## Overview

This project analyzes and models claims severity using a large property \& casualty insurance dataset. The goal is to understand severity drivers, quantify tail risk, and evaluate models using metrics aligned with real insurance decision-making.



\## Data

\- ~188,000 claims

\- 132 features (categorical + continuous)

\- Target: claim severity (`loss`)



\## Exploratory Analysis

\- Claims severity is heavily right-skewed

\- Top 1% of claims account for ~6% of total loss

\- Continuous features show weak individual correlation with severity

\- Categorical segmentation reveals meaningful severity differences



\## Modeling

Two models were evaluated:

\- \*\*Ridge Regression\*\* (baseline, full dataset)

\- \*\*Random Forest Regression\*\* (sample-trained for computational efficiency)



\### Performance

| Model | MAE | RMSE | R² |

|------|-----|------|----|

| Ridge Regression | 0.440 | 0.560 | 0.519 |

| Random Forest | 0.449 | 0.574 | 0.494 |



\### Ranking Performance

\- Top decile captures ~25.7% of total loss

\- Top two deciles capture ~41.5% of total loss



\## Key Takeaways

\- Linear models provide stable severity estimates

\- Non-linear models add value through risk ranking

\- Loss concentration metrics are critical for insurance use cases



\## Business Applications

\- Claims triage and prioritization

\- Severity-aware reserving

\- Risk segmentation and portfolio monitoring



\## Limitations \& Next Steps

\- Models were trained without policy or temporal context

\- Random Forest trained on a sample due to hardware constraints

\- Future work could include frequency–severity modeling, temporal validation, calibration, and fairness analysis



\## Project Structure

claims-severity-allstate/

├── notebooks/

│ ├── 01\_eda.ipynb

│ └── 02\_modeling.ipynb

├── data/

├── outputs/

│ └── charts/

└── README.md



>>>>>>> 842d318 (Initial commit: EDA + modeling for claims severity)
