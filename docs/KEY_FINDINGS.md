# Key Findings

## 1. Overall Care-Seeking Timeliness

The dashboard represents **422 respondents** in the overall view.

- **Within 24 hours:** 36.5% (154 respondents)
- **After 24 hours:** 63.5% (268 respondents)

This indicates that delayed care-seeking is more common than care-seeking within 24 hours in the displayed sample.

> This is a descriptive observation and should not be interpreted as a causal or population-level conclusion without considering the study design and sampling method.

---

## 2. Healthcare Facilities and First Actions

The Executive Overview shows:

### Type of facility visited

- Private clinic: **85.06%**
- Public hospital: **9.74%**
- Health center: **2.60%**
- Medical center: **2.60%**

### First action

- Health facility: **36.97%**
- Pharmacy/drug shop: **32.70%**
- Home remedy: **26.78%**
- Traditional healer: **3.55%**

The displayed dashboard therefore shows a strong use of formal healthcare facilities, particularly private clinics, while pharmacy/drug-shop use and home remedies are also important first responses.

---

## 3. Referral and Hospitalization

The Executive Overview shows:

- Referral given: **59%**
- No referral: **41%**

For hospitalization:

- Yes: **341 (80.81%)**
- No: **81 (19.19%)**

These figures describe the cases represented in the dashboard and should be interpreted in the context of how the underlying data were collected.

---

## 4. Education and Timely Care-Seeking

The Care-Seeking Pathways page shows differences in the displayed proportion of timely care-seeking across education categories.

The visual includes:

- No formal education
- Primary
- Secondary
- College and above

The dashboard should be interpreted as showing **descriptive differences between groups**, rather than evidence that education causes timely or delayed care-seeking.

---

## 5. Facility Type and Timely Care-Seeking

The Care-Seeking Pathways page displays timely and delayed care-seeking by facility type.

The visual suggests that the proportion of timely care-seeking differs across:

- Public hospitals
- Medical centers
- Health centers
- Private clinics

This pattern can be explored interactively using the dashboard filters.

---

## 6. First Action and Timely Care-Seeking

The dashboard also compares care-seeking timeliness across first actions, including:

- Traditional healer
- Home remedy
- Pharmacy/drug shop
- Health facility

This provides a useful pathway-oriented view of how the first response to childhood fever corresponds with the timing of care-seeking.

---

## 7. Knowledge and Perceptions

The Knowledge & Perceptions page examines:

- Danger-sign knowledge
- Timing knowledge
- Fever seriousness
- Fever-definition knowledge

The dashboard's intended analytical question is whether these knowledge/perception categories differ between respondents who sought care within 24 hours and those who sought care after 24 hours.

### Important validation point

Some percentages on this page exceed 100% (for example, values such as 8500% and 3300%). These values should **not** be interpreted as real percentages.

The underlying DAX measures should be checked for:

- incorrect denominator;
- incorrect filter context;
- count-vs-percentage logic;
- duplicate counting;
- subgroup denominator selection.

---

## 8. Access and Barriers

The Access & Barriers page examines:

- Healthcare accessibility
- Affordability
- Healthcare autonomy
- Transport mode

The dashboard is designed to compare these factors by care-seeking time.

However, several displayed values exceed 100%, so the associated percentage calculations require validation before these visuals are used as evidence in a report.

---

## 9. Professional Interpretation

The dashboard provides a useful descriptive picture of child fever care-seeking behavior:

> **Delayed care-seeking is more common than care-seeking within 24 hours in the displayed sample, while private clinics are the most frequently reported facility type and formal healthcare is a common first response.**

The dashboard also provides subgroup comparisons by education, facility type, first action, and caregiver knowledge/perceptions.

These patterns should be followed by formal statistical analysis if the research objective is to determine whether the observed differences represent statistically significant associations.

---

## 10. Data Visualization Quality Check

Before final publication:

- Correct all percentages above 100%.
- Verify every denominator.
- Confirm that measures return proportions rather than raw ratios.
- Test measures with and without slicers.
- Check that totals remain logically consistent.
- Re-export all screenshots after corrections.
