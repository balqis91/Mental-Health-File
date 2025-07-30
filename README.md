# 🧠 Mental Health Disorder Dashboard

## 📌 Overview  
This project provides a detailed **Mental Health Analytics Dashboard** built with **Power BI**.  
It analyzes data on **mental health disorders, depression, suicide rates, and behavioral metrics** across multiple countries and years.  

The dashboard aims to:  
- Track prevalence of mental health disorders globally  
- Highlight trends in depression and suicide rates  
- Compare behavioral metrics across different regions  
- Explore gender-based prevalence in mental health issues  

---

## 🧹 Data Cleaning & Preparation  

Before creating the dashboard, extensive **data cleaning and preparation** was carried out:

1. **Data Validation**  
   - Checked for missing or invalid values in population and disorder metrics  
   - Removed duplicate patient and country records  

2. **Data Standardization**  
   - Converted all years to a consistent `DATE` format  
   - Normalized country and entity names for consistency  

3. **Feature Engineering**  
   - Created calculated fields for **Suicide Rate by Depression**  
   - Segmented population by **Gender (Male vs Female)**  
   - Aggregated behavioral metrics (Anxiety, Bipolar, Schizophrenia, etc.)  

4. **Modeling for Power BI**  
   - Developed a **star schema** with Fact tables (mental health metrics) and Dimension tables (countries, gender, time)  
   - Built a **Date Dimension Table** for trend analysis  

---

## 📊 Dashboards  

### 📍 Mental Health Disorder Dashboard  
<img width="1297" height="727" alt="image" src="https://github.com/user-attachments/assets/dc6b515b-9669-4243-a405-5ac8942b4be8" />


### 📍 Data Model  
<img width="1103" height="375" alt="image" src="https://github.com/user-attachments/assets/e839f1ce-2abf-485a-bad3-2b3429978848" />

### 📍 Key Influencers Analysis  
<img width="1282" height="705" alt="image" src="https://github.com/user-attachments/assets/a1010f8f-c182-4881-89fd-ef26714d5f86" />


**Key Findings from Key Influencers Visual:**  
- Depression (%) is more likely to increase when:  
  - Male prevalence exceeds **3.5%** (+0.79 increase)  
  - Female prevalence exceeds **4.45%** (+0.52 increase)  
  - Alcohol use disorder ≤ **0.65%** (+0.49 increase)  
  - Drug use disorders between **0.51% – 0.57%** (+0.46 increase)  
  - Anxiety disorders between **3.11% – 3.29%** (+0.39 increase)  
- Overall, **male prevalence and alcohol/drug use** are strong indicators of rising depression rates.  

---

## ✅ Database Schema (Conceptual)  

**FactMentalHealth**
- `EntityID` (FK → Dim_Entity)  
- `Year` (FK → Dim_Date)  
- `AnxietyDisorder`  
- `DepressionRate`  
- `DrugUseRate`  
- `SuicideRate`  
- `EatingDisorder`  
- `BipolarDisorder`  
- `SchizophreniaRate`  
- `AlcoholConsumption`  
- `Population`  

**Dim_Entity**
- `EntityID` (PK)  
- `Country`  
- `Region`  

**Dim_Date**
- `Date`  
- `Year`  
- `Month`  
- `Quarter`  

**Dim_Gender**
- `GenderID` (PK)  
- `Gender`  
- `PopulationPercentage`  

---

## 🔍 Key Insights  

- **Global Prevalence:** Over **986M patients** across **49 countries**  
- **Depression Trend:** Steady rise in prevalence since 1990, reaching nearly 8B people in 2020  
- **Behavioral Disorders:** Anxiety disorder (1.04M) and Schizophrenia (51.5K) are most reported  
- **Suicide Rate Correlation:** Each depression rate segment contributes ~20% to suicide rate  
- **Gender Impact:** Slightly higher prevalence in females across most countries  
- **Predictors of Depression:** High male prevalence, female prevalence, and substance use strongly influence depression rates  

---

## 📌 Conclusion  
This dashboard highlights the growing **global challenge of mental health disorders**.  
The analysis provides valuable insights for:  
- **Health policymakers** to allocate resources  
- **NGOs** to target interventions  
- **Researchers** to track behavioral health trends  

**Future Improvements**
- Incorporate **real-time mental health survey data**  
- Add **predictive analytics** for suicide prevention  
- Compare with **economic indicators** (GDP, healthcare funding)  

---

## ⚙️ Tools Used  
- **SQL** – Data cleaning & relational modeling  
- **Power BI** – Visualization & dashboard creation  
- **DAX** – Advanced metrics & Key Influencers Analysis  
- **Data Modeling** – Star schema with fact and dimension tables  

---

👩‍💻 Created by *Balikisu Ajoke Oniyide*
# Mental-Health-File
