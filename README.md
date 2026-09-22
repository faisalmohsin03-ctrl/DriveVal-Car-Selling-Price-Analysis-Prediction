# DriveVal — Car Selling Price Analysis & Prediction

> **IBM SkillsBuild Data Analytics with AI Academic Internship Project**  
> Author: **Faisal Mohsin**

---

## Overview

DriveVal is an end-to-end data analytics and machine learning project built on a large-scale Indian used-car marketplace dataset. The project covers the complete data science workflow — from raw data ingestion and cleaning through exploratory analysis, feature engineering, model training, and evaluation — with the goal of predicting the **selling price** of a used car and surfacing actionable market insights.

---

## Dataset Information

| Property | Detail |
|---|---|
| **File** | [`Car Sell Dataset.csv`](https://www.kaggle.com/datasets/milapgohil/car-dataset) |
| **Rows** | ~140,904 listings |
| **Columns** | 12 |
| **Target Variable** | `Price` (INR) |
| **Source** | Indian used-car marketplace listings |

### Columns

| Column | Type | Description |
|---|---|---|
| Brand | Categorical | Car manufacturer |
| Model Name | Categorical | Vehicle model |
| Model Variant | Categorical | Trim / variant |
| Car Type | Categorical | Hatchback, Sedan, SUV, etc. |
| Transmission | Categorical | Manual / Automatic |
| Fuel Type | Categorical | Petrol, Diesel, CNG, Electric |
| Year | Numeric | Manufacturing year |
| Kilometers | Numeric | Odometer reading |
| Owner | Ordinal | 1st / 2nd / 3rd / 3rd+ owner |
| State | Categorical | Indian state of listing |
| Accidental | Categorical | Yes / No |
| Price | Numeric 🎯 | Selling price in INR |

---

## Technologies Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, manipulation |
| `numpy` | Numerical operations, log transforms |
| `matplotlib` | Low-level plotting |
| `seaborn` | Statistical visualisations |
| `scikit-learn` | ML models, preprocessing, evaluation |
| `jupyter` / `notebook` | Interactive notebook environment |

---

## Setup & Installation

### Prerequisites

- Python **3.9+**
- `pip` package manager

### Install dependencies

```bash
# Clone or download the project folder
cd Car_project

# (Recommended) Create and activate a virtual environment
python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate

# Install all required libraries
pip install -r requirements.txt
```

---

## How to Run the Code

```bash
# Launch Jupyter Notebook
jupyter notebook FaisalMohsin_DriveVal.ipynb
```

Then run all cells in order (**Kernel → Restart & Run All**).

The notebook will:
1. Load and clean `Car Sell Dataset.csv`
2. Perform full EDA with 12+ visualisation plots (saved as `.png` files)
3. Engineer features and prepare the modelling dataset
4. Train four regression models and print evaluation metrics
5. Plot actual vs predicted prices, residuals, and feature importances
6. Export the cleaned dataset as `Car_Sell_Dataset_Cleaned.csv`

---

## Project Structure

```
Car_project/
│
├── Car Sell Dataset.csv               ← Raw dataset
├── FaisalMohsin_DriveVal.ipynb        ← Main analysis notebook
├── requirements.txt                   ← Python dependencies
├── FaisalMohsin_ProjectReport.docx    ← Full project report
├── README.md                          ← This file
│
└── (generated on run)
    ├── Car_Sell_Dataset_Cleaned.csv
    ├── plot_price_distribution.png
    ├── plot_top_brands.png
    ├── plot_avg_price_brand.png
    ├── plot_price_fuel.png
    ├── plot_price_transmission.png
    ├── plot_age_vs_price.png
    ├── plot_km_vs_price.png
    ├── plot_correlation_heatmap.png
    ├── plot_state_listings.png
    ├── plot_yearly_trend.png
    ├── plot_car_type_pie.png
    ├── plot_accidental_price.png
    ├── plot_actual_vs_predicted.png
    ├── plot_residuals.png
    └── plot_feature_importance.png
```

---

## Key Insights & Project Summary

| Finding | Detail |
|---|---|
| 🏆 Best Model | **Gradient Boosting Regressor** (highest R², lowest MAE) |
| 📉 Top Price Driver | **Car age** — newer cars command significantly higher prices |
| ⚡ Fuel Type Impact | Electric > CNG > Diesel > Petrol for median resale value |
| 🔄 Transmission Premium | Automatic cars sell for ~30–50% more than manual equivalents |
| 🚗 Accident Discount | Accidental cars sell ~15–25% cheaper than non-accidental |
| 🗺️ Top Market | Maharashtra leads in listing volume and average price |
| 📏 Km Effect | Prices drop sharply beyond 1,00,000 km |

### Model Performance Summary (approximate)

| Model | R² Score |
|---|---|
| Gradient Boosting | ~0.82 |
| Random Forest | ~0.79 |
| Ridge Regression | ~0.61 |
| Linear Regression | ~0.60 |

---

## Recommendations

- **Sellers** — List before year 5; highlight non-accidental, low-km, single-owner status.
- **Buyers** — Target Electric/CNG, non-accidental, first-owner listings for best value.
- **Platform operators** — Deploy Gradient Boosting as a real-time pricing engine; retrain quarterly.

---

## License

This project is submitted as part of the IBM SkillsBuild Data Analytics with AI Internship 2026 . For educational use only.
