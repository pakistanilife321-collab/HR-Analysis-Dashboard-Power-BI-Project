# HR-Analysis-Dashboard-Power-BI-Project
📌 Executive Summary 
This project analyzes employee attrition to help HR leadership identify key drivers behind staff turnover and improve retention strategies. The interactive Power BI dashboard examines employee demographics, salary brackets, job roles, and tenure patterns across departments.
## 📸 Dashboard Preview
![HR analysis dashboard](images/HR_analysis_dashboard.png)

---

## 📊 Key Insights & Metrics
* **Total Employees:** 1,470
* **Attrition Count & Rate:** 237 employees (16.1% Attrition Rate)
* **Average Metrics:** Employee Age: 37 years | Average Salary: $6.5K | Tenure at Company: 7 years
* **Salary Impact:** Attrition is highest among employees earning **up to $5K/month**, pointing to compensation as a primary retention risk.
* **Tenure Pattern:** Departure rates peak during **Year 1**, highlighting the need for stronger early onboarding programs.
* **Job Satisfaction:** Laboratory Technicians and Sales Representatives record lower satisfaction scores paired with higher exit counts.

---

## 🛠️ Data Modeling & Technical Implementation
* **Data Sources:** HR Dataset containing employee demographics, performance ratings, and compensation data.
* **Data Transformation (Power Query):**
  * Cleaned missing values and standard data types.
  * Created conditional columns for **Salary Slabs** (e.g., Up to 5k, 5k-10k) and **Age Groups** (18-25, 26-35, 36-45, 55+).
* **Key DAX Measures:**
  * `Total Employees = COUNT(HR_Analytics[EmpID])`
  * `Attrition Count = CALCULATE(COUNT(HR_Analytics[EmpID]), HR_Analytics[Attrition] = "Yes")`
  * `Attrition Rate = DIVIDE([Attrition Count], [Total Employees], 0)`

---

## 📂 Repository Structure
```text
├── data/
│   └── HR_Analytics_Data.csv
├── images/
│   └── dashboard_screenshot.png
├── HR_Analytics_Dashboard.pbix
└── README.md
