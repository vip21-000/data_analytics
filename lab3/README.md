**English** | [Українська](README.uk.md)

[← Back to repository](../README.md)

# Lab 3. Data cleaning and transformation

## Goal

Get practical skills in detecting and handling missing values, duplicates and outliers; converting data types; working with string and time values; creating new features; encoding categories; applying normalisation and standardisation; building a reproducible cleaning sequence.

## Data

`index_1.csv` — coffee shop sales (the same dataset as in Lab 2), 6 columns: `date`, `datetime`, `cash_type`, `card`, `money`, `coffee_name`. The file is not stored in this repository.

## What the notebook does

1. Loads the dataset.
2. Missing values: `isnull().sum()`, `dropna()`, `fillna()`.
3. Duplicates: `duplicated()`, `drop_duplicates()`.
4. Outliers: IQR method for `money`.
5. Type conversion: `pd.to_datetime()`.
6. String cleaning: `.str.strip()`, `.str.lower()`, `.str.replace()`.
7. New features from `datetime`: hour, day of week, month.
8. One-hot encoding of `coffee_name` with `pd.get_dummies()`.
9. Min-max normalisation and standardisation of `money`.
10. Saving the cleaned dataset to `cleaned_sales.csv`.
11. **Individual task (variant 7):** feature `is_card` built with `np.where()`.
12. **Extra task (★):** function `clean_dataset(df)` that removes duplicates, converts dates, fills numeric gaps with the median and categorical ones with the mode, and removes IQR outliers; tested on a synthetic dirty dataset.
13. Answers to the self-check questions.

## How to run

1. Open `lab3_data_cleaning.ipynb` in Google Colab.
2. Upload `index_1.csv` to the session files (left panel → Files → Upload), so it is available at `/content/index_1.csv`.
3. Run all cells. Result files (`cleaned_sales.csv`, `cleaned_dirty.csv`) are saved to `/content/`.

## Skills practised

`isnull`, `dropna`, `fillna`, `drop_duplicates`, IQR, `to_datetime`, `.str` and `.dt` accessors, `get_dummies`, min-max scaling, standardisation, `np.where`.
