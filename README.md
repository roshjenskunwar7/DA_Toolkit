# Data Analysis Toolkit

**A complete, browser-based data analysis toolkit — no installation, no coding, no server required.**

## 

## What it does

Upload any CSV file and instantly get a full professional statistical analysis. The toolkit auto-detects your column types, runs the correct tests, and explains every result in plain English.

\---

## Modules

|#|Module|What's inside|
|-|-|-|
|1|**Explorer**|Row/column counts, column types, missing value heatmap, data preview|
|2|**Statistics**|Summary table, variable detail + interpretation, frequency tables|
|3|**Charts**|Histogram + KDE, box plot, scatter plot, bar chart, correlation matrix|
|4|**Distributions**|Interactive PDF/CDF explorer, Q-Q plot, goodness-of-fit tests|
|5|**Inference**|Full hypothesis test suite (see below)|
|6|**Regression**|OLS regression, R², RMSE, residual plot, prediction|
|7|**Probability Calc**|P(X≤x), P(X≥x), P(a≤X≤b), inverse CDF|

\---

## Complete Hypothesis Test Suite

### Normality Tests

|Test|What it checks|
|-|-|
|Shapiro-Wilk|Overall shape normality|
|Jarque-Bera|Normality via skewness and kurtosis|
|Kolmogorov-Smirnov|Empirical vs theoretical CDF|

### Group Comparison Tests

|Test|When used|
|-|-|
|Welch's two-sample t-test|Two groups, variable is Normal|
|Mann-Whitney U|Two groups, variable is NOT Normal (non-parametric)|
|One-way ANOVA|Three or more groups, variable is Normal|
|Kruskal-Wallis|Three or more groups, variable is NOT Normal (non-parametric)|
|Paired t-test|Two related measurements on the same subjects|

### Variance Tests

|Test|What it checks|
|-|-|
|Levene's test|Equal variances across groups (robust to non-normality)|
|Bartlett's test|Equal variances across groups (assumes normality)|

### Proportion \& Categorical Tests

|Test|When used|
|-|-|
|One-proportion Z-test|Test if a category's proportion equals a target value|
|Chi-squared independence|Association between two categorical variables|
|Fisher's exact test|Association in 2×2 tables (exact p-value, good for small samples)|

### Other Tests

|Test|When used|
|-|-|
|One-sample t-test|Does the mean equal a specific value?|
|Confidence interval|Range likely containing the true population mean|
|Pearson r|Linear correlation between two Normal variables|
|Spearman ρ|Rank correlation when variables are non-Normal|
|Simple linear regression|Predict one variable from another (OLS)|

### Auto-Test Engine

The toolkit automatically selects the correct parametric or non-parametric test for each column pair based on normality. Up to 15 tests are run and ranked by significance.

\---

## Effect Sizes

Every test reports an effect size alongside the p-value:

|Measure|Used in|Small|Medium|Large|
|-|-|-|-|-|
|Cohen's d|t-tests|0.2|0.5|0.8|
|Eta-squared η²|ANOVA|0.01|0.06|0.14|
|Cramér's V|Chi-squared, Fisher|0.1|0.3|0.5|
|r / ρ|Correlation|0.1|0.3|0.5|

\---

## How to Use

1. **Open** `index.html` in any browser (Chrome, Firefox, Edge, Safari)
2. The **built-in employee dataset** loads automatically — explore immediately
3. Click **Upload CSV** (top right) to load your own data
4. Use the **tabs** at the top to navigate between modules

No internet required after the first page load. No installation. No coding.

\---

## Loading Your Own CSV

* File must be `.csv` (comma-separated values)
* First row must be column headers
* Numbers should not contain currency symbols or commas (`5000` not `$5,000`)
* Missing values are handled automatically (filled with column median for numeric)

**Tips for unlocking all tests:**

* Include at least one **numeric** and one **categorical** column
* A **binary column** (exactly 2 categories: Yes/No, Male/Female) enables t-tests, proportion tests, and Fisher's exact test
* A **multi-category column** (3–15 categories) enables ANOVA and chi-squared

\---

## p-value Guide

|p-value|Interpretation|
|-|-|
|p < 0.001|Very strong evidence against H₀|
|p < 0.01|Strong evidence against H₀|
|p < 0.05|Significant — reject H₀|
|p < 0.10|Marginal|
|p ≥ 0.10|Insufficient evidence to reject H₀|

\---

## Files

```
DA-Toolkit/
├── index.html    ← The complete toolkit (single file, \~1 MB)
└── README.md     ← This file


