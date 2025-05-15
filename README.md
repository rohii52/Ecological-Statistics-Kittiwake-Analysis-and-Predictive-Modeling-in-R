# Ecological Statistics: Kittiwake Analysis & Predictive Modeling in R

## Overview
This repository contains a **statistical analysis** on **kittiwakes**, a gull species, using **Applied Statistics & Probability** methods. The research provides insights into kittiwake population dynamics by examining **observation, historical, measurement, and location data**.

The project addresses the ornithologist's **research questions**, covering topics such as:
- Exploratory Data Analysis
- Confidence Intervals
- Correlation and Independence Tests
- Linear Regression Modeling

The statistical analysis was conducted using **R Studio**.

---

## Datasets
The provided datasets include:

- **Observation Data**: Number of kittiwake sightings at dawn, noon, mid-afternoon, and dusk over 4 weeks.
- **Historical Data**: Number of breeding pairs at **five different sites** over **five years**.
- **Measurement Data**: Weight, wing span, and culmen (beak length) of **black-legged** and **red-legged** kittiwakes.
- **Location Data**: Breeding pairs in **29 colonies**, with environmental covariates (**temperature, cliff height, sandeel concentration, and coastal direction**).

---

## Research Questions & Methodology

### **1. Exploratory Analysis of Observation Data**
- Conducted **Exploratory Data Analysis (EDA)** with summary statistics.
- **Histogram visualizations** of kittiwake sightings at dawn, noon, and dusk.
- Constructed a **99% confidence interval** for the mean number of kittiwakes observed at dawn:
  - **Confidence Interval:** (95.92, 114.58)
  - Used **t-test** as the data followed a normal distribution.

### **2. Historical Data & Hypothesis Testing**
- Investigated if the **decline in kittiwake numbers** is independent of the site.
- Conducted a **Chi-squared test**:
  - **Chi-square value**: 30.513
  - **p-value**: 0.06196 (marginally non-significant)
  - Visual trends suggested potential site-specific declines.
- Estimated the **breeding pairs at Site E in 2006** using **linear interpolation**:
  - **Estimated breeding pairs:** 67.4

### **3. Measurement Data Analysis**
#### **(a) Visual Summary**
- Generated **scatter plots, histograms, and box plots** for weight, wingspan, and culmen length.

#### **(b) Independence Between Wingspan & Culmen**
- **Black-legged Kittiwakes**:
  - **Correlation coefficient**: 0.33 (p = 0.1951, not significant)
- **Red-legged Kittiwakes**:
  - **Correlation coefficient**: 0.48 (p = 0.07314, moderate positive correlation)

#### **(c) Weight Differences Between Sub-species**
- Conducted a **Welch’s Two-Sample t-test**:
  - **p-value**: 0.8938 (No significant difference in weights)

#### **(d) Overall Differences Between Sub-species**
- **MANOVA test** showed no strong evidence of substantial differences between the two sub-species.

### **4. Location Data & Linear Modeling**
#### **(a) Linear Model for Breeding Pairs**
- Fit a **multiple linear regression model**:
  - **Adjusted R²** = 0.9171 (91.71% variability explained)
  - **Significant predictor:** Cliff height (p < 0.001)

#### **(b) Log-Transformed Model**
- Improved model fit with **Adjusted R² = 0.9866**

#### **(c) Model Selection & Covariates**
- Best model selected using **AIC-based stepwise regression**
- **Significant variables:**
  - **Cliff height (p < 0.001)**
  - **Summer temperature (p = 0.02073)**
  
#### **(d) Prediction for a Given Site**
- **Predicted breeding pairs at Site (South, sandeel = 1.36, temp = 23.5, cliff = 3.99):**
  - **Estimate** = 303.14
  - **80% Confidence Interval:** (250.87, 355.41)

---

## Repository Structure
```
├── Dataset
│   ├── Historical.csv (Breeding Pairs Data)
│   ├── Location.csv (Location Data)
│   ├── Measurement.csv (Weight, Wing Span, Culmen Data)
│   ├── Observation.csv (Kittiwake Sightings Data)
│
├── Paperwork
│   ├── Paperwork.pdf (Research Report)
│   ├── RMD File.pdf (R Markdown Code & Analysis)
│   ├── Rohith Questions.pdf (Assignment Questions)
│
├── Source Code
│   ├── Code.Rmd (R Code for Statistical Analysis)
│
└── README.md (Project Documentation)
```

---

## Installation & Usage
### **1. Clone Repository**
```bash
git clone https://github.com/yourusername/Applied-Statistics-Probability.git
cd Applied-Statistics-Probability
```

### **2. Load the Data**
- Ensure the CSV datasets are in the **Dataset/** folder before running the scripts.

### **3. Run the Analysis in R**
```r
source('Source Code/Code.Rmd')
```

---

## Conclusion
This research successfully applies **statistical methods** to analyze kittiwake population trends. The key takeaways include:
- **Observation data** supports a **99% confidence interval for dawn sightings**.
- **Historical data** suggests **potential site-specific declines**.
- **Measurement data** shows **moderate correlation** between wing span and culmen.
- **Location-based modeling** identifies **cliff height as a key predictor of breeding pairs**.

Future studies can explore:
- **Advanced statistical modeling**
- **Multivariate regression techniques**
- **Time-series forecasting for long-term trends**

---

## Author
[Rohith Ganesan](https://github.com/rohi52)

---

## References
1. Kittiwake Population Research
2. Applied Statistics & Probability Coursework (MTHS4005)
3. Statistical Methods in R

For further information, refer to **Paperwork.pdf** in this repository.
