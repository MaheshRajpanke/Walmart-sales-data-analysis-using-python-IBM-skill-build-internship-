# Walmart sales data analysis using python (IBM-skill-build-internship)


## Project Overview

A complete end-to-end Python data analytics project using five years of Walmart retail
transaction data (2019–2023) from 100 stores across 98 Texas cities. The project covers
data inspection, cleaning, exploratory data analysis (EDA), KPI computation, business
insights, and recommendations — all inside a single fully executable Jupyter Notebook.

---

## Objectives

1. Understand the structure and quality of the raw Walmart transaction dataset.
2. Clean and standardise the data for analysis.
3. Explore sales patterns across time, categories, payment methods, and store locations.
4. Compute key business KPIs (revenue, gross profit, margin, basket value, rating).
5. Identify the most profitable and highest-potential product categories.
6. Provide actionable, data-backed business recommendations.

---

## Dataset

| Property          | Value                                       |
|-------------------|---------------------------------------------|
| **Source**        | Kaggle — Walmart Sales Dataset              |
| **Kaggle Link**   | https://www.kaggle.com/datasets/mikhail1681/walmart-sales |
| **Raw file**      | `Walmart org.csv`                           |
| **Raw rows**      | 10,051                                      |
| **Raw columns**   | 11                                          |
| **Cleaned file**  | `Walmart_cleaned.csv`                       |
| **Cleaned rows**  | 9,969                                       |
| **Cleaned columns** | 18                                        |
| **Period**        | 2019-01-01 to 2023-12-31                    |
| **Stores**        | 100 branches across 98 Texas cities         |

### Column Descriptions (original)

| Column           | Description                                            |
|------------------|--------------------------------------------------------|
| `invoice_id`     | Unique transaction identifier (1–10,000)               |
| `Branch`         | Store code (WALM001–WALM100)                           |
| `City`           | City where the store is located                        |
| `category`       | Product category (6 categories)                        |
| `unit_price`     | Price per unit (stored as "$xx.xx" string)             |
| `quantity`       | Units purchased per transaction (1–10)                 |
| `date`           | Transaction date (DD/MM/YY format)                     |
| `time`           | Transaction time (HH:MM:SS format)                     |
| `payment_method` | Payment type: Cash, Ewallet, Credit card               |
| `rating`         | Customer satisfaction score (3.0–10.0)                 |
| `profit_margin`  | Category-level profit margin fraction (0.18–0.57)      |

---

## Technologies Used

| Library      | Version  | Purpose                                  |
|--------------|----------|------------------------------------------|
| Python       | 3.12     | Core language                            |
| pandas       | 3.0.5    | Data loading, cleaning, aggregation      |
| numpy        | 2.5.3    | Numerical operations                     |
| matplotlib   | 3.11.2   | Static charts and visualizations         |
| seaborn      | 0.13.2   | Statistical plots (heatmaps, violins)    |
| plotly       | 7.0.0    | Interactive charts                       |
| nbformat     | 5.11.1   | Notebook creation utilities              |
| nbconvert    | 7.17.1   | Notebook execution and export            |
| ipykernel    | 7.3.0    | Jupyter kernel                           |

---

## Setup Instructions

### 1. Clone / Download the project

```bash
# Place all files in the same directory
Walmart org.csv
Walmart_cleaned.csv
Mahesh_WalmartDataAnalytics.ipynb
requirements.txt
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter

```bash
jupyter notebook
# or
jupyter lab
```

---

## How to Run the Notebook

1. Open `Mahesh_WalmartDataAnalytics.ipynb` in Jupyter.
2. Ensure `Walmart org.csv` and `Walmart_cleaned.csv` are in the **same folder** as the notebook.
3. Click **Kernel → Restart & Run All**.
4. All 45 code cells execute in order; the notebook is fully self-contained.

> The notebook performs cleaning internally from `Walmart org.csv` and also reads
> `Walmart_cleaned.csv` for downstream analysis. Both files must be present.

---

## Project Structure

```
walmart-analytics/
│
├── Walmart org.csv                              # Original raw dataset (do not modify)
├── Walmart_cleaned.csv                          # Cleaned dataset (output of Section 4)
├── Mahesh_WalmartDataAnalytics.ipynb            # Main analysis notebook
├── Mahesh_WalmartDataAnalytics_ProjectReport.docx  # Full project report
├── requirements.txt                             # Python dependencies
└── README.md                                    # This file
```

---

## Key Findings

| Finding | Detail |
|---------|--------|
| Total Revenue (2019–2023) | **$1,209,726** |
| Total Gross Profit | **$476,139** |
| Overall Gross Margin | **39.4%** (stable every year) |
| Average Basket Value | **$121.35** |
| Average Customer Rating | **5.83 / 10** |
| Category concentration | Fashion accessories + Home & lifestyle = **90.7% of transactions** |
| Highest basket value category | Sports & Travel at **$316.25 avg** |
| Highest margin category | Sports & Travel at **57% gross margin** |
| Peak trading hour | **15:00 (3 PM)** — 15:00–20:59 = **63.9% of daily traffic** |
| Seasonal peak | November + December = **49.7% of annual transactions** |
| Best-rated payment | Ewallet: **6.48 / 10** vs Cash/Card: **5.42 / 10** |
| Top branch by revenue | **WALM009** |
| Top city by revenue | **Weslaco** (has 2 branches) |
| Rating vs spend correlation | **~0.00** — satisfaction is independent of purchase size |

---

## Future Scope

1. **Customer segmentation** using clustering (K-Means) to identify high-value vs casual shoppers.
2. **Demand forecasting** with time-series models (Prophet, ARIMA) to predict monthly sales.
3. **Basket analysis** (association rules, Apriori) to discover cross-category buying patterns.
4. **Geospatial analysis** using Texas city coordinates to map revenue density across the state.
5. **Sentiment analysis** on customer reviews (if available) to complement the numeric rating column.
6. **Inventory optimisation model** based on seasonal peaks and category-level demand curves.
7. **Price elasticity study** to test whether unit price changes affect quantity purchased.

