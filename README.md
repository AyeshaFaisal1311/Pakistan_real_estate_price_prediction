# Pakistan Real Estate Price Prediction

Predict the price of houses **for sale** in Pakistan using real listing data from Zameen.com.

**Goal:** compare 2 machine learning models and evaluate them in a fair way.

## Dataset
Download from Kaggle: [Zameen.com Property Data Pakistan](https://www.kaggle.com/datasets/huzzefakhan/zameencom-property-data-pakistan)

- Save the file as `Property.csv` in the project folder before running the notebook (it is not uploaded here because it is large).
- Columns are separated by `;`.
- Only `For Sale` listings are used (about 124,000 rows after cleaning).

## Steps
1. **Preprocessing:** keep sale rows, remove very low prices, change area to marla, remove outliers per property type, fix zero baths and bedrooms
2. **EDA:** price is skewed, price grows with area, price changes by city
3. **Features:** group rare locations, `log(area)`, one-hot encoding, `log(price)` as the target
4. **Models:** Linear Regression (baseline) and Model 2 (coming)
5. **Evaluation:** R2, MAE and median error, in PKR

## Results

| Model | R2 (log) | MAE (PKR) | Median error (PKR) |
|---|---|---|---|
| Linear Regression | 0.89 | 5.6M | 2.2M |
| Model 2 | - | - | - |

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook code_1.ipynb
```
Keep `Property.csv` in the same folder as the notebook.

## Project Files
- `code_1.ipynb`: the full project notebook
- `requirements.txt`: Python packages needed
- `README.md`: this file