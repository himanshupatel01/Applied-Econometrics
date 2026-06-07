# Applied Econometrics: Socioeconomic Determinants of the Fear of Crime

## 📌 Project Overview
This project applies econometric and statistical methods to analyse the demographic and socioeconomic factors that influence an individual's perceived worry about being a victim of crime. Utilising the **Crime Survey for England and Wales (CSEW) 2017-2018 teaching dataset**, the study evaluates the correlations between personal income, age, gender, education, and ethnicity and public safety perceptions. 

The repository showcases a full data pipeline in R, spanning from structural missing-value filtration to bi-variate statistical testing and multi-variable Ordinary Least Squares (OLS) linear regressions.

---

## 🛠️ Technical Toolkit & R Libraries
* **Language & Environment:** RStudio / R Markdown (`.Rmd`)
* **Core Data Packages:** `tidyverse`, `haven` (SPSS `.sav` file parsing), `dplyr`
* **Visualisation:** `ggplot2` (Jitter plotting, smooth linear trend lines, distribution histograms)
* **Diagnostics & Tables:** `stargazer` (Publication-grade summary statistics and regression modelling comparison tables)

---

## 📈 Key Methodology & Statistical Insights

### 1. Data Cleaning & Exploratory Analysis
* **Missing Value Management:** Programmatically handled hidden missing indicators across continuous and categorical arrays (e.g., negative values filtered to `NA`) to prevent bias.
* **Distribution Mapping:** Plotted sample densities using `ggplot2`, showing a right-skewed metric where most respondents report low-to-moderate levels of crime worry.

### 2. Hypothesis Testing & Mean Comparisons
* **Gender Disparity (t-test):** Executed an independent t-test confirming a highly significant gap (p < 0.01). On average, females report higher baseline worry levels (0.828) than males (0.660), aligning with vulnerability theories in the criminological literature.
* **Ethnic Variation (ANOVA):** Deployed a one-way Analysis of Variance (p < 0.01) showing strong variations across ethnic backgrounds. The highest mean worry was observed among Asian/Asian British respondents (1.290) compared to White respondents (0.708).

### 3. Econometric Modeling & OLS Comparison (N = 3,389)
Two nested linear regression configurations were designed and analysed side-by-side:
* **Baseline Specification:** Evaluated income and age. Income yielded a statistically significant negative coefficient (\(-0.024^{***}\)), confirming that higher financial assets act as a buffer against crime anxiety, potentially due to neighbourhood self-selection. Age proved small and statistically insignificant.
* **Full Extended Model:** Incorporated controls for gender, education, and ethnicity. While income remained robust (\(-0.017^{***}\)), education exerted a strong negative mitigation effect (\(-0.040^{***}\)), showing that access to safety resources scales with educational attainment. Jointly significant ethnic coefficients demonstrated elevated relative worry among Asian (\(0.621^{***}\)) and Black (\(0.431^{***}\)) communities relative to the baseline.
* **Goodness-of-Fit:** Expanding from the baseline to the full specification boosted the model's R² explanatory power from 1.2% to 6.5%.

---
