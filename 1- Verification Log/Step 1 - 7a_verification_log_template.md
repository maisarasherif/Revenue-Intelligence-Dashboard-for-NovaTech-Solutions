# NovaTech Data Verification Log

**Student Name:**  Maysara Sherif
**Date:** 12/09/2026

## Instructions

Query each pre-indexed knowledge base using Quick Chat. For each question, record the expected answer (from the data dictionary), Q's actual response, and whether they match. Minimum 6 entries (2 per data knowledge base).

## Verification Log

| #   | Knowledge Base               | Question Asked                                                                                                 | Expected Answer                                                                                | Q's Actual Answer                                                                                                                                                                                                                  | Match? | Notes |
| --- | ---------------------------- | -------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ----- |
| 1   | NovaTech CRM Deals           | how many **rows** in this dataset?                                                                             | 499                                                                                            | The **novatech_crm_deals.csv** dataset contains **499 rows**.                                                                                                                                                                      | yes    |       |
| 2   | NovaTech CRM Deals           | what company have the largest employee count in this dataset?                                                  | 34288                                                                                          | The company with the largest employee count is **YieldMax Software** with **34,288 employees**.                                                                                                                                    | yes    |       |
| 3   | NovaTech Marketing Campaigns | how many **rows** in this dataset?                                                                             | 2240                                                                                           | The **novatech_marketing_campaigns.csv** dataset contains **2,240 rows**.                                                                                                                                                          | yes    |       |
| 4   | NovaTech Marketing Campaigns | what is the **annual income for LEAD-00022** in this dataset?                                                  | 46310                                                                                          | The annual income for **LEAD-00022** is **46,310**.                                                                                                                                                                                | yes    |       |
| 5   | NovaTech Support Tickets     | how many **rows** in this dataset?                                                                             | 3000                                                                                           | The **novatech_support_tickets.csv** dataset contains **3,000 rows**.                                                                                                                                                              | yes    |       |
| 6   | NovaTech Support Tickets     | how many users affected across al supporting tickets that ACCT-007 has handled in the support tickets dataset? | 460                                                                                            | The total users affected across all support tickets for **ACCT-007** is **460 users** (across 8 distinct tickets).                                                                                                                 | yes    |       |
| 7   | NovaTech Reference Documents | what type of dashboard and how many views does sarah chen want to achieve?                                     | A single dashboard with three views. One place the whole revenue team can go instead of three. | **Dashboard Type:** A **Revenue Intelligence Dashboard** — a single, unified dashboard that connects data from three siloed systems (CRM, Marketing platform, and Support ticketing system).<br><br>**Number of Views: Three (3)** | yes    |       |

## Cross-Check

Pick one fact from above and confirm it independently in the QuickSight dataset preview.

- **Fact verified:** Question 2, in the CRM Deals dataset, the company with largest employee count is **YieldMax Software** with 34288
- **Chat said:** **YieldMax Software** has the largest employee count in the CRM deals data with **34,288 employees**
- **QuickSight shows:** **34,288** screenshot attached
- **Consistent?** yes


![[largest employee count in a company.png]]