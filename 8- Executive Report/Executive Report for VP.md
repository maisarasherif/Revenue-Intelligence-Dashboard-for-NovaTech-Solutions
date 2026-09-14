# Executive Summary
The NovaTech Revenue Intelligence dashboard brings marketing, sales and support information into one place. It replaces the weekly manual process of copying figures from three systems, and gives the revenue team a shared view of campaign results, deal performance and account risk.

The dashboard found three issues that need attention. Marketing spend is much higher than attributed revenue across every campaign. Sales results are strongest in the Central region but weaker in East and West. Several valuable accounts also carry a heavy support load, especially YieldMax Software. Quick Chat can now answer follow-up questions across the datasets, though important answers should still be checked against the dashboard.

# Data strategy
The CRM, marketing and support files were prepared separately before they were connected. Dates and numeric fields were corrected, fields with no useful reporting purpose were left out of the analysis, and calculated fields were added for measures such as days to close, campaign ROI, response rate, resolution hours, ticket frequency and closed-won conversion.

The three sources share account_id. The CRM account list was used as the main account reference, then marketing and support information was linked to the same accounts. One account can have several leads, deals and support tickets, so a direct join can repeat records. Distinct lead, opportunity and ticket counts were used where needed. Account-level totals and averages were also used in the unified health table so repeated rows did not inflate the results.

The source datasets were kept for detailed marketing, sales and support visuals, while the unified dataset was used for account-level questions. Weekly freshness is enough, so there is no need for a real-time connection.

# Dashboard design

| **Sheet**        | **Purpose**                                     | **Main content**                                                                                   |
| ---------------- | ----------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Marketing Funnel | Show how campaign activity turns into pipeline. | Lead funnel, campaign conversion, response rate, spend, attributed revenue and ROI.                |
| Sales Pipeline   | Show deal outcomes and revenue performance.     | Win rate, won revenue, days to close, deal value, regional results and loss reasons.               |
| Customer Health  | Identify accounts that may be at risk.          | Ticket volume, resolution time, priority, sentiment, product issues and the unified account table. |
Each sheet includes business filters. Chart selections filter related visuals, and Customer Health includes navigation to the Sales Pipeline.

# Key findings and recommended actions

The findings below use the full date range with dashboard filters set to All.

| **Finding**                                                                                                                                                       | **Why it matters**                                                                                                                                | **Recommended action**                                                                                                                                                         |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| All six campaigns spent more than their attributed revenue. NovaPulse Launch had the best ROI at -83.73%, while NovaEdge Awareness was lowest at -97.74%.         | The current campaign revenue does not cover the recorded marketing cost. This may reflect weak campaign returns, incomplete attribution, or both. | Check the attribution rules and campaign costs first. If the figures are confirmed, reduce or redesign NovaEdge Awareness and set a clear return target for each campaign.     |
| Digital Retarget generated the most leads at 419, but its closed-won conversion was 16.23%. NovaPulse Launch generated 409 leads and converted 33.74%.            | Lead volume alone does not show lead quality. NovaPulse produced almost the same volume and more than twice the conversion rate.                  | Test moving part of the Digital Retarget budget to NovaPulse, while keeping a controlled comparison of lead quality and cost.                                                  |
| Enterprise accounts produced $319,423 in won revenue across 127 deals. Their average won deal size was $2,515, the highest of the four company sizes.             | Enterprise accounts provide the largest revenue contribution and the highest average deal value.                                                  | Give Enterprise opportunities clear account plans and senior sales coverage. Track service problems closely because several Enterprise accounts also have high ticket volumes. |
| The overall win rate was 63.51%. Central led at 70.24%, compared with West at 58.79% and East at 57.81%.                                                          | The gap between Central and the other regions points to missed sales opportunities and inconsistent sales practice.                               | Review how Central qualifies and closes deals. Use the useful parts of that approach in East and West, then compare win rates each month.                                      |
| No Decision Made and Poor Product Fit each caused 43 lost deals. Together they represent 86 of 184 losses, or 46.7%.                                              | Almost half of all losses relate to customer commitment or fit. Both can often be identified earlier in the sales process.                        | Strengthen early discovery and product-fit checks. Sales managers should review deals showing either risk before they reach the final stage.                                   |
| YieldMax Software had 334 support tickets, 13 recent tickets and $40,722 in total deal value. It also appeared among Enterprise accounts with negative sentiment. | This is the clearest combination of revenue value and service pressure. If the issues continue, the account may be difficult to retain.           | Arrange a joint Sales and Support review for YieldMax. Agree the main service issues, owner and follow-up date, then monitor recent ticket volume.                             |

# Topic configuration and Quick Chat results

A NovaTech Revenue Intelligence Topic was published for Quick Chat. It connects marketing, CRM and support data through account_id and gives Quick Chat rules for business measures. The main rules are to count distinct opportunity IDs for deal metrics, use won deal value for revenue, and calculate cross-account resolution time as an unweighted average of the account averages.

At first Quick Chat calculated the sales win rate from 499 CRM rows. It returned 63.13% overall and 69.90% for Central, while the dashboard used 496 distinct opportunities. After the Topic was updated the same question returned 63.51% overall and 70.24% for Central, matching the dashboard.

|**Test**|**Before Topic refinement**|**After Topic refinement**|
|---|---|---|
|Campaign leads and conversion|Correct: Digital Retarget, 419 leads and 16.2% conversion.|Correct: 419 leads and 16.23%. The change was mainly better precision.|
|Overall and regional win rate|Incorrect denominator: 63.13% overall and 69.90% for Central.|Correct distinct-deal result: 63.51% overall and 70.24% for Central.|
|Highest support-volume account|Correct main answer, but the supporting list was limited.|Correct: YieldMax, 334 tickets and $40,722. Account-level questions also returned more detail.|

The Topic also answered questions that were not shown in one dashboard visual. It identified 27 Enterprise accounts with negative sentiment. It also found that Q3 Growth Sprint was associated with $279,337 in won value across 28 qualifying accounts, with an unweighted high or critical ticket resolution average of 57.22 hours. Another test showed that Small accounts had the highest campaign response rate at 28.01%, while Large accounts had the lowest sales win rate at 61.57% and averaged 13.23 tickets per account.

# AI and dashboard comparison

Quick Chat and the dashboard agreed on the main campaign, revenue and account-health findings after the Topic rules were corrected. The first sales win-rate answer counted rows rather than distinct deals. An early complex question also treated the highest response rate and lowest win rate as if they belonged to one segment. Rewording it separated the measures and produced the correct answer.

The dashboard should remain the main tool for weekly reporting because its measures and filters are already defined. Quick Chat is more useful for follow-up questions, especially when the answer needs fields from more than one source. Important figures should be checked against the dashboard before they are used in a decision.

# Recommended next steps

- Review campaign attribution and decide whether NovaEdge Awareness should continue in its current form.

- Apply useful Central region practices in East and West, and tighten product-fit checks.

- Start a recovery review for YieldMax and monitor recent tickets for other high-value Enterprise accounts.

- Refresh SPICE weekly and review unclear or conflicting Quick Chat results.