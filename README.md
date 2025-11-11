# IQR-OutlierHandling
# 📊 Detecting Outliers Using IQR Method  
**AI Generated README**

---

## 📘 Overview
This experiment demonstrates how to **detect and handle outliers using the Interquartile Range (IQR) method**.  
We analyze **CGPA**, **Placement Exam Marks**, and **Placement Status** to identify and treat outliers effectively.

---

## ⚙️ Steps and Process

### **1. Dataset and Initial Observation**
- Dataset is available in the repository.  
- Columns used: **CGPA**, **PlacementExamMarks**, **Placed**.  
- **Distribution plots** were created for both features.  
  🖼️ *Image 1 attached.*

**Observations:**
- **CGPA** → Normally distributed (skewness = -0.014, negligible).  
- **Placement Exam Marks** → Right skewed (skewness = 0.82).  
  → IQR method is suitable for this feature.  

**Summary Stats for Placement Marks:**
- Mean = 32  
- Min = 0  
- Max = 100  

---

### **2. Box Plot Analysis**
- Box plot created for **PlacementExamMarks**.  
  🖼️ *Image 2 attached.*  
  → Shows a large number of outliers on the higher side.

---

### **3. Calculating IQR**
1. Calculated **25th (Q1)** and **75th (Q3)** percentiles for placement marks.  
2. Computed **IQR = Q3 - Q1**.  
3. Determined limits:
   - **Upper Limit = Q3 + (1.5 × IQR)**  
   - **Lower Limit = Q1 - (1.5 × IQR)**  

**Results:**
- Upper Limit = **84.5**  
- Lower Limit = **23.5**

---

### **4. Detecting Outliers**
- Checked data points:
  - Above 84.5 → **Outliers found**
  - Below 23.5 → **None**

---

### **5. Handling Outliers**

| Method | Description | Result |
|--------|--------------|---------|
| **Trimming** | Removed rows above upper limit | Distribution remained almost same; outliers removed |
| **Capping** | Replaced outliers with max/min values | Slight spike at extreme right (due to capping with max value) |

🖼️ *Image 3:* Distribution and box plot after trimming  
🖼️ *Image 4:* Distribution and box plot after capping  

---

## 📎 Attachments
<img width="1321" height="448" alt="iqr 1" src="https://github.com/user-attachments/assets/8174caa9-3305-4db4-9c80-c1e33c737394" />

- Initial distribution of CGPA & Placement Marks.  
- <img width="571" height="394" alt="iqr2" src="https://github.com/user-attachments/assets/108743af-c3ae-41fb-9778-a97449a99ef8" />
Box plot before outlier handling.  
- <img width="1328" height="448" alt="iqr3" src="https://github.com/user-attachments/assets/d22efcfb-dfdc-43be-8e68-12c9b8843f90" />
 After trimming (outliers removed).  
- <img width="1320" height="448" alt="iqr4" src="https://github.com/user-attachments/assets/4d48c47a-07a1-48c1-b9c1-c95aea8bbc14" />
 After capping (spike at right end).

---

## 🧩 Key Insights
- CGPA shows no significant outliers; Placement Marks does.  
- IQR method effective for **right-skewed** data.  
- **Trimming** gives a cleaner distribution, while **Capping** retains data size but alters shape slightly.  

---

> ⚠️ *This README is AI-generated and describes the detection and handling of outliers using the IQR method in a structured, experiment-style format.*
