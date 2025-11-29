
# Confidence Intervals Calculation – Titanic Dataset

##  Overview
This notebook demonstrates how to calculate **Confidence Intervals (CI)** for the Titanic dataset using **T-Procedure**.  
We use T-Procedure because:
- Population standard deviation (σ) is unknown.
- We rely on **sample standard deviation (s)** and **t-distribution**.

The notebook covers:
1. **Data Preparation**:
   - Merge Titanic train and test datasets.
   - Clean and preprocess data (focus on `Fare` column).
2. **Sampling**:
   - Perform multiple random samples (e.g., 10 samples).
   - Each sample size = 30 (suitable for t-table lookup).
3. **Calculations**:
   - Compute sample mean (\(\bar{X}\)) for each sample.
   - Compute sample standard deviation (s) for each sample.
   - Calculate **Confidence Interval** using T-Procedure:
     \[
     CI = \bar{X} \pm t_{\alpha/2, df} \times \frac{s}{\sqrt{n}}
     \]
     - Where:
       - \( t_{\alpha/2, df} \) = t critical value from t-table.
       - \( df = n - 1 \).
       - \( s \) = sample standard deviation.
       - \( n \) = sample size.
4. **Confidence Levels**:
   - Demonstrate CI for different confidence levels:
     - 95% (standard).
     - 50% (narrower interval).
     - 99% (wider interval).
   - Show how CI width changes with confidence level.
5. **Visualization**:
   - Plot CI ranges for each sample.
   - Compare intervals visually.

---

## Why T-Procedure?
- Z-Procedure assumes population SD is known → Not practical.
- T-Procedure adjusts for uncertainty using **t-distribution**:
  - Fatter tails for small samples.
  - Depends on **degrees of freedom (df = n − 1)**.
- As sample size increases:
  - t-distribution approaches normal distribution.

---

##  Key Observations
- **Confidence Level ↑ → CI width ↑**.
- **Confidence Level ↓ → CI width ↓**.
- **Sample Size ↑ → CI width ↓ (with diminishing returns)**.
- Using Z when σ is unknown → Incorrect coverage (e.g., 95% claim but actual ~92%).

---


