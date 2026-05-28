# Astro-Statistical Analysis: Investigating Zodiac Signs & Personality Traits

[![R Language](https://img.shields.io/badge/Language-R-blue.svg)](https://www.r-project.org/)
[![Python](https://img.shields.io/badge/Language-Python-green.svg)](https://www.python.org/)
[![Academic Project](https://img.shields.io/badge/Coursework-Hochschule%20Mittweida-darkred.svg)](https://www.hs-mittweida.de/)

Can the alignment of the stars at your birth predict your personality, or is it all just a cosmic coincidence? This repository contains the data, statistical workflows, and findings of an empirical study investigating the relationship between **Sidereal (Vedic) Zodiac signs** and self-reported personality traits. 

Conducted as part of the *Selected Topics in Computational Statistics* curriculum at **Hochschule Mittweida University of Applied Sciences**, Germany, this research utilizes quantitative data from over 80 surveyed individuals to test the validity of horoscopic descriptions through rigorous statistical hypothesis testing.

---

## 📊 Executive Summary & Key Findings

* **Personality vs. Zodiac:** Using Chi-Square tests for independence and correlation matrices, the study found **no statistically significant association** ($p > 0.05$) between an individual's True Vedic Zodiac sign and their assumed personality traits. 
* **Demographics of Belief:** Belief in astrology was found to be independent of age, gender, and geographic background.
* **Socioeconomic Trends:** Descriptive exploratory data analysis (EDA) revealed an inverse behavioral relationship: self-reported belief in astrology noticeably **decreases** as formal education levels and household financial status increase.

---

## 🛠️ Methodology & Tech Stack

### Data Collection & Preprocessing
* **Primary Data:** Collected custom survey responses ($N=80+$, predominantly localized to Mangaluru, Karnataka, India) using a structured 30-question, **7-level Likert Scale**.
* **Astronomical Standardization:** Transformed raw dates and birth times into exact Sidereal Zodiac signs using precise geographic coordinates (Latitude/Longitude) to adjust for local solar time and earth's axial precession.
* **Data Cleaning:** Processed, handled missing values, and isolated outliers using **Microsoft Excel** and **R (dplyr)**.

### Statistical Framework
* **Chi-Square ($\chi^2$) Tests for Independence:** Applied to evaluate binary cross-contingency tables (e.g., target zodiac vs. baseline distribution) to audit trait alignment.
* **Correlation Metrics:** Generated Pearson/Spearman coefficients to look for latent positive or negative linear dependencies.
* **Data Visualization:** Built box plots, stacked distribution bars, and coordinate $p$-value trend charts.

### Tech Stack
* **R Environment:** `dplyr`, `ggplot2`, `stats`
* **Python Environment:** `Pandas`, `NumPy`, `Seaborn`, `Matplotlib`
* **Spreadsheets:** Microsoft Excel (Initial tallying and filtering)

---

## 📈 Key Visualizations Explained

### 1. Chi-Square $p$-Value Thresholds
The calculated $p$-values across all 12 astrological signs consistently crossed the critical $\alpha = 0.05$ threshold. Because we fail to reject the null hypothesis ($H_0$), we statistically confirm that the traits of individuals belonging to a specific sign are not meaningfully different from the rest of the general population.

### 2. Socioeconomic Trends (Box Plots)
Visual distribution matrices show a distinct downward shift in astrological belief markers among postgraduate academic profiles and affluent income brackets, highlighting strong demographic patterns in alternative belief systems.

---

## 📂 Repository Structure

```text
├── data/
│   └── survey_responses_cleaned.csv   # Anonymized & standardized dataset
├── notebooks/
│   ├── eda_and_visualization.ipynb    # Python-based exploratory plotting
│   └── hypothesis_testing.R           # R script for Chi-Square and correlations
├── reports/
│   └── Project_Report_Presentation.pdf # Full academic poster summary
└── README.md
