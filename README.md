# Advertising Budget Optimization & Revenue Prediction

## 1. Project Overview

This project aims to develop a data-driven advertising budget optimization framework using historical advertising performance data.

The project combines time-series revenue prediction, machine learning interpretability, and budget allocation simulation to evaluate different advertising investment strategies and identify potential improvements in budget efficiency.

A **LightGBM regression model** is developed to predict advertising revenue, followed by a budget allocation simulation comparing three strategies under a fixed total budget.

**Key Result:** Under a simulated total budget of RMB 10,000, the model-driven allocation strategy achieved the highest expected ROI of **10.72**, with **68.8% higher expected revenue** than the equal allocation strategy.

> **Note:** This is an independent simulation project based on historical advertising data. The reported results are simulation outcomes rather than actual campaign performance.

## 2. Project Objectives

- Build a machine learning model to predict advertising revenue based on historical time-series data.
- Apply time-aware cross-validation to prevent temporal data leakage.
- Improve model performance through hyperparameter optimization.
- Interpret model predictions and feature contributions using SHAP.
- Compare different budget allocation strategies under a fixed investment constraint.
- Evaluate model limitations and the practical feasibility of model-driven budget recommendations.

## 3. Tech Stack

| Category | Tools & Techniques |
|---|---|
| Programming | Python |
| Data Processing | Pandas, NumPy |
| Machine Learning | LightGBM, Scikit-learn |
| Cross-validation | TimeSeriesSplit |
| Hyperparameter Optimization | Optuna |
| Model Interpretability | SHAP |
| Visualization | Matplotlib, Seaborn |

## 4. Project Workflow

### Step 1: Data Cleaning & Feature Engineering

- Cleaned and processed granular advertising time-series data.
- Handled missing values, data inconsistencies, and feature formatting.
- Conducted feature engineering to extract relevant advertising performance indicators.
- Organized historical advertising data into a structured format for model training.

### Step 2: Revenue Prediction Modeling

Developed a LightGBM regression model to predict advertising revenue.

Key techniques:

- **TimeSeriesSplit:** Applied time-series cross-validation to preserve chronological order and reduce the risk of data leakage.
- **LightGBM:** Built a gradient boosting regression model to capture nonlinear relationships between advertising features and revenue.
- **Optuna:** Optimized model hyperparameters through automated hyperparameter search.
- **SHAP:** Analyzed feature contributions to understand the key drivers behind revenue predictions.

### Step 3: Budget Allocation Simulation

Designed a simulation framework to compare three advertising budget allocation strategies under the same total budget constraint.

| Strategy | Description |
|---|---|
| Equal Allocation | Distributes the total budget equally across advertising channels. |
| Historical ROI-based Allocation | Allocates more budget to channels with better historical ROI. |
| Model-driven Allocation | Uses predicted advertising revenue and expected ROI to guide budget distribution. |

**Simulation Setup:**

- Total Budget: RMB 10,000
- Allocation Constraint: Fixed total budget across all strategies
- Evaluation Metrics: Expected Revenue and Expected ROI

### Step 4: Business Analysis & Model Validation

- Compared allocation results across different strategies.
- Evaluated model recommendations against advertising business logic.
- Identified potential single-channel revenue bottlenecks.
- Examined cross-month prediction biases and model limitations.
- Summarized potential improvements to enhance the robustness of budget allocation recommendations.

## 5. Key Results

Under a simulated total advertising budget of RMB 10,000:

| Metric | Result |
|---|---:|
| Total Budget | RMB 10,000 |
| Best Allocation Strategy | Model-driven Allocation |
| Highest Expected ROI | 10.72 |
| Expected Revenue Improvement vs. Equal Allocation | +68.8% |

The simulation suggests that incorporating machine learning predictions into budget allocation can improve expected advertising returns compared with an equal allocation strategy.

## 6. Key Skills Demonstrated

- **Data Processing:** Data cleaning, feature engineering, time-series data preparation.
- **Machine Learning:** LightGBM regression, model training, and evaluation.
- **Model Optimization:** TimeSeriesSplit, Optuna hyperparameter tuning.
- **Model Interpretability:** SHAP feature importance and prediction analysis.
- **Business Analytics:** ROI analysis, budget allocation, and strategy comparison.
- **Simulation & Decision Support:** Fixed-budget optimization and scenario evaluation.

## 7. Future Improvements

- Incorporate additional time-related features to better capture seasonality and cross-month variations.
- Explore more advanced time-series forecasting approaches.
- Introduce allocation constraints such as minimum channel budgets and diminishing marginal returns.
- Evaluate allocation strategies using rolling-window backtesting.
- Further investigate the stability of model predictions across different time periods.

## 8. Conclusion

This project demonstrates an end-to-end data science workflow, from advertising data preprocessing and revenue prediction to model interpretation and budget allocation simulation.

By combining machine learning with business-oriented simulation, the project explores how predictive analytics can support more informed advertising investment decisions.
