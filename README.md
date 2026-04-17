📊 ENIAC A/B Testing – Homepage Experiment
Statistical Analysis • Chi‑Square Test • CTR Evaluation


🏷️ Badges

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Colab](https://img.shields.io/badge/Run%20in-Colab-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Analysis](https://img.shields.io/badge/Method-A/B%20Testing-purple)


🎯 Project Overview
Analyzed four homepage versions (A, B, C, D) from the ENIAC case study

Evaluated user engagement using CTR, drop‑off rate, and homepage‑return rate

Performed statistical testing to determine significant performance differences

Created visualizations to support insights

Identified the best‑performing version for deployment

🧪 Methods Used
🔹 1. Data Cleaning & Preparation
Loaded CSV files for all four versions

-->Extracted:
    
    Total visits

    CTA clicks

-->Calculated:

    CTR

Prepared contingency tables for chi‑square testing

🔹 2. Statistical Testing
Global Chi‑Square Test to check if differences between versions are statistically significant

Post‑hoc Pairwise Chi‑Square Tests with Bonferroni correction

Identified which version pairs differ significantly

🔹 3. Visualization
CTR bar chart

CTR with 95% confidence intervals

Drop‑off rate comparison

Homepage‑return rate comparison

📊 Key Results
✔ Global Chi‑Square Test
p‑value < 0.05

Conclusion: Significant difference exists between the four versions

✔ Post‑hoc Pairwise Results
Significant differences
A > B

A > D

C > B

C > D

Not significant
A vs C → Similar CTR performance

✔ CTR & Drop‑off Insights
Version C has the highest CTR

Version A is very close, and the difference is not statistically significant

Version A has better behavioral metrics (lower drop‑off, higher homepage‑return rate)

Versions B and D underperform consistently

🏆 Final Recommendation
⭐ Adopt Version A as the new homepage CTA button.
Why Version A wins
CTR statistically equal to Version C

Lowest drop‑off rate among top performers

Highest homepage‑return rate

Strong, consistent performance across all metrics

🛠 Tools & Technologies
markdown
- Python  
- Pandas  
- NumPy  
- SciPy  
- Seaborn / Matplotlib  
- Google Colab  
- GitHub
-  
🚀 How to Run the Notebook
Open the notebook in Google Colab
Upload the CSV files from the Data/ folder
Run all cells sequentially

Review statistical outputs and visualizations

👩‍💻 Author
Pavani Bandla  
A/B Testing & Data Analysis – ENIAC Case Study






