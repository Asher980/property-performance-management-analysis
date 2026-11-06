# property-performance-management-analysis
A property management data analysis project using SQL to investigate tenant records, validate potential duplicates, and assess data quality through record-level comparisons.

# Property Performance Management Analysis

## Project Overview

This project explores data analysis in property management, with a focus on investigating potential duplicate tenant records using SQL.

As part of the analysis, I performed a duplicate-name check on the tenant table. Rather than assuming that repeated names represented duplicate records, I examined individual records and compared key fields to understand whether the entries were genuinely duplicates.

## Project Objectives

- Identify tenant names appearing more than once.
- Investigate records flagged by the initial duplicate check.
- Compare TenantID, ContactDetails, and LeaseStartDate.
- Distinguish repeated names from actual duplicate records.
- Apply data validation before drawing conclusions about data quality.

## Tools Used

- SQL
- Data validation
- Data quality analysis

## Analysis Process

### 1. Initial Duplicate Check

I grouped tenant records by name and identified names appearing multiple times.

The query returned **9 tenant names** that appeared more than once, including one name that appeared three times.

### 2. Record-Level Investigation

Instead of immediately classifying these records as duplicates, I queried the individual records and compared:

- TenantID
- ContactDetails
- LeaseStartDate

### 3. Validation

The investigation showed that records with identical tenant names had different TenantIDs, contact details, and lease start dates.

This suggested that the records represented different individuals who shared the same name, rather than duplicate tenant entries.

## Key Finding

The initial duplicate check identified repeated tenant names, but further investigation showed that these were not necessarily duplicate records.

**Key takeaway:** Similar names do not automatically mean duplicate records. Data findings must be investigated and validated before being classified as data quality issues.

## Skills Demonstrated

- SQL querying
- Duplicate record investigation
- Data validation
- Data quality assessment
- Critical thinking
- Analytical problem-solving

## Conclusion

This analysis reinforced the importance of looking beyond initial query results. A repeated value may indicate something worth investigating, but it is not a conclusion on its own.

As a data analyst, validating findings and understanding the context behind records are essential before reporting data quality issues.
