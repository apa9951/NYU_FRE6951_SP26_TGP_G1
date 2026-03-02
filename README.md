# NYU_FRE6951_SP26_TGP_G1  
## Sustainability Investment – ESG News Sentiment & Market Risk

### A. Project Overview

This project investigates whether ESG-related news sentiment can serve as an early warning indicator for short-term market risk. Using structured news tone data from GDELT and market data from Yahoo Finance, we examine the relationship between ESG news sentiment and equity market volatility.

The objective is to evaluate whether negative ESG sentiment precedes elevated market risk and whether incorporating sentiment signals improves short-term risk monitoring.

---

### B. Research Focus

We define **short-term risk** as a 5-day rolling volatility window.  
The study evaluates:

- The relationship between ESG news tone and short-term market volatility  
- Whether lagged sentiment variables have predictive power  
- The robustness of results across alternative volatility windows and threshold definitions  

---

### C. Data Sources

- **GDELT Project** – ESG-related news tone (TimelineTone API)
- **Yahoo Finance (yfinance)** – SPY and ESGU daily price data
- Sample period: One-month event-based window surrounding an ESG-related financial event

---

### D. Methodology

1. News filtering using predefined ESG keyword queries  
2. Extraction of daily average Tone scores  
3. Construction of rolling averages (3-day and 5-day) to smooth noise  
4. Computation of 5-day and 20-day rolling volatility  
5. Regression analysis (OLS and Lasso with cross-validation)  
6. Early-warning classification using high-volatility percentile thresholds (75th and 80th)  
7. Robustness checks across alternative specifications  

---

### E. Key Findings

- Negative ESG sentiment is associated with higher short-term volatility  
- Lagged sentiment (t-2 to t-5) remains statistically relevant  
- Results are stable across different volatility windows and threshold levels  
- Rolling smoothing improves signal clarity and reduces noise impact  

---

### F. Repository Structure
NYU_FRE6951_SP26_TGP_G1/
│
├── ESG_Project_Final.ipynb
├── requirements.txt
├── figures/
│ ├── fig1_tone_distribution.png
│ ├── fig2_time_series.png
│ ├── fig3_esg_subindex.png
│ └── ...
└── report/
└── Final_Report.pdf


---

### G. How to Run

1. Install required packages:
pip install -r requirements.txt

2. Open the Jupyter Notebook:
ESG Final Project - Muhideen Ogunlowo and Azfina.ipynb

3. Run all cells sequentially.

---

### H. Limitations

- GDELT Tone scores are broad and not ESG-calibrated  
- Short sample window limits external generalizability  
- Correlation does not imply causation  

---

### Thank You

Muhideen Ogunlowo and Azfina Anindita – FRE 6951  
NYU Tandon School of Engineering  
Spring 2026

---


