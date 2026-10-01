# DAX Measures Documentation

> The exact measure names/formulas in the PBIX are authoritative. The patterns below are documentation and validation templates.

## Total Respondents

```DAX
Total Respondents =
COUNTROWS('YourTable')
```

If the analytical unit is a unique respondent:

```DAX
Total Respondents =
DISTINCTCOUNT('YourTable'[Respondent_ID])
```

## Timely Care-Seeking Count

```DAX
Timely Care-Seeking Count =
CALCULATE(
    COUNTROWS('YourTable'),
    'YourTable'[Care_Seeking_Time] = "Within 24 hours"
)
```

## Delayed Care-Seeking Count

```DAX
Delayed Care-Seeking Count =
CALCULATE(
    COUNTROWS('YourTable'),
    'YourTable'[Care_Seeking_Time] = "After 24 hours"
)
```

## Timely Care-Seeking Percentage

```DAX
Timely Care-Seeking % =
DIVIDE(
    [Timely Care-Seeking Count],
    [Total Respondents],
    0
)
```

Format the measure as **Percentage**.

## Delayed Care-Seeking Percentage

```DAX
Delayed Care-Seeking % =
DIVIDE(
    [Delayed Care-Seeking Count],
    [Total Respondents],
    0
)
```

## Generic Category Percentage

```DAX
Category % =
DIVIDE(
    [Category Count],
    [Relevant Total],
    0
)
```

## Referral Percentage

```DAX
Referral % =
DIVIDE(
    CALCULATE(
        COUNTROWS('YourTable'),
        'YourTable'[Referral] = "Yes"
    ),
    [Total Respondents],
    0
)
```

## Hospitalization Percentage

```DAX
Hospitalization % =
DIVIDE(
    CALCULATE(
        COUNTROWS('YourTable'),
        'YourTable'[Hospitalization] = "Yes"
    ),
    [Total Respondents],
    0
)
```

## Important Validation: Percentages Above 100%

Values such as **442.5%, 8500%, or 3300%** indicate that the relevant percentage calculation needs review.

Common causes:

1. Wrong denominator.
2. Unexpected `CALCULATE()` filter context.
3. Double percentage conversion.
4. Duplicate counting.
5. Incorrect analytical unit.

Avoid this pattern when the measure is formatted as Percentage:

```DAX
Percentage = DIVIDE([Count], [Total], 0) * 100
```

Prefer:

```DAX
Percentage = DIVIDE([Count], [Total], 0)
```

and format it as Percentage in Power BI.

## Manual Validation Example

For 154 timely cases out of 422 respondents:

```text
154 / 422 = 0.365
0.365 × 100 = 36.5%
```

The Power BI percentage measure should therefore return approximately `0.365` internally when formatted as Percentage.

## Best Practices

- Prefer `DIVIDE()` for percentage measures.
- Use `DISTINCTCOUNT()` when the unit is a unique respondent.
- Keep percentage measures as decimal ratios and format them as Percentage.
- Test measures under different slicer selections.
- Validate totals against source data.
- Use descriptive measure names.
