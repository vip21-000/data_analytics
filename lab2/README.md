**English** | [Українська](README.uk.md)

[← Back to repository](../README.md)

# Lab 2. Pandas: working with tables

## Goal

Learn the main Pandas structures (`DataFrame` and `Series`), import data from files, inspect it, and perform indexing, filtering and sorting of tabular data.

## Data

`coffee_sales.csv` — coffee shop sales, over 4 000 records, 6 columns:

| Column | Description |
|--------|-------------|
| `date` | date of the sale |
| `datetime` | date and time of the sale |
| `cash_type` | payment type (`card` / `cash`) |
| `card` | anonymised card ID (empty for cash) |
| `money` | transaction amount |
| `coffee_name` | name of the drink |

## What the notebook does

1. Creates a `DataFrame` from a dictionary (books table).
2. Reads the CSV into a `DataFrame` and inspects it: `head()`, `tail()`, `info()`, `describe()`, `columns`.
3. Selects data with `loc` and `iloc`.
4. Filters rows with boolean masks (`cash_type == 'card'`, `Latte` and `money > 30`).
5. Sorts by `datetime` (after `pd.to_datetime`) and by `money`.
6. Saves the filtered and sorted result to CSV.
7. Extra task: a function that counts records per category with `value_counts()` and sorts them in descending order.
8. Answers to the self-check questions.

## How to run

1. Upload `coffee_sales.csv` to the root of your Google Drive (`MyDrive`).
2. Open `lab2_pandas_tables.ipynb` in Google Colab.
3. Run all cells and allow access to Google Drive when asked.

If the file has another name or location, change the `PATH` variable in the data loading cell.

## Skills practised

`DataFrame` and `Series`, `read_csv` / `to_csv`, `loc` / `iloc`, boolean masks with `&`, `sort_values`, `to_datetime`, `value_counts`.
