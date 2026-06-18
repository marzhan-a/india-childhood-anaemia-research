# Determinants of Childhood Anaemia in India: Does Household Head Gender Matter?

This repository contains the core components of a quantitative research project analyzing the socio-economic and demographic drivers of childhood anaemia in India, using large-scale survey data. 

## Repository Contents
* **`Research-Project-Report.Rmd`**: The complete R Markdown source script, including data cleaning, variable recoding, descriptive statistics, visualization code (`ggplot2`), and multivariate logistic regression models.
* **`Research-Project-Report.pdf`**: The final compiled research report presenting the comprehensive analysis, structured regression tables, and policy discussions.

## Project Overview & Methodology

### 1. Objective & Hypothesis
The study evaluates whether the gender of the household head significantly influences childhood anaemia outcomes in India. It tests the primary null hypothesis:
$$H_{0}: \beta_{1} = 0$$
Where $\beta_{1}$ represents the coefficient for female-headed households in a logit model framework.

### 2. Dataset & Sample Size
* **Source:** India Standard Demographic and Health Survey (DHS).
* **Sample Size:** Filtered down to a final clean sample of **168,175 observations** of children after accounting for missing values and data cleaning steps.
* *Note: In compliance with DHS data redistribution policies, the raw and cleaned data files are excluded from this public repository.*

### 3. Model Progression
The analysis employs three nested multivariate logistic regression models to isolate the effect of household head gender while controlling for compounding factors:
* **Model 1:** Baseline model testing only the primary explanatory variable (household head gender).
* **Model 2:** Adds child and maternal characteristics (e.g., child's age, maternal education).
* **Model 3:** Incorporates broader environmental and household wealth controls (e.g., regional state groups, wealth index).

## Key Findings

* **The Gender Paradox:** While the baseline model initially suggests a statistically significant relationship, the effect completely disappears once maternal and socioeconomic characteristics are controlled for. Ultimately, the study **fails to reject the null hypothesis**, finding that household head gender is *not* a statistically significant independent determinant of childhood anaemia.
* **Maternal Education:** Mother's highest education level emerged as one of the most powerful and consistent protective factors against childhood anaemia across all models. Higher levels of maternal education heavily correlate with a decreased likelihood of a child being anaemic.
* **Geographic Variations:** Significant regional disparities persist, highlighting that environmental and state-level infrastructure play a critical role in childhood health outcomes.

## Required R Packages
If you wish to replicate the analysis locally using your own authorized DHS dataset, the `.Rmd` file requires the following packages:
* `tidyverse` (for data manipulation and visualization)
* `stargazer` or `broom` (for clean regression outputs)
* `car` (for multicollinearity checks)
