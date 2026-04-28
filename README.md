# 📊 A/B Testing Case Study – Homepage Versions A/B/C/D
![Python](https://img.shields.io/badge/Python-3.10-blue)
![License](https://img.shields.io/badge/License-MIT-green)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_NOTEBOOK_URL)






# 🎯 This repository contains an A/B test analysis comparing four homepage variants (A, B, C, D). The analysis evaluates click-through rate (CTR), performs a global chi-square test and Bonferroni-corrected pairwise chi-square tests, and inspects behavioral metrics (drop-off and homepage-return rates) to determine the best-performing design.

---------------------------------------------------------------------------------------------------

# 🔍 TL;DR  —  Recommendation

Version A is the recommended homepage. Although Version C has the highest raw CTR, its CTR is statistically indistinguishable from A and A outperforms C on behavioral metrics (notably lower drop-off and higher homepage-return rate), making A the strongest balanced choice for deployment.
Eniac wants to optimize homepage engagement and reduce user friction. This A/B test compares four CTR designs to identify the most effective version.

---------------------------------------------------------------------------------------------------
# 📁 Data used

Visits: A=25,326;  B=24,747;  C=24,876;  D=25,233
clicks :  A=512;  B=281;  C=527;  D=193

📁 Data Source: [Google Drive Link]( Notebooks/Eniac_case_A_B_test_structure.ipynb)


---------------------------------------------------------------------------------------------------

# 📊 Key results


- CTRs (rounded): A=2.02% | B=1.14% | C=2.12% | D=0.76%

- Global chi-square test:$\chi^2 = 224.02$; p-value < 0.001 → reject H₀ (differences exist among variants).

- Pairwise (Bonferroni-corrected) chi-square results : A vs B (significant), A vs C (NOT significant, p≈0.446), A vs D (significant), B vs C (significant), B vs D (significant), C vs D (significant).

📊 Pairwise Chi‑Square Test Results

| Comparison | p-value | Result          |
|-----------|---------|-----------------|
| A vs B    | 0.000   | 🔥 Significant  |
| A vs C    | 0.446   | ✅ Not Significant |
| A vs D    | 0.000   | 🔥 Significant  |
| B vs C    | 0.000   | 🔥 Significant  |
| B vs D    | 0.000   | 🔥 Significant  |
| C vs D    | 0.000   | 🔥 Significant  |

---------------------------------------------------------------------------------------------------

# Interpretation :   Only A and C are statistically indistinguishable on CTR.
95% confidence intervals for CTRs overlap between A and C, supporting the same conclusion.






<p align="center">
<img width="350" height="350" alt="image" src="https://github.com/user-attachments/assets/d308c178-d267-46d2-a286-26e27c4e51a0" />
</p>





---------------------------------------------------------------------------------------------------
# 🧠 Decision Logic
Use global chi-square(χ²) to detect any difference across all variants.
Run Bonferroni-corrected pairwise chi-square tests to locate significant differences.

When CTR ties occur (A vs C), use behavioral metrics (drop-off rate, homepage-return rate) to break ties.
- Drop-off rate → users leave the funnel early → revenue loss
- Homepage-return rate → users didn’t find what they expected → UX mismatch

Version A wins due to balanced performance across CTR and behavioral metrics.

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/d20c7f39-87ee-46b5-934f-4fb2444bb0b3" />      <img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/13183895-4cad-46c8-b4c1-5926f1d9df82" />






---------------------------------------------------------------------------------------------------

# 🛠️ How to run

Clone the repo:

git clone https://github.com/pavanibandla25/Eniac_case_A-B-_testing
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_NOTEBOOK_URL)


---------------------------------------------------------------------------------------------------

# Install dependencies:

pip install -r requirements.txt
(or pip install pandas numpy scipy matplotlib seaborn)

Open the notebook in Jupyter/Colab/VS Code: Notebooks/Eniac_case_A_B_test_structure .ipynb

---------------------------------------------------------------------------------------------------
# 📂 Files of interest

- Notebooks/Eniac_case_A_B_test_structure.ipynb — main analysis and charts
- [Data/](Data/) — CSV files used by the notebook
- README.md — this file
--------------------------------------------------------------------------------------------------
# 📁 Repository Structure

Eniac_case_A-B-_testing/
```
Eniac_case_A-B-_testing/
├── Data/
│   ├── eniac_a.csv
│   ├── eniac_b.csv
│   ├── eniac_c.csv
│   └── eniac_d.csv
├── Notebooks/
│   └── Eniac_case_A_B_test_structure.ipynb
├── README.md
└── requirements.txt
```

---------------------------------------------------------------------------------------------------
# 📝 Notes
The notebook sets alpha = 0.10 in one cell but uses alpha = 0.05 and Bonferroni correction for pairwise testing; 
the effective threshold for pairwise tests is Bonferroni-corrected α = 0.0083.
Some pairwise p-values are displayed rounded to three decimals ("0.000") in the notebook; 
exact p-values can be produced by re-running the notebook or using a small helper script.

---------------------------------------------------------------------------------------------------
# 💡 Business Impact 

Choosing Version A improves user engagement while minimizing drop-off, 
leading to a more stable and scalable homepage experience.


---------------------------------------------------------------------------------------------------
# 🚀 Next steps (suggested)

(Optional)  Re-run pairwise tests to save exact p-values in the notebook output.
Create a short slide or README summary image for stakeholders with the contingency table, CTRs+CI, chi-square statistic, and recommendation.

---------------------------------------------------------------------------------------------------
# 👤 Author

Pavani Bandla — Data Analytics Trainee | WBS Coding School

