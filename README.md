# ApexPlanet Data Analytics Internship - Task 1: Data Immersion & Wrangling

Profiling, cleaning and preparing a 1,000-row sales dataset for analysis using Python and pandas.

## Files
| File | Description |
|------|-------------|
| `data_dictionary.md` | Every column: meaning, type, business relevance, plus engineered columns |
| `data_quality_report.md` | Issues found, how each was handled, assumptions |
| `data_cleaning.py` | Profiling + cleaning + feature engineering script |
| `cleaned_sales_dataset.csv` | Final analysis-ready dataset (1,000 rows x 28 columns) |

## How to run
```bash
pip install pandas numpy openpyxl
python data_cleaning.py "ApexPlanet_DataAnalytics_Dataset.xlsx"
```
The raw Excel file must be in the same folder. The script prints a quality profile and saves `cleaned_sales_dataset.csv`.

## Key findings
- 20 missing ages and 13 missing cities
- 8 duplicate Order_IDs, restored using the sequential ID pattern
- Dates stored as text, 5 orders dated outside 2025
- 52 Customer_IDs shared by different customers
- 19 high-value outliers, flagged and kept

## Tech stack
Python 3, pandas, NumPy
