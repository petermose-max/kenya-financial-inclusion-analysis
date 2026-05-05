# Data Dictionary
## Key Variables in `finaccess_master`

The `finaccess_master` view contains one record per respondent and brings together the core variables used for SQL analysis of financial inclusion, geography, demographics, product usage, financial health, and vulnerability.

| Column | Description | Coding and Interpretation |
|---|---|---|
| `interview__key` | Unique respondent interview identifier | Used to join survey tables and preserve respondent-level records. |
| `county` | Kenya county code | Numeric county code from 1 to 47. |
| `Sex` | Respondent gender | 1 = Male, 2 = Female. |
| `Age` | Respondent age group | 1 = Under 16, 2 = 16-25, 3 = 26-35, 4 = 36-45, 5 = 46-55, 6 = 56+. |
| `Education` | Highest education category | 1 = None, 2 = Primary, 3 = Secondary, 4 = Tertiary. |
| `Marital` | Marital status category | Used as a demographic segmentation variable where relevant. |
| `Latitude`, `Longitude` | Geographic coordinates | Used to explore spatial patterns in financial exclusion and vulnerability. |
| `Quintiles` | Household welfare or income quintile | 1 = Lowest income quintile, 5 = Highest income quintile. |
| `indWeight` | Individual survey weight | Used for weighted estimates where survey-weighted analysis is required. |
| `Access_Strand` | Financial access strand classification | 1 = Formally included, 2 = Informally served, 3 = Financially excluded, 4 = Other. |
| `mobile_money_use` | Mobile money usage indicator | Binary indicator where 1 = Yes and 0 = No. |
| `bank_use` | Bank usage indicator | Binary indicator where 1 = Yes and 0 = No. |
| `mobile_money_access` | Mobile money access indicator | Binary indicator where 1 = Yes and 0 = No. |
| `Savings_usage` | Savings product or practice indicator | Binary indicator where 1 = Yes and 0 = No. |
| `Loan_usage` | Credit or loan usage indicator | Binary indicator where 1 = Yes and 0 = No. |
| `All_Insurance_including_NHIF` | Insurance usage indicator including NHIF | Binary indicator where 1 = Yes and 0 = No. |
| `Informal_usage` | Informal financial service usage indicator | Binary indicator where 1 = Yes and 0 = No. |
| `mobile` | Mobile phone ownership or use indicator | Binary indicator where 1 = Yes and 0 = No. |
| `digital_acc` | Digital financial access indicator | Binary indicator where 1 = Yes and 0 = No. |
| `Overall_Access_fnl` | Overall financial access indicator | Binary indicator where 1 = Yes and 0 = No. |
| `Financial_literacy_index_fnl` | Financial literacy index | Numeric score used to compare financial knowledge across respondents and counties. |
| `finhealth_fnl` | Financial health score | Numeric score used to assess household financial resilience and wellbeing. |
| `vul_index_fnl` | Vulnerability index | Numeric score used to assess relative financial vulnerability. Higher values indicate greater vulnerability. |

## SQL Quoting Rule

PostgreSQL folds unquoted identifiers to lowercase. For this project, all column names containing uppercase letters must be wrapped in double quotes in SQL queries.

Columns requiring double quotes:

- `"Sex"`
- `"Age"`
- `"Education"`
- `"Marital"`
- `"Latitude"`
- `"Longitude"`
- `"Quintiles"`
- `"indWeight"`
- `"Access_Strand"`
- `"Savings_usage"`
- `"Loan_usage"`
- `"All_Insurance_including_NHIF"`
- `"Informal_usage"`
- `"Overall_Access_fnl"`
- `"Financial_literacy_index_fnl"`

Columns that do not require quotes:

- `interview__key`
- `county`
- `mobile_money_use`
- `bank_use`
- `mobile_money_access`
- `mobile`
- `digital_acc`
- `finhealth_fnl`
- `vul_index_fnl`
