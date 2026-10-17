# Yooli Serious-Default Borrower Notice Statistics and the “Zero Overdue” Question

> Compiled: 2026-10-13  
> Chinese original: [`有利网严重失信借款人公示统计与零逾期疑点分析.md`](../docs/有利网严重失信借款人公示统计与零逾期疑点分析.md)  
> Data: Yooli serious-default borrower notices, batches 1–295; structured statistics; and Yooli public operating data from 2019–2021.  
> Original notice archive and reproducible statistics: [`yooli-public-notice-archive`](https://github.com/stepfunc-droid/yooli-public-notice-archive)
>
> **Statistical note:** this article aggregates Yooli's official serious-default borrower notices from batches 1–295. The RMB 9.794 billion figure is the sum of readable “overdue amount” values **by notice appearance**. It is not the platform's real-time overdue balance on any one date and is not automatically equal to unique claim principal. A strict masked-fingerprint sensitivity analysis is used below to test exact cross-batch duplicate records.
>
> This English version is a research translation. If wording differs, the Chinese original controls.

## 1. Overall scale of the 295 serious-default notice batches

Yooli began publishing “serious-default borrower” lists in June 2020. The current archive covers batches 1 through 295, from **2020-06-25** through **2024-10-29**.

After removing 75 duplicate records created when the same image was referenced twice within an original notice page, the archive contains:

| Metric | Result |
| --- | ---: |
| Notice batches | **295** |
| Official notice records | **621,387** |
| Cumulative readable overdue amount | **RMB 9,794,144,241.81** |
| Equivalent | **about RMB 9.794 billion** |
| Records with unreadable amount | **2** |

Reproducible outputs:

- [Summary JSON](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/summary.json)
- [Yearly summary CSV](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/yearly-summary.csv)
- [Verification report](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/verification.json)

The notices therefore cover hundreds of thousands of small-loan records with cumulative readable overdue amounts approaching RMB 10 billion by notice appearance. Because borrower identity fields are masked and no true unique claim ID is available, this project does **not** describe the RMB 9.794 billion as mutually exclusive unique bad-debt principal.

---

## 2. First finding: loans later published as serious defaults are heavily concentrated in 2016–2018 originations

Grouped by loan start year:

| Loan start year | Notice records | Readable overdue amount |
| --- | ---: | ---: |
| 2015 | 9,366 | **RMB 1.005bn** |
| 2016 | 119,827 | **RMB 2.244bn** |
| 2017 | 319,166 | **RMB 4.853bn** |
| 2018 | 110,132 | **RMB 1.444bn** |
| 2019 | 62,868 | **RMB 247m** |
| 2020 | 28 | **RMB 207,800** |

Loans originated in **2016–2018 account for about RMB 8.542 billion, roughly 87.2% of all readable notice amounts**. Loans originated in 2017 alone account for approximately **RMB 4.853 billion, about 49.6%**.

This origination-year distribution is important.

It shows that the severe delinquencies publicized after 2020 were not mainly loans newly originated in 2020. The overwhelming majority of the later serious-default records correspond to loans originated in 2016–2018.

In other words, **2020 looks more like the period when large volumes of historical loan risk became visible. But loan-origination year alone cannot be used to backdate the formation of risk or the date of default to 2016–2018.**

A 2017 loan was not necessarily delinquent in 2017. But the notices include many 18-, 24-, and 36-month terms. A 2017 loan with an 18- or 24-month term would already have entered or completed its original maturity phase by 2019.

That creates an important timing question between the large amount of later serious-default assets originated in 2017 and Yooli's continuing “zero overdue” reporting in 2019.

---

## 3. The notice process itself shows that Yooli was progressively working backward through old assets

The 295 batches are not “new bad debts incurred in the publication period.” The sequence shows the platform progressively reaching further back into older loan vintages:

- **Batch 1, 2020-06-25:** many records from 2019 originations;
- **Batch 102, 2022-01-04:** large numbers of 2017 loans appear;
- **Batch 214, 2023-02-13:** the list reaches mainly late-2016 loans;
- **Batch 295, 2024-10-29:** loans from mid-2016 are still being published.

Original tables:

- [Batch 1](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/tables/batch-0001.csv)
- [Batch 102](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/tables/batch-0102.csv)
- [Batch 214](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/tables/batch-0214.csv)
- [Batch 295](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/tables/batch-0295.csv)

By publication year, the 2021 and 2022 notices together account for about **RMB 8.772 billion, roughly 89.6%** of cumulative notice amounts.

Thus, a large number of loans published in 2022 should not be interpreted as loans that first became bad in 2022. A more reasonable reading is that **during the wind-down, old loans originated years earlier were progressively identified, organized, and entered into the serious-default publication process.**

---

## 4. Put on one timeline, the 2019 “zero overdue” issue becomes prominent

| Time | Outstanding loan balance | Cumulative compensation | Public overdue / bad-debt status |
| --- | ---: | ---: | --- |
| **2019-10-31** | **about RMB 12.6bn** | **about RMB 603m** | Overdue projects and overdue amount both **0** |
| **Jul. 2020** | **RMB 11.418bn** | **about RMB 4.891bn** | Overdue amount **about RMB 2.678bn**, project overdue rate 13.60% |
| **End-Mar. 2021** | **about RMB 8bn** | **about RMB 5bn** | Yooli said bad debt near **RMB 7bn**, underlying overdue rate near **90%** |
| **2020–2024 serious-default notices** | — | — | Cumulative notice-appearance overdue amount **about RMB 9.794bn**, 87.2% from 2016–2018 originations |

2019 operating-data archive:

- https://wayback.yooli-action.online/statistic/platform/index.html

Related data reconstruction:

- [Yooli's Last Public Operating Data](./last-public-operating-data.md)
- [Yooli Event Timeline](./yooli-event-timeline.md)

Three points can be established.

First, **risk transmission accelerated extremely quickly.** From October 2019 to July 2020, cumulative compensation rose from about RMB 603 million to about RMB 4.891 billion, an increase of roughly **RMB 4.288 billion**, while public overdue went from zero to about **RMB 2.678 billion**.

Second, **the problem assets exposed in 2020 were not mainly new 2020 loans.** The later serious-default notices are dominated by 2016–2018, especially 2017, originations.

Third, by 2021 Yooli itself said the underlying overdue rate was close to 90% and bad debt close to RMB 7 billion. That shows the final underlying credit picture was very different from what a lender might infer from a single “zero overdue” metric in 2019.

### Deeper look-through: final contractual maturity shows that many later serious-default loans had already matured before the 2019 “zero overdue” date

Origination year alone does not tell whether a 2017 loan had matured by 2019. The notice archive therefore calculates final contractual maturity as loan start date plus original term.

Results:

- after removing duplicate images within batches, there are **621,387** records;
- batch 214 contains **2,000 records** without loan-term data, so final maturity cannot be calculated for them;
- among the remaining **619,387 calculable records**, **481,434 (77.73%)** had final contractual maturity no later than **2019-10-31**;
- those records later carried cumulative notice-appearance overdue amounts of about **RMB 6.26570 billion (64.01%)**;
- **301,479 records, about RMB 2.57891 billion**, had reached final contractual maturity by **2018-12-31**;
- among records matured by 2019-10-31, 2017 originations accounted for **288,577 records, about RMB 3.01854 billion**, and 2016 originations about **RMB 1.95362 billion**;
- after a conservative strict-fingerprint sensitivity removal of exact cross-batch duplicates, records matured by 2019-10-31 still total **441,695 records and about RMB 6.11316 billion**.

This is stronger evidence than simply saying “the loans were originated in 2016–2018.” Large amounts of the loans later appearing in serious-default notices had already passed their original final contractual maturity by 2019-10-31.

But the evidentiary boundary remains essential: **final contractual maturity ≠ judicially established default ≠ proof that Yooli had already classified the loan as bad debt at that time.** Extensions, restructurings, and guarantee compensation may have intervened. The missing evidence is the contemporaneous loan-level repayment, extension, and compensation record.

Reproducible maturity analysis:

https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/maturity-analysis.md

---

## 5. Yooli's “nearly RMB 7bn bad debt” and the RMB 9.794bn notice total cannot be directly subtracted

In April 2021 Yooli's *Recent Update on the Company* described bad debt as “nearly **RMB 7 billion**.” The readable overdue amounts in notice batches 1–295 sum to approximately **RMB 9.794 billion** by notice appearance. The apparent gap of roughly RMB 2.794 billion is **not** presently an interpretable “missing bad-debt amount.”

The figures differ in date and definition, while RMB 9.794 billion remains a notice-appearance aggregate.

A strict-fingerprint sensitivity analysis finds **41,546 exact additional cross-batch records totaling about RMB 195.22 million**, approximately **1.99%** of calculable cumulative notice amount. Exact duplicates therefore exist but are not the main explanation for the RMB 9.794 billion figure.

However, the strict fingerprint cannot identify the same claim if its remaining amount changes across publications, and masked identities do not provide a true unique claim ID. Further deterioration after 2021 and the difference between “bad debt” and “overdue amount” also matter.

Accordingly, **the apparent RMB 2.794 billion difference must not be presented as proof that Yooli underreported bad debt.**

The two metrics should be preserved separately until unique-claim de-duplication and definitions can be reconciled. The more useful research questions are: how many unique claims remain, when did each first become delinquent, when was it compensated, and when did the platform internally classify it as bad debt?

---

## 6. “Zero overdue” most likely described whether lenders received money on time, not whether underlying borrowers were performing

This distinction follows from Yooli's own disclosed metrics.

In October 2019, Yooli reported approximately **RMB 603 million across 86,441 compensated cases** while still showing overdue at zero. Under the regulatory disclosure definition, if a borrower defaults but a third party compensates in time so that the lender receives principal and interest on schedule, the lender-facing overdue amount can remain zero.

Yooli's historical safety messaging used the same logic: a surviving help page says that since launch the platform had “not had a single overdue case” and lenders received principal and return on the repayment date, while separately explaining that a guarantor would compensate after borrower default.

Thus, **“zero overdue in 2019” did not establish zero underlying borrower default. It more closely indicated that borrower defaults were still being absorbed before they became missed lender receipts.**

That distinction separates two very different questions:

> **Did the lender receive money on time?** versus **Was the underlying borrower's credit quality deteriorating?**

Later data show those two questions eventually diverged dramatically.

---

## 7. What the existing data already support

### 7.1 Underlying risk did not suddenly arise from zero in 2020

Yooli had already reported roughly RMB 603 million of cumulative compensation by October 2019. Borrower-level default and credit loss therefore existed before 2020. The later serious-default notices also show that much of the ultimately problematic stock consisted of older loans, with a significant share already past original contractual maturity by 2019-10-31.

That does not establish that every such loan had already defaulted in earlier years or that Yooli already knew its ultimate loss severity.

### 7.2 “Zero overdue” in 2019 was not a measure of healthy underlying asset quality

The existence of RMB 603 million in cumulative compensation directly means borrower-level default was not zero.

The lender-facing zero-overdue figure showed only that risk had not yet fully passed through to lender receipts. It did not mean the underlying loan pool had no credit losses.

### 7.3 The central change from late 2019 through mid-2020 was the rapid failure of mechanisms that had absorbed risk

In less than a year, cumulative compensation increased by about RMB 4.288 billion while public overdue rose to about RMB 2.678 billion. The mechanisms that had previously allowed lender-side overdue to remain at or near zero were no longer able to cover all underlying stress.

A more accurate description of 2020 is therefore:

> **risk began passing directly from underlying borrowers and the compensation system through to lenders.**

### 7.4 Later serious-default notices make the “old asset” nature of the crisis clearer

2017-originated loans account for about RMB 4.853 billion of cumulative serious-default notice amounts, the largest annual cohort. The 2016–2018 cohorts together account for 87.2%.

This sharpens the disclosure question: **as these older loans matured and compensation pressure increased, did the risk metrics and public messaging presented to ordinary lenders in 2018–2019 adequately communicate what was happening in the underlying pool?**

During the same period Yooli continued emphasizing compliant leading-platform status, regulatory-system connectivity, filing/pilot prospects, bank depository, steady operation, and “safe, authentic, trustworthy” services.

### 7.5 The 2021 “nearly RMB 7bn bad debt” figure was not the final ceiling of historical problem assets later appearing in notices

The later official notice appearances sum to approximately RMB 9.794 billion, compared with Yooli's 2021 statement of nearly RMB 7 billion bad debt. Because dates and definitions differ, this does not prove underreporting. It does show that the 2021 bad-debt number was not a final upper bound on all historical problem assets later exposed through serious-default notices.

Related analysis:

- [Yooli “Compliance / Pilot” Promotion and Risk Disclosure](./compliance-pilot-promotion-and-risk-disclosure.md)
- [Yooli's “150,000 Fully Repaid” Figure and the Payout Boundary](./full-recovery-cohort-and-payout-boundary.md)

---

## 8. Conclusion

The greatest value of the first 295 serious-default notice batches is not simply to produce a headline “RMB 9.794 billion bad debt” number. It fills an important gap in the earlier public record: **when were the loans that later became serious-default assets originally made?**

The answer is highly concentrated: mainly **2016–2018, especially 2017**.

Placed alongside Yooli's October 2019 zero-overdue disclosure, roughly RMB 603 million in cumulative compensation, and the subsequent jump of compensation and overdue to billions of renminbi within less than a year, the notices support a coherent risk-evolution chain:

> **large volumes of historical loans enter repayment and maturity phases → underlying defaults are initially absorbed through guarantees and compensation, allowing lender-side metrics to remain at “zero overdue” → compensation rises sharply from late 2019 into mid-2020 → risk-absorption and claim-transfer mechanisms can no longer maintain the previous structure → overdue becomes visible to lenders → during the following years Yooli continues processing and publishing large volumes of serious-default loans originated in 2016–2018.**

The exact first-default date for each loan cannot be reconstructed from the notice list, so the later cumulative amount cannot be backdated into a 2019 overdue balance. But the public evidence is sufficient to establish that:

> **Yooli's 2019 “zero overdue” cannot be understood as zero underlying asset risk. A large part of the risk that became visible in 2020 came from older loans formed over preceding years, while the lender-facing overdue metric disclosed in 2019 did not display the scale of underlying risk that later emerged.**

Yooli's 2021 “nearly RMB 7 billion bad debt” statement and the approximately RMB 9.794 billion cumulative notice-appearance overdue amount should remain separate metrics until unique claim IDs and precise bad-debt/overdue definitions can be reconciled.