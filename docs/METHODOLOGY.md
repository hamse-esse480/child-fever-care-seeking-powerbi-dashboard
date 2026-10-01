# Methodology

## 1. Project Objective

This dashboard provides an interactive descriptive analysis of healthcare-seeking behavior among caregivers of children experiencing fever / acute febrile illness (AFI).

The analysis covers timeliness of care-seeking, first actions, facility utilization, healthcare access, caregiver knowledge and perceptions, referral, hospitalization, and subgroup patterns.

## 2. Analytical Framework

### Care-Seeking Behavior
- First action
- Facility type
- Referral
- Hospitalization
- Child outcome

### Timeliness
Care-seeking is categorized as **within 24 hours** or **after 24 hours**.

### Healthcare Access
- Accessibility
- Affordability
- Healthcare autonomy
- Transport mode

### Knowledge & Perceptions
- Danger-sign knowledge
- Timing knowledge
- Fever seriousness
- Fever-definition knowledge

## 3. Data Workflow

```text
Source Data
    ↓
Power Query
    ↓
Data Cleaning & Transformation
    ↓
Data Model
    ↓
DAX Measures
    ↓
Interactive Visualizations
    ↓
Dashboard
```

Typical preparation includes data-type review, categorical standardization, missing-value and duplicate checks, creation of analytical categories, and validation of counts and percentages.

## 4. Dashboard Pages

1. **Executive Overview** — first action, facility type, referral, hospitalization, and child outcome.
2. **Access & Barriers** — accessibility, affordability, autonomy, and transport by care-seeking time.
3. **Knowledge & Perceptions** — caregiver knowledge/perceptions by care-seeking time.
4. **Care-Seeking Pathways** — overall timeliness and differences by education, facility type, and first action.
5. **Care-Seeking Details** — detailed filtered view of represented records.

## 5. Technologies

- Microsoft Power BI Desktop
- Power Query
- DAX
- Slicers and filters
- Cards, charts, and detail tables

## 6. Analysis Type

The dashboard is primarily descriptive. It does not by itself establish causality or statistical significance. Formal inferential analysis requires appropriate study design, sampling information, and statistical methods.

## 7. Percentage Principle

For a proportion:

```text
Percentage = Category Count / Relevant Denominator × 100
```

In Power BI, `DIVIDE()` is preferred for safe percentage calculations. The denominator must match the intended population and filter context.

## 8. Quality Assurance

Before final publication:

- Verify total respondent count.
- Verify category counts against source data.
- Confirm percentages are logically bounded when they represent proportions.
- Test slicers and cross-filtering.
- Validate DAX measures manually.
- Check missing/unexpected categories.
- Review page titles and labels for consistency.

## 9. Current Validation Note

The current screenshots contain some percentage values above 100% on the Access & Barriers and Knowledge & Perceptions pages. These should be treated as a **DAX/denominator validation issue**, not as substantive findings. Check numerator, denominator, filter context, duplicate counting, and percentage formatting before final publication.
