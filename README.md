# Supply Chain Shipment Data Validation

This project was completed during my internship at Cognizant from January to April 2026, in the Artificial Intelligence and Analytics (AIA) domain, as part of the ETL Testing work.

## About the Project

The project focuses on transforming and validating shipment data transferred from a source table to a target table. It uses MySQL to handle data transformation and validation, while Microsoft Excel is used to document the source data, target data, field mappings, test scenarios, and test results.

## Problem Statement

When shipment data is transferred between systems, the target data must retain the required information and follow the defined business rules.

Issues such as missing values, duplicate records, incorrect field mappings, calculation errors, and inconsistent dates can affect data accuracy. The challenge was to identify these issues and verify that the transformed shipment records met the expected requirements.

## Solution

I used MySQL to create the source and target tables, transform shipment records, apply business rules, calculate freight charges, and perform data validation.

Microsoft Excel was used to organise the shipment data, document field mappings, define test scenarios, and record test cases and their results.

## Data Transformation and Validation

The SQL script covers:

- Source and target table creation.
- Shipment data transformation and surrogate key generation.
- Transit day calculation.
- Service-level rate multiplier mapping.
- Linehaul cost and freight charge calculations.
- Fuel surcharge and COD fee calculations.
- Delivery target and date-sequence checks.
- Duplicate, missing value, and calculation checks.

## Test Results

The project contains 25 source records, 25 target records, 20 test scenarios, 20 field-mapping entries, and 34 test-case entries across two testing cycles.

| Test Cycle | Test Cases | Recorded Status |
|---|---:|---|
| Cycle 1 - Positive Testing | 24 | Pass |
| Cycle 1 - Negative Testing | 5 | Fail |
| Cycle 2 - Retesting | 5 | Pass |

The recorded validation results include:

| Validation | Result |
|---|---:|
| Duplicate records | 0 |
| Missing values | 0 |
| Unmatched records | 0 |
| Calculation mismatches | 0 |
| Date-sequence exceptions | 4 |

The four date-sequence exceptions were identified and recorded as validation findings.

**Testing Note:** The supplied SQL script references additional tables in its negative testing section that are not created within the script. The Excel workbook contains the test cases and recorded results for both testing cycles.

## Tech Stack

- MySQL
- Microsoft Excel

## Project Structure

```text
Supply Chain Shipment Data Validation/
│
├── .gitignore
├── LICENSE
├── README.md
├── Shipment Data Transformation and Validation.sql
└── Shipment Data Analysis and Test Results.xlsx
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
