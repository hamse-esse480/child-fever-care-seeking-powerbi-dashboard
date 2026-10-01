# Child Fever & Care-Seeking Power BI Dashboard

> An interactive Power BI dashboard exploring healthcare-seeking behavior, timeliness of care, healthcare access, caregiver knowledge, and care-seeking pathways among caregivers of children with fever / acute febrile illness (AFI).

## Project Overview

This project presents a **Power BI healthcare analytics dashboard** designed to understand what caregivers did when a child developed fever, how quickly care was sought, where care was obtained, and how access and caregiver knowledge relate to care-seeking timing.

The dashboard is organized around four analytical questions:

1. **What did caregivers actually do when the child had fever?**
2. **How do healthcare access factors differ by care-seeking timeliness?**
3. **How are knowledge and perceptions related to healthcare-seeking timeliness?**
4. **What are the overall patterns of timely and delayed care-seeking?**

A separate detail page allows users to inspect the selected subgroup at record level.

---

## Dashboard Pages

| Page | Purpose |
|---|---|
| **Executive Overview** | Summarizes first actions, facility type, referral, hospitalization, and child outcomes. |
| **Access & Barriers** | Explores accessibility, affordability, healthcare autonomy, and transport by care-seeking time. |
| **Knowledge & Perceptions** | Examines danger-sign knowledge, timing knowledge, fever seriousness, and fever-definition knowledge. |
| **Care-Seeking Pathways** | Shows overall timely vs delayed care-seeking and differences by education, facility type, and first action. |
| **Care-Seeking Details** | Provides a detailed filtered view of selected respondents and care-seeking characteristics. |

---

## Key Findings

Based on the dashboard visuals currently included in this repository:

- **422 respondents** are represented in the overall dashboard view.
- **36.5%** of respondents sought care **within 24 hours**, while **63.5%** sought care **after 24 hours**.
- **Private clinics** were the main type of facility visited, accounting for approximately **85.06%** of facility visits shown on the Executive Overview.
- The most common **first action** was going to a **health facility (36.97%)**, followed by a **pharmacy/drug shop (32.70%)** and **home remedy (26.78%)**. Traditional healer use was shown at **3.55%**.
- **59%** of cases shown on the Executive Overview had a referral given, compared with **41%** without a referral.
- The hospitalization visual shows **341 children (80.81%)** as hospitalized and **81 (19.19%)** as not hospitalized.
- The dashboard's overall pattern indicates that **delayed care-seeking was more common than care-seeking within 24 hours** in the displayed sample.
- The dashboard also displays differences in timely care-seeking across **education level, facility type, and first action**, which can be explored interactively using the slicers.

### Interpretation note

These are **descriptive dashboard findings**. They show patterns in the displayed dataset and should not be interpreted as causal relationships without appropriate statistical analysis.

---

## Important Visual QA Note

A professional review of the current dashboard screenshots identified a calculation/denominator issue on some visuals in the **Access & Barriers** and **Knowledge & Perceptions** pages.

Several displayed percentages are greater than 100% (for example values such as 442.5%, 8500%, and 3300%). Percentages representing proportions should normally remain within **0–100%**.

Before using the dashboard for a final report, publication, presentation, or portfolio, review the DAX measures behind these visuals—especially the denominator and filter context.

Recommended checks:

- Confirm that the percentage measure uses the intended denominator.
- Check whether counts are being divided by a filtered subgroup count or an overall count.
- Review `CALCULATE`, `DIVIDE`, `COUNTROWS`, `DISTINCTCOUNT`, and filter context.
- Test each measure against a simple manual calculation.
- Recheck the visuals after applying slicers.

The repository intentionally keeps the original PBIX unchanged so the dashboard can be audited and corrected separately.

---

## Interactivity

The dashboard includes interactive filters/slicers for variables such as:

- Child age group
- Gender
- Education level
- Facility type
- Household type

The pages are connected through Power BI interactions, allowing users to examine differences in care-seeking behavior across selected subgroups.

---

## Repository Structure

```text
health-care-seeking-dashboard/
│
├── README.md
│
├── powerbi/
│   └── FACT_CARE_SEEKING_PROJECT_ONE.pbix
│
├── screenshots/
│   ├── 01_executive_overview.png
│   ├── 02_access_and_barriers.png
│   ├── 03_knowledge_and_perceptions.png
│   ├── 04_care_seeking_pathways.png
│   └── 05_care_seeking_details.png
│
└── docs/
    └── KEY_FINDINGS.md
```

---

## How to Use

### Open the Power BI dashboard

1. Download or clone this repository.
2. Open:
   `powerbi/FACT_CARE_SEEKING_PROJECT_ONE.pbix`
3. Open the report in **Microsoft Power BI Desktop**.
4. Use the slicers and page navigation buttons to explore the dashboard.
5. Review the DAX measures before reusing the reported percentages in formal analysis.

### GitHub

The repository is structured so that:

- the **PBIX file** is separated from documentation;
- the **dashboard screenshots** are stored independently;
- the **key findings** are documented separately;
- the root README provides a concise project-level explanation.

---

## Analytical Scope

The dashboard focuses on:

**Outcome / main analytical variable**
- Care-seeking timeliness: within 24 hours vs after 24 hours.

**Care-seeking behavior**
- First action
- Type of facility visited
- Referral
- Hospitalization
- Child outcome

**Access and contextual factors**
- Healthcare accessibility
- Affordability
- Healthcare autonomy
- Transport mode

**Knowledge and perception factors**
- Danger-sign knowledge
- Timing knowledge
- Fever seriousness
- Fever-definition knowledge

**Stratification variables**
- Child age group
- Gender
- Education level
- Household type
- Facility type

---

## Limitations

- The dashboard is primarily **descriptive** and does not by itself establish statistical association or causality.
- Some visuals require DAX/denominator validation because of percentages exceeding 100%.
- The repository contains the Power BI report and screenshots; the underlying raw dataset is not included.
- Findings should therefore be interpreted within the population and sampling context of the original dataset.

---

## Recommended Next Steps

For a final professional version:

1. Validate and correct the percentage measures exceeding 100%.
2. Standardize visual titles and capitalization.
3. Add a short **Data & Methods** page documenting the dataset, sample, variables, and definition of timely care-seeking.
4. Add a **DAX Measures** documentation file if this project is being used as a Power BI portfolio project.
5. Re-export the screenshots after the calculation fixes.
6. If inferential analysis is required, complement the dashboard with appropriate statistical tests or regression analysis outside the dashboard.

---

## Project Type

**Tools:** Microsoft Power BI, Power Query, DAX  
**Domain:** Public Health / Healthcare Analytics  
**Analysis Type:** Descriptive and interactive dashboarding  
**Primary Theme:** Child fever / acute febrile illness care-seeking behavior
