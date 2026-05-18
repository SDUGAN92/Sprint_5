# Project Overview: Video Game Sales Forecasting (Ice Online Store)

## 📌 Project Background

This project focuses on a real-life analytical case study for the international online video game store, **Ice**. The dataset contains historical open-source data running up to 2016, including global game sales, user/expert reviews, genres, platform categories (e.g., Xbox, PlayStation), and Entertainment Software Rating Board (ESRB) age ratings.

### 🎯 Core Business Objective

Imagine it is **December 2016**, and Ice is mapping out its retail and advertising strategy for the upcoming **2017 calendar year**. The objective is to identify critical, data-driven patterns that determine whether a video game succeeds or fails. By uncovering these metrics, the store can spot potential "big winners," optimize inventory, and plan highly targeted, profitable marketing campaigns.

---

## 🛠️ Integrated Project Workflow

The project is structured into six key development phases inside a Jupyter Notebook, executing a complete data science lifecycle:

### Step 1: Data Assessment & Overview

* **File Path:** `/datasets/games.csv`
* **Objective:** Load and examine the structural features of the data.
* **Key Variable Challenges:** Identifying structural issues with missing entries, checking row dimensions, and noting that 2016 data may be incomplete.

### Step 2: Rigorous Data Preprocessing

* **Formatting:** Standardizing all column names to lowercase for clean code syntax.
* **Type Casting:** Converting data categories to correct logical types (e.g., converting scores or dates) and documenting the exact engineering reasoning.
* **Missing Value Engineering:** Investigating the root causes behind missing values and establishing an imputation or exclusion strategy. Special attention is paid to isolating and handling the **"TBD" (To Be Determined)** values in user scores.
* **Feature Engineering:** Creating a new `total_sales` column combining regional sales metrics ($NA\_sales + EU\_sales + JP\_sales + Other\_sales$).

### Step 3: Exploratory Data Analysis (EDA)

* **Historical Release Trends:** Tracking the volume of games released per year to identify relevant analytical periods.
* **Platform Lifecycle Analysis:** Analyzing sales shifts from platform to platform. This involves tracking how long it takes for new consoles to peak and legacy systems to fade out, allowing us to choose a precise **relevant time window** to build the 2017 prognosis.
* **Visualizing Global Volume:** Utilizing **Box Plots** to compare global sales distributions across platforms and check for significant differences in averages.
* **Review Impact Studies:** Building **Scatter Plots** and calculating correlation coefficients to see exactly how professional critic scores vs. user scores influence sales on a chosen baseline platform, then comparing those trends against other systems.
* **Genre Dominance:** Mapping out distributions by genre to distinguish high-volume profit generators from low-grossing niches.

### Step 4: Regional User Profiling

To optimize localized advertising budgets, distinct profiles are developed for three major geographic markets (**North America (NA), Europe (EU), and Japan (JP)**):

* Isolating the **top five platforms** and calculating variations in market share.
* Identifying the **top five genres** to pinpoint regional gaming preferences.
* Evaluating whether **ESRB ratings** systematically affect regional sales performance differently.

### Step 5: Statistical Hypothesis Testing

Using statistical criteria and a custom alpha ($\alpha$) threshold to test key consumer behavior assumptions:

1. **Hypothesis 1:** * $H_0$: The average user ratings of the Xbox One and PC platforms are equal.
* $H_1$: The average user ratings of the Xbox One and PC platforms are different.


2. **Hypothesis 2:** * $H_0$: The average user ratings for the Action and Sports genres are equal.
* $H_1$: The average user ratings for the Action and Sports genres are different.



### Step 6: General Conclusion

Synthesizing all visual findings, data treatments, and statistical test results into an actionable commercial recommendation for Ice's 2017 strategy.
