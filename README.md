# Insurance Claims & Policyholder Risk Analysis (Power BI)

This Power BI dashboard provides insights into insurance claims and policyholder risk.  
It helps identify high-risk customers, analyze claims patterns, and assess premium adjustments.

---

## 📊 Dashboard Highlights

**KPIs**
- **4972** Total Claims  
- **0.50** Avg Claims per Policyholder  
- **368K** Total Claims Adjustment  
- **73.97** Average Claim Amount  
- **10K** Total Records  

**Visuals**
- 📊 **Bar Chart**: Count of Records by Claims Severity (Low/Medium/High)  
- 🍩 **Donut Chart**: Count of Records by Region (Urban, Suburban, Rural)  
- 🔹 **Scatter Plot**: Claims Frequency vs Premium Amount (with trend line)  
- 📊 **Stacked Column Chart**: Count of Records by Age (bins) and Claims Severity  
- 📊 **100% Stacked Bar Chart**: Claim Severity distribution across Regions  
- 📊 **Treemap**: Policyholder distribution by Marital Status  

**Filters (Slicers)**
- Policy Type (Full Coverage, Liability-Only)  
- Region (Rural, Suburban, Urban)  
- Source of Lead (Agent, Online, Referral)  
- Marital Status (Divorced, Single, Married, Widowed)  

---

## 🧮 DAX Measures

```DAX
Total Claims =
SUM ( 'synthetic_insurance_data'[Claims_Frequency] )

Avg Claims per Policyholder =
AVERAGE ( 'synthetic_insurance_data'[Claims_Frequency] )

Claims Adjustment Impact =
SUM ( 'synthetic_insurance_data'[Claims_Adjustment] )

Average Claim Amount =
DIVIDE (
    SUM ( 'synthetic_insurance_data'[Claims_Adjustment] ),
    SUM ( 'synthetic_insurance_data'[Claims_Frequency] ),
    0
)

---

Hi
