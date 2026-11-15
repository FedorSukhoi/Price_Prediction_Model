# House Price Prediction

A coursework project for Kaggle’s [House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques), predicting house sale prices from the Ames Housing dataset.

## Approach

- Explore feature distributions, missing values and relationships with SalePrice.
- Distinguish absent amenities from genuinely missing information.
- Split labelled data into 80% training and 20% validation.
- Encode categorical features by meaning and log selected area features and the target.
- Engineer features describing age, total area, bathrooms, amenities and quality.
- Compare regression models across preprocessing versions.
- Tune Linear Regression, Ridge and Random Forest with five-fold GridSearchCV, fitting preprocessing separately within each fold.
- Refit selected models on all labelled data and generate Kaggle submissions.

## Evaluation

Models are compared using training and validation R² and RMSE on log prices.

| Submitted model | Kaggle score ↓ |
|---|---:|
| Random Forest | **0.13211** |
| Ridge | 0.13642 |
| Linear Regression | 0.14367 |

## Files

- **start.ipynb** — exploration, preprocessing, model comparison, tuning and submission code.
- **train.csv / test.csv** — competition datasets.
- **data_description.txt** — feature definitions.
- **sample_submission.csv** — required submission format.
- **submission.csv / submission2.csv / submission3.csv** — Ridge, Random Forest and Linear Regression predictions.
- **model_results.csv / tuning_results.csv** — saved evaluation results.

## Running

Install the dependencies:

```bash
python -m pip install numpy pandas matplotlib seaborn scikit-learn jupyter kaggle
```

Open **start.ipynb** with **HW_Comp** as the working directory and run the analysis cells in order. Kaggle authentication is required for uploads; run submission cells separately when ready.