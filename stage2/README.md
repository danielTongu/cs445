# CS445 Final Project: Visualizing Credit Card Fraud Patterns Within PCA-Transformed Data

**Team Members:** Fisher, Cole, Daniel  
**Supervisor:** Dr. Zhu  
**Date:** May 9, 2025  

---

## Introduction
This project analyzes the **Kaggle Credit Card Fraud Detection** dataset, which contains **284,807 European credit card transactions** from September 2013. The dataset presents unique challenges due to its **PCA-transformed features** and **extreme class imbalance** (only 0.17% fraud rate). Our goal is to develop innovative visualization techniques to uncover patterns in fraudulent transactions.

### Dataset Description  
- **Attributes:**  
  - **Time** (numeric): Seconds elapsed since the first transaction (range: 0–172,792s ≈ 48 hours).  
  - **Amount** (numeric): Transaction value in Euros (range: €0.01–€25,691.16).  
  - **V1–V28** (numeric): Principal components from PCA transformation (ranges vary by component).  
  - **Class** (binary): `0` for legitimate transactions, `1` for fraudulent transactions.  

- **Key Characteristics:**  
  - Highly dimensional (31 features).  
  - Extremely imbalanced (492 frauds vs. 284,315 legitimate transactions).  
  - Anonymized features for confidentiality.  

### Research Questions  
1. **Temporal Patterns:** Do fraud attempts follow discernible time patterns? Are there peak hours/days for fraudulent activity?  
2. **Behavioral Signals:** What transaction amount ranges are most vulnerable? Do PCA components reveal consistent fraud signatures?  
3. **Detection Strategies:** Can we identify visual thresholds for fraud screening? What multidimensional patterns characterize frauds?  

---

## Visualization Proposals  

### Member 1: **Cole** – Temporal & Amount Analysis  
1. **Transaction Amount Distribution by Class**  
   - *Type:* Overlaid histograms (log-scale) for fraud vs. legitimate transactions.  
   - *Goal:* Determine if fraud targets small (stealth) or large (high-value) transactions.  

2. **Time vs. Amount Scatter Plot**  
   - *Type:* Scatter plot colored by fraud status.  
   - *Goal:* Visualize high-risk time-amount combinations.  

3. **Fraud Hourly Heatmap**  
   - *Type:* Calendar heatmap (hours vs. days) with fraud counts.  
   - *Goal:* Identify peak fraud periods (e.g., midnight, weekends).  

---

### Member 2: **Daniel** – PCA Component Exploration  
1. **Fraud Cluster Scatter Plot**  
   - *Type:* 2D scatter plot (V1 vs. V2) colored by class.  
   - *Goal:* Visualize if fraud forms clusters in PCA space.  

2. **PCA Component Radar Chart**  
   - *Type:* Radar chart comparing mean values of V1–V5 for fraud vs. normal transactions.  
   - *Goal:* Identify which transformed dimensions differ most.  

3. **Component Correlation Heatmap**  
   - *Type:* Heatmap of V1–V10 correlations with Amount/Time.  
   - *Goal:* Find relationships between interpretable and transformed features.  

---

### Member 3: **Fisher** – Comparative & Composite Visuals  
1. **Parallel Coordinates Plot**  
   - *Type:* Parallel plot of Time, Amount, and top 3 PCA components.  
   - *Goal:* Reveal multidimensional fraud patterns.  

2. **Fraud Proportion by Amount Bracket**  
   - *Type:* Bar chart showing % fraud in different amount ranges.  
   - *Goal:* Quantify risk levels for transaction sizes.  

3. **Cumulative Fraud Timeline**  
   - *Type:* Area chart showing fraud accumulation over 48 hours.  
   - *Goal:* Detect "fraud bursts" suggesting coordinated attacks.  

---

## Conclusion  
Our **9 visualizations** strategically overcome dataset limitations by:  
1. Focusing on interpretable features (Time, Amount, Class).  
2. Using PCA components only where patterns can be meaningfully observed.  
3. Employing complementary views (temporal, comparative, multidimensional).  

All visualizations are implemented in **Python** using **Matplotlib/Seaborn**, with interactive elements via **Plotly** where beneficial.  

--- 

**Expected Contributions:**  
- Novel visualization techniques for PCA-transformed financial data.  
- Methodology for analyzing extreme class imbalance.  
- Actionable insights for fraud detection systems.  