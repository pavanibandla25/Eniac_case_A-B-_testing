# 📊 A/B Testing Eniac_Case Study – Homepage “SHOP NOW” & “SEE DEALS” Button Analysis
This project analyzes four homepage CTA button designs (Versions A, B, C, and D) to determine which version drives the highest user engagement. The analysis uses real visitor and click data from the ENIAC case study and applies statistical testing to identify the winning variant.

--## 🔍 Project Overview
The goal of this A/B test is to evaluate how different button designs impact user behavior on the homepage.  
We compare four versions:

- **Version A**
- **Version B**
- **Version C**
- **Version D**

Each version received **different numbers of visitors**, and user actions (clicks, drop‑offs) were recorded.

---
## 📈 Methods Used

### **1. Data Cleaning & Preparation**
- Loaded CSV files for all four versions  
- Extracted visits, clicks, and drop‑off counts  
- Calculated CTR and drop‑off rates  

### **2. Statistical Testing**
- **Global Chi‑Square Test** to check if differences between versions are statistically significant  
- **Post‑hoc Pairwise Chi‑Square Tests** with Bonferroni correction to identify which versions differ  

### **3. Visualization**
- CTR bar chart  
- Drop‑off bar chart  
- CTR with 95% confidence intervals  

---

## 📊 Key Results

### **✔ Global Chi‑Square Test**
- p‑value < 0.05  
- **Conclusion:** There is a statistically significant difference between the four versions.

### **✔ Post‑hoc Pairwise Results**
Significant differences:
- C > B  
- C > D  
- A > B  
- A > D  

Not significant:
- A vs C (similar performance)

### **✔ CTR & Drop‑off Insights**
- **Version C has the highest CTR**
- **Version C has the lowest drop‑off**
- B and D consistently underperform

---

## 🏆 Final Recommendation

### **Adopt Version C as the new homepage CTA button.**

**Why Version C wins:**
- Highest click‑through rate  
- Lowest drop‑off rate  
- Statistically significant improvement over B and D  
- Strong, consistent performance across all metrics  

---

## 🛠 Tools & Technologies

- Python  
- Pandas  
- NumPy  
- SciPy  
- Seaborn / Matplotlib  
- Google Colab  
- GitHub  

---

## 📌 How to Run the Notebook

1. Open the notebook in **Google Colab**  
2. Upload the CSV files from the `Data/` folder  
3. Run all cells sequentially  
4. View statistical results and charts  

---

## 👩‍💻 Author

**Pavani Bandla**  
A/B Testing & Data Analysis – ENIAC Case Study  



