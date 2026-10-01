# Data Dictionary

## Overview
This document describes the main variables represented in the Child Fever & Care-Seeking Power BI dashboard. The dashboard focuses on child/caregiver characteristics, healthcare access, knowledge and perceptions, care-seeking behavior, and timeliness.

> The original dataset/codebook remains the authoritative source for exact technical variable names, coding, and missing-value definitions.

## Core Variables

| Variable | Description | Type / Role |
|---|---|---|
| `Age` | Age of the child represented in the record | Numeric |
| `Gender` | Sex/gender of the child | Categorical |
| `Education_Level` | Education level of the caregiver/respondent | Categorical |
| `Household_Type` | Household classification | Categorical |
| `First_Action` | First action taken when the child developed fever | Categorical |
| `Care_Seeking_Time` | Timing of care-seeking relative to fever onset | Categorical / Main outcome |
| `Facility_Type` | Type of healthcare facility visited | Categorical |
| `Referral` | Whether a referral was given | Binary/Categorical |
| `Hospitalization` | Whether the child was hospitalized | Binary/Categorical |
| `Child_Outcome` | Recorded outcome/status of the child | Categorical |

## Care-Seeking Timeliness

The dashboard uses two main categories:

- **Within 24 hours**
- **After 24 hours**

This is the primary descriptive outcome used to compare access, knowledge, perceptions, education, facility type, and first action.

## Healthcare Access Domains

- Healthcare accessibility
- Affordability
- Healthcare autonomy
- Transport mode

## Knowledge & Perception Domains

- Danger-sign knowledge
- Timing knowledge
- Perceived seriousness of fever
- Fever-definition knowledge

## Care-Seeking Behavior

### First Action
- Health facility
- Pharmacy/drug shop
- Home remedy
- Traditional healer

### Facility Type
- Private clinic
- Public hospital
- Health center
- Medical center

## Stratification Variables

The dashboard can be explored by child age group, gender, education level, household type, facility type, and first action.

## Data Quality Checks

Before final publication, verify exact variable names, category labels, missing-value codes, numeric ranges, duplicates, the 24-hour definition, and the denominator used by each percentage measure.
