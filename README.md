# Spectrum Shades LLC — Production Data Cleaning & Quality Analysis

This project analyzes production data for **Spectrum Shades LLC**, a supplier of concrete color pigments.  
The goal is to clean the production dataset, validate data accuracy, and generate insights into factors affecting inconsistent color quality.

This project was completed as part of a **DataCamp Python Data Associate Practical Exam**.

---

## 🔍 Business Problem

Spectrum Shades LLC has recently experienced an increase in customer complaints about inconsistent color quality in their concrete pigments.  
To address this, the data team must:

- Validate and clean production data  
- Standardize categorical and numeric fields  
- Analyze how supplier type and pigment quantity affect product quality  
- Identify patterns that may contribute to color variation  

The analysis focuses on improving product reliability and reducing customer dissatisfaction.

---

## 🛠️ Skills Used

- Python (Pandas, NumPy)  
- Data Cleaning & Preprocessing  
- Missing Value Imputation  
- GroupBy Aggregations  
- Filtering & Conditional Logic  
- Statistical Analysis (Mean, SD, Correlation)  

---

## 📂 Project Tasks

### **Task 1 — Clean the Production Dataset**
Using `production_data.csv`, the dataset was cleaned according to strict criteria:

- `raw_material_supplier`:  
  - 1 → `national_supplier`  
  - 2 → `international_supplier`  
  - Missing → `national_supplier`
- `pigment_type`: missing → `other`
- `pigment_quantity`: missing → median
- `mixing_time`: missing → mean
- `mixing_speed`: missing → `"Not Specified"`
- `product_quality_score`: missing → mean

Output: **`clean_data`** dataframe.

---

### **Task 2 — Supplier Impact Analysis**
Calculated:

- Average pigment quantity  
- Average product quality score  

Grouped by `raw_material_supplier` and rounded to 2 decimals.

Output: **`aggregated_data`** dataframe.

---

### **Task 3 — High‑Pigment Batches (International Supplier)**
Filtered batches where:

- `raw_material_supplier` = `"international_supplier"`  
- `pigment_quantity` > 35 kg  

Returned:

- `raw_material_supplier`  
- `pigment_quantity`  
- `product_quality_score`  

Output: **`pigment_data`** dataframe.

---

### **Task 4 — Statistical & Correlation Analysis**
Computed:

- Mean & standard deviation of `pigment_quantity`  
- Mean & standard deviation of `product_quality_score`  
- Pearson correlation coefficient between the two variables  

Rounded to 2 decimals.

Output: **`product_quality`** dataframe.

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `Spectrum Shades LLC.pdf` | Original DataCamp practical exam submission |
| `production_data.csv` | Raw production dataset |
| `clean_data_frame.py` | Data cleaning function |
| `aggregate_data.py` | Supplier analysis |
| `filter_data.py` | High‑pigment batch filter |
| `calculate_statistics.py` | Statistical and correlation analysis |

---

## 🧠 Key Insights

- National suppliers produced batches with higher average quality scores.  
- International suppliers used lower pigment quantities on average.  
- Several high‑pigment batches still showed low quality scores, indicating other contributing factors.  
- Correlation analysis helps determine whether pigment quantity influences product quality.  

---

## 👤 Author

**Bala Akhil Rajdeep Battula**  
Data & Technology Professional → Automotive Technology (WDTC Fall 2026)
