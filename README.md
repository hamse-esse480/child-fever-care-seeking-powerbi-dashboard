# Child Fever & Care-Seeking Power BI Dashboard

## 📌 Project Overview

An interactive **Power BI dashboard** analyzing healthcare-seeking behavior among caregivers of children experiencing **fever and acute febrile illness (AFI)**.

The dashboard explores caregivers' **knowledge and perceptions, healthcare access, barriers, care-seeking pathways, and the timing of healthcare-seeking**. The analysis focuses particularly on the difference between caregivers who sought care **within 24 hours** and those who sought care **after 24 hours**.

The project transforms caregiver-level data into interactive visualizations and analytical indicators to identify patterns associated with **timely and delayed healthcare-seeking**.

---

## 🎯 Project Objectives

The dashboard was developed to:

* Assess the overall pattern of **timely versus delayed care-seeking**.
* Examine differences in care-seeking by **caregiver characteristics and education level**.
* Explore the relationship between **healthcare access and care-seeking timeliness**.
* Examine caregivers' **knowledge of danger signs and perceptions of fever**.
* Compare **danger signs across timely and delayed care-seeking groups**.
* Analyze caregivers' **first actions when a child develops fever**.
* Examine healthcare facilities and transportation methods used.
* Describe **referral and hospitalization patterns**.
* Explore reported **clinical outcomes**.

---

# 📊 Dashboard Structure

The dashboard is organized into four main analytical pages.

## 1. Executive Overview & Timeliness

This page provides an overall picture of healthcare-seeking behavior.

### Key indicators

* **Total Respondents:** 422
* **Delayed Care-Seeking:** 63.5% (268 respondents)
* **Timely Care-Seeking:** 36.5% (154 respondents)
* **Timely Care:** Within 24 hours
* **Delayed Care:** After 24 hours

### Main analyses

* Timely vs. delayed care-seeking
* Care-seeking by education level
* Care-seeking by facility type
* First action and care-seeking timeliness
* Overall distribution of delayed care

---

## 2. Healthcare Access & Barriers

This page examines factors that may influence how quickly caregivers seek healthcare.

### Key areas

* Physical accessibility of healthcare
* Affordability of healthcare services
* Household healthcare decision-making
* Transportation methods
* Care-seeking time

### Key observation

The dashboard shows different patterns of timely and delayed care-seeking according to reported **accessibility, affordability, household decision-making, and transportation**.

---

## 3. Knowledge, Perception & Danger Signs

This page focuses on caregivers' knowledge and perceptions related to childhood fever.

### Key analyses

* Knowledge of childhood danger signs
* Danger signs × care-seeking time
* Perceived seriousness of fever
* Preferred timing of action
* Understanding/definition of fever

### Danger Signs Analysis

A key analysis compares **reported danger signs** between:

* **Within 24 Hours**
* **After 24 Hours**

This allows the dashboard to examine which danger signs are more commonly represented among caregivers who sought care within 24 hours compared with those who sought care after 24 hours.

### Key observation

Caregivers with poorer knowledge of illness danger signs showed a greater proportion of delayed care-seeking, while recognition of danger signs and perception of fever seriousness were associated with differences in care-seeking timeliness.

---

## 4. Care-Seeking Pathways & Outcomes

This page examines what caregivers did first, where they sought care, and what happened afterward.

### First Action

The reported first actions included:

* Health facility — **36.97%**
* Pharmacy/Drug shop — **32.70%**
* Home remedies — **26.78%**
* Traditional healer — **3.55%**

### Facility Visited

The most commonly reported facilities were:

* Private clinics — **85.06%**
* Public hospitals — **9.74%**
* Health centers — **2.60%**
* MCH centers — **2.60%**

### Referral

* Formal referral — **41.00%**
* No formal referral — **59.00%**

### Hospitalization

* Hospitalized — **19.19% (81 children)**
* Not hospitalized — **80.81% (341 children)**

### Clinical Outcomes

* Improved outcome — **63.03%**
* Overall positive/recovery outcome pattern — **99.35%**

---

# 🔎 Key Findings

## Overall Care-Seeking Pattern

Delayed care-seeking was more common than timely care-seeking in the analyzed dataset.

**63.5%** of respondents sought care **after 24 hours**, compared with **36.5%** who sought care **within 24 hours**.

This indicates that the 24-hour threshold is an important analytical point for understanding healthcare-seeking behavior in this dataset.

---

## Education & Timeliness

Care-seeking patterns differed across education levels.

Caregivers with **college-level education and above** demonstrated a higher proportion of timely care-seeking compared with lower education groups, where delayed care-seeking was more prominent.

---

## Healthcare Access

Differences were observed according to reported:

* Physical accessibility
* Affordability
* Transportation
* Household decision-making

Caregivers reporting better physical access and more affordable services showed a greater proportion of timely care-seeking.

---

## Knowledge & Danger Signs

Knowledge of childhood illness danger signs showed differences between timely and delayed care-seeking groups.

The dashboard also directly compares individual **danger signs** with **care-seeking time**, allowing identification of patterns between danger-sign reporting and whether care was sought within or after 24 hours.

---

## First Action & Care-Seeking

The first action taken when a child developed fever differed across care-seeking groups.

Health facilities and pharmacies/drug shops represented the most common initial actions, while home remedies and traditional healers were also reported.

Initial use of home remedies and traditional healers was more commonly associated with delayed care-seeking in the analyzed data.

---

## Care Pathways

Private clinics represented the largest proportion of facilities visited.

The care pathway also included pharmacies/drug shops, public hospitals, health centers, and MCH centers, demonstrating that caregivers entered and moved through the healthcare system through multiple points of care.

---

# 💡 Analytical Insights

The dashboard provides several important analytical perspectives:

### 1. Timeliness

The analysis identifies the proportion of caregivers seeking care within versus after the 24-hour threshold.

### 2. Knowledge

It examines whether caregiver knowledge and recognition of childhood danger signs differ across care-seeking groups.

### 3. Accessibility

It explores how reported healthcare accessibility, affordability, and transportation relate to care-seeking patterns.

### 4. Decision-Making

It examines household decision-making patterns and their distribution across timely and delayed care.

### 5. Care-Seeking Pathway

It follows the pathway from the **first action** to the **facility visited**, referral, hospitalization, and reported outcome.

---

# 📈 Power BI Features Used

The project demonstrates practical use of Power BI for healthcare data analysis, including:

* Data cleaning and transformation using **Power Query**
* Data modeling
* Relationships between tables
* DAX measures
* Calculated columns
* KPI cards
* Bar charts
* Donut/pie charts
* Slicers
* Filters
* Data labels
* Conditional formatting
* Interactive visual analysis
* Cross-filtering between visuals

---

# 🧮 Key DAX Measures

Examples of measures used in the dashboard include:

```DAX
Total Respondents =
COUNTROWS(Fact_CareSeeking)
```

```DAX
Delayed Care =
CALCULATE(
    [Total Respondents],
    Fact_CareSeeking[CareSeeking_Time] = "After 24 Hours"
)
```

```DAX
Timely Care =
CALCULATE(
    [Total Respondents],
    Fact_CareSeeking[CareSeeking_Time] = "Within 24 Hours"
)
```

```DAX
Delayed Care % =
DIVIDE(
    [Delayed Care],
    [Total Respondents],
    0
)
```

```DAX
Timely Care % =
DIVIDE(
    [Timely Care],
    [Total Respondents],
    0
)
```

These measures allow the dashboard to dynamically respond to slicers and filters.

---

# 🗂️ Project Structure

```text
Child-Fever-Care-Seeking-PowerBI/
│
├── README.md
│
├── Dashboard/
│   └── Child_Fever_Care_Seeking.pbix
│
├── Data/
│   └── [Dataset / Source Files]
│
├── Documentation/
│   └── Key_Findings.md
│
└── Screenshots/
    └── Dashboard_Pages/
```

---

# 🛠️ Tools & Technologies

| Tool                 | Purpose                                          |
| -------------------- | ------------------------------------------------ |
| **Power BI Desktop** | Dashboard development and visualization          |
| **Power Query**      | Data cleaning and transformation                 |
| **DAX**              | Measures and analytical calculations             |
| **Excel/CSV**        | Data source and preparation                      |
| **GitHub**           | Project documentation and portfolio presentation |

---

# 📌 Important Definitions

### Timely Care-Seeking

Care-seeking that occurred **within 24 hours**.

### Delayed Care-Seeking

Care-seeking that occurred **after 24 hours**.

### Care-Seeking Time

The time interval between recognition of the child's illness/fever and seeking healthcare.

### Danger Signs

Reported signs indicating potentially serious childhood illness and requiring attention in the context of the dataset.

---

# ⚠️ Interpretation Note

The findings presented in this dashboard are **descriptive and based on the analyzed dataset**.

Observed differences between timely and delayed care-seeking groups should not automatically be interpreted as causal relationships. The dashboard is intended to identify patterns and support further investigation.

Percentages may vary depending on the selected filters and slicers.

---

# 🎯 Project Value

This project demonstrates the application of **Power BI, data modeling, Power Query, and DAX** to a public-health dataset.

It shows how raw caregiver-level data can be transformed into an interactive analytical dashboard that communicates:

* Who seeks care promptly
* Where delays occur
* How caregivers respond to childhood fever
* How knowledge and perceptions differ
* What barriers may affect timeliness
* How caregivers navigate healthcare services
* What outcomes are reported

---

# 📚 Documentation

For detailed analytical findings, see:

**`Documentation/Key_Findings.md`**

The documentation provides a structured summary of the major findings identified across the dashboard pages.

---

# 👤 Project Focus

**Domain:** Public Health / Healthcare Analytics
**Topic:** Childhood Fever & Healthcare-Seeking Behavior
**Tool:** Microsoft Power BI
**Analysis Type:** Descriptive & Exploratory Data Analysis
**Dashboard Focus:** Timely vs. Delayed Care-Seeking

---

## ⭐ Summary

The **Child Fever & Care-Seeking Power BI Dashboard** provides an interactive analysis of healthcare-seeking behavior among caregivers of children with fever/acute febrile illness.

The central analytical focus is the comparison between **care-seeking within 24 hours and after 24 hours**, while examining caregiver knowledge, perceptions, healthcare access, barriers, first actions, healthcare pathways, and outcomes.

The project demonstrates how **data analytics and visualization can be used to identify patterns in healthcare-seeking behavior and communicate public-health findings effectively.**
