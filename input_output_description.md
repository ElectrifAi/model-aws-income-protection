# Input/Output Description

## Input:
A **zip file** with the following comma separated csv files. Reference file: sample.zip


| Raw Table         | Table Required? | Column                    | Column Required? | Meaning                                                               |
|-------------------|-----------------|---------------------------|------------------|-----------------------------------------------------------------------|
| customer_info.csv | Y               | CUSTOMER_ID               | Y                | customer id                                                           |
|                   |                 | DOB                       | Y                | date of birth of customer                                             |
|                   |                 | MARITAL STATUS            | Y                | martial status                                                        |
|                   |                 | AUSTRALIAN_CITIZEN        | Y                | australian citizen y/n                                                |
|                   |                 | EMPLOYEMENT_TYPE          | Y                | type of employement part time, full time , free lancing,self employed |
|                   |                 | NATURE_OF_BUSINESS        | Y                | nature_of_employement                                                 |
|                   |                 | EMPLOYED_SINCE            | Y                | date of employement                                                   |
|                   |                 | EMPLOYER_NAME             | Y                | name of employer                                                      |
|                   |                 | GROSS_INCOME_MNTHLY       | Y                | monthly income                                                        |
|                   |                 | LAST_DRAWN_SAL            | Y                | last month salary in hand                                             |
|                   |                 | LAST_MNTH_OF_SAL          | Y                | last month for which salry was paid                                   |
| paln_details.csv  | y               | PLAN_ID                   | Y                | id of plan                                                            |
|                   |                 | MIN_AGE                   | Y                | min age for the plan                                                  |
|                   |                 | MAX_AGE                   | Y                | max age for plan                                                      |
|                   |                 | NO_OF_DEPENDENTS          | Y                | max dependents allowed per claim                                      |
|                   |                 | DISEASES_COVERED          | Y                | list of diseases covered under this plan                              |
|                   |                 | MIN_BENEFIT_AMT           | Y                | mininmum benefit for this plan                                        |
|                   |                 | MAX_BENEFIT_AMT           | Y                | maximum benefit allowed for this claim                                |
|                   |                 | DOCS_REUQIRED             | Y                | list of documents required in this claim                              |
| sales_info.csv    | y               | POLICY_ID                 | Y                | policy id                                                             |
|                   |                 | CUSTOMER_ID               | Y                | customer id                                                           |
|                   |                 | RETURN_WORK_INCLUDED      | Y                | is return to work included in policy                                  |
|                   |                 | POLICY_OWNER              | Y                | name of policy owner                                                  |
|                   |                 | FUND_DETAILS              | Y                | fund details for policy                                               |
|                   |                 | TRUSTEE_DETAILS           | Y                | trustee details for policy                                            |
|                   |                 | NO_OF_DEPENDENTS          | Y                | total number of dependents on this policy                             |
|                   |                 | NOMINEE_DOB               | Y                | age of nominee                                                        |
|                   |                 | NOMMINE_RELATIONSHIP      | Y                | relation ship with policy owner                                       |
|                   |                 | PREMIUM_AMOUNT            | Y                | premium amount for policy                                             |
| claim_info.csv    | y               | CLAIM_ID                  | Y                | claim id                                                              |
|                   |                 | DATE_OF_CLAIM_OPENED      | Y                | claim opened date                                                     |
|                   |                 | POLICY_ID                 | Y                | policy id                                                             |
|                   |                 | DOCS_SUBMITTED            | Y                | documents submitted for the claim                                     |
|                   |                 | CLAIM_AMOUNT              | Y                | claim amount reuested                                                 |
|                   |                 | CLAIM_INSPECTION_STATUS   | Y                | status of inspection                                                  |
|                   |                 | CLAIM_VERIFICATION_STATUS | Y                | claim verifictaion status                                             |
|                   |                 | CLAIM_INSPECTOR_ID        | Y                | id of inspector of claim                                              |
|                   |                 | CLAIM_HISTORY             | Y                | has claim hostory prior to this claim                                 |
|                   |                 | PREVIOUS_CLAIM_AMOUNT     | Y                | cummulative sum of previous claims                                    |
|                   |                 | TYPE_OF_INJURY            | Y                | type of injury illness /accident                                      |
|                   |                 | DATE_OF_INCIDENT          | Y                | date of incident                                                      |
|                   |                 | CAUSE_OF_INCIDENT         | Y                | cause of incident                                                     |
|                   |                 | REPETETIVE_INCIDENT       | Y                | is this is a repetetive incident                                      |
|                   |                 | LAST_DAY_OF_WORK          | Y                | last day of work before incident                                      |
|                   |                 | INJURY_CODE               | Y                | injury code                                                           |
|                   |                 | ORG_BENEFIT_PAID          | Y                | benfits paid by the organisations                                     |
|                   |                 | AMOUNT_RECEIVED_FRM_ORG   | Y                | amount received from organisation                                     |
|                   |                 | BENEFIT_FRM_OTHR_ORG      | Y                | benfits paid by other  organisations                                  |
|                   |                 | AMOUNT_RECEIVED           | Y                | amount received other organisation                                    |


## Output:
A list of JSON objects containing the fields listed below. Reference file: sample.zip.out

| Raw Table  | Table Required? | Column               | Column Required? | Meaning                                       |
|------------|-----------------|----------------------|------------------|-----------------------------------------------|
| output.csv | y               | claim_id             | Y                | claim id                                      |
|            |                 | claim_complexity     | Y                | complexity of the claim                       |
|            |                 | claim_duration       | Y                | duration for which the claim will remain open |
|            |                 | amount_paid_monthly  | Y                | amount paid by the company                    |
