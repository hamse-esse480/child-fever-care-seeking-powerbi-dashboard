# Data Quality & Validation

## Purpose

This document records the quality checks applied to the Child Fever & Care-Seeking Power BI dashboard and highlights items that should be verified before final publication.

## Quality Checks

- Record/participant count consistency
- Duplicate records
- Missing or blank values
- Category consistency
- Numeric and percentage calculations
- Measure/filter behavior
- Relationship and model integrity
- Visual-level totals and denominators
- Consistency between KPI cards and detailed visuals

## Dashboard-Level Validation

The dashboard currently reports 422 respondents. This value should remain consistent across pages unless a visual is intentionally affected by a slicer or filter.

Key displayed indicators include:

| Indicator | Displayed value |
|---|---:|
| Total respondents | 422 |
| Care sought within 24 hours | 36.5% |
| Care sought after 24 hours | 63.5% |
| Private clinic as facility type | 85.06% |
| Referral given | 59% |
| Hospitalized | 80.81% |

These values should be rechecked against the underlying measures after any model or DAX changes.

## Percentage Validation

A proportion should follow:

`Category Percentage = Category Count / Relevant Denominator`

The denominator must represent the appropriate population for the visual. A percentage should not exceed 100% unless the metric is intentionally defined as an index or another non-proportion measure.

### Important validation flag

Some visuals in the current dashboard have displayed percentages above 100%. Examples previously observed include values such as 442.5%, 3,300%, and 8,500%.

These values should **not be treated as final findings** until the underlying DAX measure, denominator, filter context, and data type/format are verified.

Possible causes to check include:

1. A count measure being divided by the wrong denominator.
2. A percentage measure being divided by 100 again.
3. A visual using a denominator that changes unexpectedly under filter context.
4. Duplicate rows affecting counts.
5. A measure being formatted as a percentage when its underlying value is already multiplied by 100.
6. Incorrect relationship/filter propagation.

## DAX QA Checklist

- [ ] Check every percentage measure.
- [ ] Confirm numerator and denominator.
- [ ] Confirm the denominator responds correctly to intended slicers.
- [ ] Confirm percentages are stored/calculated as decimals before percentage formatting.
- [ ] Avoid multiplying by 100 if the measure is already formatted as Percentage.
- [ ] Check that counts are not unintentionally duplicated through relationships.
- [ ] Test measures with no filters and with each major slicer.
- [ ] Compare KPI cards with the corresponding chart totals.

## Model QA

Verify:

- Relationships are active where required.
- There are no ambiguous filter paths.
- Cardinality matches the data structure.
- Cross-filter direction is intentional.
- Dimension/category tables contain unique values where required.
- No unnecessary many-to-many relationships are used.

## Visual QA

Check:

- Titles clearly describe the metric.
- Category labels are readable.
- Percentages use consistent decimal places.
- No chart contains impossible proportions.
- Tooltips provide useful context.
- Slicers affect only the intended visuals/pages.

## Publication Status

**Status: Requires final DAX percentage verification before the dashboard is considered fully validated.**

The PBIX should remain unchanged until the questionable percentage measures have been reviewed and corrected if necessary.
