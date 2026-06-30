# Superstore Sales Analysis

This project contains an exploratory data analysis of the Sample Superstore dataset using Python and Jupyter Notebook.

The main analysis lives in [notebook/Superstore_EDA.ipynb], with the source dataset in [data/SampleSuperstore.csv].

## Project Goal

The analysis focuses on:

- understanding overall sales and profit performance
- comparing categories, sub-categories, regions, and shipping modes
- identifying loss-making areas
- examining the relationship between discounting and profitability

## Project Structure

- `notebook/Superstore_EDA.ipynb`: main EDA notebook
- `data/SampleSuperstore.csv`: raw dataset
- `cleaned_data/Superstore_Cleaned.csv`: cleaned dataset export

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Data Cleaning Performed

The notebook applies the following cleaning steps:

- checked for missing values
- removed duplicate rows
- converted `Postal Code` to string
- standardized column names by replacing spaces with underscores
- stripped extra spaces from `City`
- normalized `Region` text casing

After duplicate removal, the working dataset contains `9,977` rows.

## Key Metrics

- Total sales: `2,296,195.59`
- Total profit: `286,241.42`
- Total units sold: `37,820`
- Overall profit margin: `12.47%`

Note: `37,820` is the sum of `Quantity`, not the number of unique orders.

## Key Insights

- `Technology` is the top-performing category by both sales (`836,154.03`) and profit (`145,454.95`).
- `Furniture` generates strong sales (`741,306.31`) but weak profit (`18,421.81`), making it the least efficient major category.
- The `West` region leads revenue with `725,255.64` in sales.
- `Phones` and `Chairs` are the biggest sales-driving sub-categories.
- `Tables` is the largest profit-losing sub-category at `-17,725.48`.
- The biggest loss-making states are `Texas`, `Ohio`, and `Pennsylvania`.
- Higher discount levels are associated with lower profit, and heavily discounted transactions tend to become loss-making.
- `Standard Class` is the dominant shipping mode by sales contribution.



## How To Run

1. Open the notebook:

```bash
jupyter notebook notebook/Superstore_EDA.ipynb
```

2. Run the cells from top to bottom.

## Summary

The business story is straightforward: sales strength comes mainly from `Technology` and the `West`, while profit leakage is concentrated in `Furniture`, especially `Tables`, and in a few states where discounting appears too aggressive.
