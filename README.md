# Conduct a Statistical Analysis Using Python

Statistical analysis of the **Breast Cancer Wisconsin (Diagnostic)** dataset, completed as Project 2 — Data and Statistical Reasoning in Udacity's AI Mastery program.

**Analytical question:** Do malignant and benign breast masses differ in mean nuclear radius, and how large is the difference?

## Key result

Malignant samples had a larger mean nuclear radius than benign samples (17.46 vs. 12.15). A two-sided Welch's t-test rejected the null hypothesis of equal means (t = 22.21, p < 0.001), with a 95% confidence interval of 4.85–5.79 for the difference. The two groups still overlap, so radius alone cannot classify every sample.

## Contents

| File | Description |
|---|---|
| `analysis.ipynb` | Data loading and screening, descriptive statistics, four visualizations, Welch's t-test |
| `module_summary.pdf` | Written statistical analysis report with citations |
| `wdbc.csv` | Original UCI `wdbc.data` file, renamed (no header row) |
| `wdbc.names` | UCI documentation of the dataset and its 32 columns |
| `requirements.txt` | Exact package versions (`pip freeze`) |

## Methods

- **Data screening:** checked types, missing values and duplicates before analysis (none found; 569 rows × 32 columns)
- **Descriptive statistics:** summary statistics, skewness, class counts, radius by diagnosis
- **Visualizations:** histogram, boxplot with data points, Spearman correlation heatmap, bar chart
- **Hypothesis test:** Welch's two-sample t-test (unequal variances, variance ratio ≈ 3.2), α = 0.05, with a 95% confidence interval

## How to run

Requires Python 3.9+.

```bash
git clone https://github.com/vutran-us/conduct-a-statistical-analysis-using-python.git
cd conduct-a-statistical-analysis-using-python
python3 -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook analysis.ipynb
```

Run all cells top to bottom (**Kernel → Restart Kernel and Run All Cells**).

## Dataset and license

Wolberg, W., Mangasarian, O., Street, N., & Street, W. (1993). *Breast Cancer Wisconsin (Diagnostic)* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5DW2B

The dataset is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). It is redistributed here unmodified, apart from the file being renamed from `wdbc.data` to `wdbc.csv`.

## Author

Vu Tran — [GitHub](https://github.com/vutran-us)
