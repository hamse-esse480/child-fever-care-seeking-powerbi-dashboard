# DAX Measures

## Project
**Child Fever & Care-Seeking Power BI Dashboard**

This document contains the main DAX measures used to calculate respondent totals and care-seeking indicators.

## 1. Total Respondents

```DAX
Total Respondents =
COUNTROWS(Fact_CareSeeking)
```

Counts the total number of respondents in the fact table.

## 2. Delayed Care

```DAX
Delayed Care =
CALCULATE(
    [Total Respondents],
    Fact_CareSeeking[CareSeeking_Time] = "After 24 Hours"
)
```

Counts respondents who sought care after 24 hours.

## 3. Timely Care

```DAX
Timely Care =
CALCULATE(
    [Total Respondents],
    Fact_CareSeeking[CareSeeking_Time] = "Within 24 Hours"
)
```

Counts respondents who sought care within 24 hours.

## 4. Delayed Care %

```DAX
Delayed Care % =
DIVIDE(
    [Delayed Care],
    [Total Respondents],
    0
)
```

Calculates the percentage of respondents who delayed care-seeking.

## 5. Timely Care %

```DAX
Timely Care % =
DIVIDE(
    [Timely Care],
    [Total Respondents],
    0
)
```

Calculates the percentage of respondents who sought care within 24 hours.

## 6. Selected Education

```DAX
Selected Education =
SELECTEDVALUE(
    Fact_CareSeeking[Educational level],
    "All Education"
)
```

Returns the currently selected education category when a single category is selected. If multiple categories or no specific category are selected, it returns **"All Education"**.

## DAX Approach

The project primarily uses:

- `COUNTROWS()` for respondent counts
- `CALCULATE()` for filtered calculations
- `DIVIDE()` for percentages
- `SELECTEDVALUE()` for dynamic category selection

These measures support interactive analysis through slicers, filters, and visual cross-filtering.
