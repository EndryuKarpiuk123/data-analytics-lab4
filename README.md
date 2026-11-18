# Practical Work No. 4 - Aggregation and Grouping

This repository contains my solution for Practical Work No. 4. The goal of the work is to gain practical skills in using `groupby` and aggregate functions; building pivot tables and cross-tabulations; combining datasets with `concat`, `merge` and `join`; calculating analytical indicators by group; and interpreting aggregation results.

## Repository contents

| File / folder | Description |
|---------------|-------------|
| `karpiuk_lb4.ipynb` | Practical part (Steps 1-10): `groupby` with one and several columns, `agg()`, `pivot_table()`, `crosstab()`, `merge`, `concat`, `join`, and revenue share by group. |
| `karpiuk_tasks4.ipynb` | Individual tasks 1-7 and the additional ★ task (custom two-table dataset), plus answers to the self-check questions. |
| `results/` | CSV files produced by the ★ task (see below). |
| `README.md` | This file. |

### `results/` folder

| File | Description |
|------|-------------|
| `merged_orders.csv` | `orders` and `products` tables merged with `merge()`, with a calculated `revenue` column. |
| `revenue_by_category.csv` | Total revenue, average revenue and number of orders per product category (`groupby` + `agg`). |
| `pivot_category_city.csv` | Pivot table: total revenue by category and city. |

## Dataset

The notebooks use `sales.csv` - a coffee shop transactions dataset:

| Column | Description |
|--------|-------------|
| `date` | Transaction date |
| `datetime` | Transaction date and time |
| `cash_type` | Payment type (`card` / `cash`) |
| `card` | Anonymised card identifier (empty for cash payments) |
| `money` | Transaction amount |
| `coffee_name` | Name of the drink |

If `sales.csv` is not found on Google Drive, the notebooks automatically generate a synthetic sample with the same structure (600 rows), so every cell can be run without extra preparation. The ★ task uses its own small dataset (`products` and `orders` tables) created directly in the notebook.

## How to run

1. Open [Google Colab](https://colab.research.google.com) and sign in with your Google account.
2. Choose **File → Upload notebook** and select one of the `.ipynb` files (or open it directly from GitHub).
3. Upload `sales.csv` to the root of your Google Drive (`MyDrive`), or skip this step to use the generated sample.
4. Run the cells in order with **Shift + Enter**. When prompted by `drive.mount('/content/drive')`, grant access to your Drive.

> Note: the ★ task saves its CSV files to the `results` folder on Google Drive.

## Requirements

- Python 3 (pre-installed in Google Colab)
- `pandas`
- `numpy`

## What was covered

- Grouping by one and several columns: `groupby()`, `size()`, `reset_index()`
- Aggregate functions: `sum`, `mean`, `min`, `max`, `count`, and several at once with `agg()`
- Pivot tables with `pd.pivot_table()` and cross-tabulations with `pd.crosstab()`
- Combining data: `merge()` (with `how='left'`), `concat()` (index handling, `ignore_index`), `join()`
- Calculating analytical indicators by group (revenue share, profit, average check by hour)
- Saving aggregation results to CSV

## Author

Karpiuk
