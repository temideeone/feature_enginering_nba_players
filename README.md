# NBA Player Longevity Prediction – Feature Engineering Pipeline

##  Project Overview
This project focuses on the crucial pre-modeling phase of machine learning: **Feature Engineering**. Using a dataset of NBA rookie performance statistics, the goal is to clean, filter, and transform raw box-score metrics into a highly predictive, non-redundant feature set optimized for forecasting whether a player's career will last 5+ years.

##  Feature Engineering Workflow & Rationale

1. **Target Isolation:** Standardized `target_5yrs` as our binary dependent variable (1 = Career ≥ 5 Years, 0 = Career < 5 Years).
2. **Noise Reduction:** Stripped structural identifiers like `Name` and `ID` to prevent overfitting and eliminate data leakage.
3. **Imputation Strategy:** Identified null values within shooting percentage metrics (e.g., `3P%`). Imputed these instances with `0` to reflect zero conversion on zero attempts accurately without distorting the data distribution.
4. **Multicollinearity Resolution:** Conducted correlation matrix evaluations. High colinearity was observed between volume metrics (e.g., Minutes Played vs Points). 
5. **Composite Metric Generation:** Developed **Points Per Minute (PPM)** and **Efficiency Per Minute** to pivot the model's focus from sheer playing volume to per-minute productivity.

##  Repository Structure
* `nba_players.ipynb` - Completed notebook with visualizations and data pipeline.
* `nba_players.csv` - The final clean, engineered dataset ready for ML modeling.
* `requirements.txt` - Dependency file.

Developed by [Temidayo Samuel Abodunrin] as 3mtt project
