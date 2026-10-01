# Limitations & Future Work

## Limitations

### 1. Descriptive dashboard scope

The dashboard is primarily descriptive. It summarizes care-seeking behavior, access barriers, caregiver knowledge/perceptions, and related characteristics. It should not be interpreted as establishing causal relationships.

### 2. Percentage calculation validation

Some percentage visuals require additional DAX validation because values above 100% have appeared in parts of the dashboard. These measures should be verified before the dashboard is used for formal reporting or decision-making.

### 3. Filter-context dependence

Dashboard indicators can change according to slicers and filters. Users should interpret each percentage in the context of the population currently selected.

### 4. Data completeness

The completeness and accuracy of the dashboard depend on the quality of the underlying source data. Missing, inconsistent, or incorrectly coded values can affect calculated indicators.

### 5. Self-reported information

Where caregiver responses are self-reported, responses may be affected by recall or reporting differences.

### 6. Generalizability

Findings should be interpreted according to the population and setting represented by the underlying dataset. They should not automatically be generalized to all children, caregivers, facilities, or geographic areas.

### 7. Dashboard is not a clinical decision tool

The dashboard is intended for analytical and reporting purposes. It should not be used by itself to make individual clinical decisions.

## Future Work

### Data and model improvements

- Validate and document all DAX percentage measures.
- Add a formal data-quality summary.
- Document the final data model and relationships.
- Add automated checks for impossible percentage values.
- Create a reproducible data-preparation workflow where the source data can be shared safely.

### Analytical improvements

Future versions could include:

- Trend analysis if a suitable date/time variable is available.
- Comparison of timely versus delayed care-seeking across key demographic groups.
- Stratified analysis by facility and access characteristics.
- Additional KPI definitions with clearly documented denominators.
- More advanced DAX measures for comparative analysis.
- Statistical analysis outside Power BI where inferential questions are required.

### Dashboard improvements

- Add explanatory tooltips for major indicators.
- Add a dedicated methodology/definitions page.
- Add a data-quality status indicator.
- Standardize decimal places and percentage formatting.
- Improve accessibility through consistent contrast, labels, and readable font sizes.
- Add drill-through pages where they provide meaningful analytical value.

## Recommended Final QA

1. Verify the percentage measures.
2. Recheck the key KPI values.
3. Test all slicers and filters.
4. Confirm there are no ambiguous relationships.
5. Review all chart titles and labels.
6. Confirm screenshots represent the final PBIX version.
7. Remove or exclude any sensitive/raw individual-level data.

## Final Status

The project structure and documentation are designed for a professional portfolio presentation. The remaining analytical validation item is the final review of the percentage measures identified in the Data Quality documentation.
