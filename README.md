## 📊 A/B Testing Case Study – Homepage Versions A/B/C/D

![Python](https://img.shields.io/badge/Python-3.10-blue)  
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)  
![AB Testing](https://img.shields.io/badge/A%2FB_Testing-Statistical_Analysis-green)  
![License](https://img.shields.io/badge/License-MIT-yellow)  
![Updated](https://img.shields.io/badge/Last_Updated-April_2026-purple)


## 🎯 This repository contains an A/B test analysis comparing four homepage variants (A, B, C, D). The analysis evaluates click-through rate (CTR), performs a global chi-square test and Bonferroni-corrected pairwise chi-square tests, and inspects behavioral metrics (drop-off and homepage-return rates) to determine the best-performing design.

--------------------------------------------------------------------------------------------------------------------------------

## 🔍 TL;DR  —  Recommendation

Version A is the recommended homepage. Although Version C has the highest raw CTR, its CTR is statistically indistinguishable from A and A outperforms C on behavioral metrics (notably lower drop-off and higher homepage-return rate), making A the strongest balanced choice for deployment.

---------------------------------------------------------------------------------------------------------------------------------
📁 Data used

Visits: A=25,326;  B=24,747;  C=24,876;  D=25,233
CTA clicks :  A=512;  B=281;  C=527;  D=193

Source files:  Notebooks/Eniac_case_A_B_test_structure.ipynb  and CSVs referenced in the notebook (Google Drive link ).

--------------------------------------------------------------------------------------------------------------------------------

## 📊 Key results


CTRs (rounded): A=2.02% | B=1.14% | C=2.12% | D=0.76%
Global chi-square test: chi2 = 224.0188; p-value ≈ 2.716e-48 → reject H₀ (differences exist among variants).
Pairwise (Bonferroni-corrected) chi-square results: A vs B (significant), A vs C (NOT significant, p≈0.446), A vs D (significant), B vs C (significant), B vs D (significant), C vs D (significant).

---------------------------------------------------------------------------------------------------------------------------------

Interpretation:  Only A and C are statistically indistinguishable on CTR.
95% confidence intervals for CTRs overlap between A and C, supporting the same conclusion.







<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/d308c178-d267-46d2-a286-26e27c4e51a0" />






---------------------------------------------------------------------------------------------------------------------------------
## 🧠 Decision Logic
Use global chi-square to detect any difference across all variants.
Run Bonferroni-corrected pairwise chi-square tests to locate significant differences.

📊 Pairwise Chi‑Square Test Results

| Comparison | p-value | Result          |
|-----------|---------|-----------------|
| A vs B    | 0.000   | 🔥 Significant  |
| A vs C    | 0.446   | ✅ Not Significant |
| A vs D    | 0.000   | 🔥 Significant  |
| B vs C    | 0.000   | 🔥 Significant  |
| B vs D    | 0.000   | 🔥 Significant  |
| C vs D    | 0.000   | 🔥 Significant  |



When CTR ties occur (A vs C), use behavioral metrics (drop-off rate, homepage-return rate) to break ties.
Version A wins due to balanced performance across CTR and behavioral metrics.

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/d20c7f39-87ee-46b5-934f-4fb2444bb0b3" />      <img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/13183895-4cad-46c8-b4c1-5926f1d9df82" />






---------------------------------------------------------------------------------------------------------------------------------

## 🛠️How to run

Clone the repo:

git clone https://github.com/pavanibandla25/Eniac_case_A-B-_testing

---------------------------------------------------------------------------------------------------------------------------------

## Install dependencies:

pip install -r requirements.txt
(or pip install pandas numpy scipy matplotlib seaborn)

Open the notebook in Jupyter/Colab/VS Code: Notebooks/Eniac_case_A_B_test_structure .ipynb

---------------------------------------------------------------------------------------------------------------------------------
## 📂Files of interest

- Notebooks/Eniac_case_A_B_test_structure .ipynb — main analysis and charts
- [Data/](Data/) — CSV files used by the notebook
- README.md — this file

---------------------------------------------------------------------------------------------------------------------------------
## 📝Notes
The notebook sets alpha = 0.10 in one cell but uses alpha = 0.05 and Bonferroni correction for pairwise testing; 
the effective threshold for pairwise tests is 0.05/6.
Some pairwise p-values are displayed rounded to three decimals ("0.000") in the notebook; 
exact p-values can be produced by re-running the notebook or using a small helper script.

---------------------------------------------------------------------------------------------------------------------------------
## 💡 Business Impact 

Choosing Version A improves user engagement while minimizing drop-off, 
leading to a more stable and scalable homepage experience.


---------------------------------------------------------------------------------------------------------------------------------
## 🚀Next steps (suggested)

(Optional)  Re-run pairwise tests to save exact p-values in the notebook output.
Create a short slide or README summary image for stakeholders with the contingency table, CTRs+CI, chi-square statistic, and recommendation.

---------------------------------------------------------------------------------------------------------------------------------
## 👤 Author

Pavani Bandla — Data Analytics Trainee | WBS Coding School

