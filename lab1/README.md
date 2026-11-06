**English** | [Українська](README.uk.md)

[← Back to repository](../README.md)

# Lab 1. Dota 2: most picked heroes

## Goal

Analyse Dota 2 pick and ban data with Pandas, find the 10 most frequently picked heroes and visualise the result as a bar chart.

## Data

Files for the notebook (upload them to the Colab session, path `/content/`):

- `picks_bans.csv` — picks and bans of heroes (columns used: `hero_id`, `is_pick`);
- `Constants.Heroes.csv` — hero reference (columns used: `id`, `localized_name`).

The data files are not stored in this repository.

## What the notebook does

1. Reads both CSV files with `pd.read_csv()`.
2. Keeps only picks (`is_pick == True`), dropping bans.
3. Counts picks per hero with `value_counts()`.
4. Adds hero names via `merge()` on `hero_id` = `id`.
5. Takes the top 10 and prints the table.
6. Draws a bar chart with Matplotlib.

## Result

| # | Hero | Picks |
|---|------|-------|
| 1 | Rubick | 6561 |
| 2 | Tiny | 5877 |
| 3 | Jakiro | 5611 |
| 4 | Shadow Fiend | 5217 |
| 5 | Queen of Pain | 5071 |
| 6 | Ogre Magi | 5024 |
| 7 | Pudge | 4688 |
| 8 | Tusk | 4681 |
| 9 | Mars | 4620 |
| 10 | Dragon Knight | 4585 |

## How to run

1. Open `lab1_dota2_top_heroes.ipynb` in Google Colab.
2. Upload `picks_bans.csv` and `Constants.Heroes.csv` to the session files (left panel → Files).
3. Run all cells.

## Skills practised

Filtering with boolean masks, `value_counts()`, `merge()`, selecting the top rows, bar charts with Matplotlib.
