# Yooli Serious-Default Loans: Contract Maturity and Publication-Lag Analysis

> Compiled: 2026-10-13  
> Chinese original: [`严重失信贷款合同到期与公示滞后分析.md`](../docs/严重失信贷款合同到期与公示滞后分析.md)  
> Data basis: Yooli serious-default borrower notices, batches 1–295.  
> Reproducible statistics: [Maturity-date statistical matrix](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/maturity-matrix.md)  
> This English version is a research translation. If wording differs, the Chinese original controls.

## 1. Why calculate the final contractual maturity date separately?

Looking only at the fact that loans were originated in 2016–2018 shows that they came from earlier years. It does **not** prove that the loans had already matured in 2019, much less that they had already defaulted.

For that reason, every serious-default notice record was recalculated using:

> **Final contractual maturity date = loan start date + loan term (months)**

The resulting dates were then compared with **2019-10-31**, when Yooli was still publicly reporting zero overdue projects and zero overdue amount.

This is a more conservative and more precise time-based look-through method than simply examining origination year.

---

## 2. Core result: a large share of loans later classified as serious defaults had already completed their original contractual terms before the “zero overdue” date

After removing 75 duplicate records created by repeated image references within the same batch, batches 1–295 contain **621,387 records**.

Batch 214 contains **2,000 records** for which the original table did not provide a loan term, so a final maturity date cannot be calculated. The remaining **619,387 records** are calculable.

The results are:

- **481,434 records** had a final contractual maturity date no later than **2019-10-31**, representing about **77.73%** of calculable records;
- the overdue amounts later published for those records, accumulated by notice appearance, total about **RMB 6.26570 billion**, or approximately **64.01%** of the calculable amount;
- among them, **301,479 records**, corresponding to about **RMB 2.57891 billion**, had already reached final contractual maturity by **2018-12-31**.

A sensitivity analysis using a strict masked-record fingerprint to remove identical cross-batch appearances produces the same basic result:

- final maturity before 2019-10-31: **441,695 records, about RMB 6.11316 billion**;
- final maturity before the end of 2018: **274,445 records, about RMB 2.50326 billion**.

Accordingly, the explanation that “most loans that later became serious-default assets had not yet matured in 2019” is inconsistent with the available data.

---

## 3. The most important layer: loans that had already matured by end-2018 but were not published as serious defaults until years later

For the **301,479 records whose final contractual maturity was no later than 2018-12-31**, later publication years break down as follows:

| Later publication year | Records | Accumulated overdue amount by notice appearance |
| --- | ---: | ---: |
| 2020 | 36 | **RMB 0.00027 bn** |
| 2021 | 16,632 | **RMB 0.09049 bn** |
| 2022 | 139,386 | **RMB 1.83519 bn** |
| 2023 | 86,794 | **RMB 0.49569 bn** |
| 2024 | 58,631 | **RMB 0.15728 bn** |

In other words, among loans later classified as serious defaults, original contracts corresponding to about **RMB 2.579 billion** had reached their final contractual maturity no later than the end of 2018. Roughly **RMB 2.488 billion** of those records were not published as serious defaults until **2022–2024**.

This does **not** mean that these loans remained wholly unpaid from 2018 onward. Interim events could include ordinary installment payments, extensions, restructurings, guarantee compensation, or other arrangements.

It does, however, rule out a weaker explanation:

> **It is not sufficient to say that these loans had not yet contractually matured in 2019 and therefore the platform could not yet observe their ultimate performance.**

For loans already beyond their original final maturity date and later classified as serious defaults, their actual 2019 performance status, compensation status, extension history, and internal risk classification are highly relevant investigative questions.

---

## 4. Final maturity year × later publication year

Accumulated amount by notice appearance:

| Final contractual maturity year | 2020 notices | 2021 notices | 2022 notices | 2023 notices | 2024 notices | Total |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| 2015 | RMB 0.0000 bn | RMB 0.0000 bn | RMB 0.0000 bn | RMB 0.00001 bn | RMB 0.0000 bn | **RMB 0.00001 bn** |
| 2016 | RMB 0.0000 bn | RMB 0.0000 bn | RMB 0.06268 bn | RMB 0.03989 bn | RMB 0.00106 bn | **RMB 0.10363 bn** |
| 2017 | RMB 0.0000 bn | RMB 0.0000 bn | RMB 0.52761 bn | RMB 0.22492 bn | RMB 0.04755 bn | **RMB 0.80008 bn** |
| 2018 | RMB 0.00027 bn | RMB 0.09049 bn | RMB 1.24490 bn | RMB 0.23086 bn | RMB 0.10866 bn | **RMB 1.67518 bn** |
| 2019 (through October) | RMB 0.00090 bn | RMB 1.02320 bn | RMB 2.44661 bn | RMB 0.13903 bn | RMB 0.07706 bn | **RMB 3.68678 bn** |

This further shows that the later serious-default notices were progressively reaching backward into loans whose contractual terms had ended much earlier during the wind-down. They were not merely recording “new defaults occurring in the year of publication.”

---

## 5. Loan-term structure is also notable

Among records that had reached final contractual maturity by 2019-10-31 and were later published as serious defaults, the largest amounts were concentrated in:

- **24-month loans:** about **RMB 3.16360 billion**;
- **36-month loans:** about **RMB 1.09320 billion**;
- **18-month loans:** about **RMB 844.71 million**;
- **12-month loans:** about **RMB 771.12 million**.

The 24-month loans are particularly prominent: about **RMB 745.99 million** was published in 2021 and about **RMB 2.18259 billion** in 2022.

This means that a large body of medium- and long-term loans later classified as serious defaults had already completed their entire original contract terms before Yooli’s 2019 “zero overdue” disclosure point.

---

## 6. What does this mean for Yooli’s “zero overdue” disclosure in 2019?

The available evidence still does **not** prove the stronger proposition that:

> “All of these loans were already overdue on 2019-10-31 and Yooli intentionally reported them as zero.”

That conclusion would exceed the evidence because there may have been:

- loan extensions or debt restructurings;
- timely compensation by guarantors or asset partners;
- repayment of the original loan followed by changes elsewhere in the claim chain;
- a disclosure metric that measured whether the **lender** had received scheduled principal and interest, rather than whether the underlying borrower had defaulted.

But once the maturity statistics are placed directly alongside the public disclosure, the question can be stated much more precisely:

> **As of 2019-10-31, original contracts corresponding to about RMB 6.26570 billion of loans later appearing in Yooli’s serious-default notices had already reached their final maturity date. At the same time, Yooli was still publicly reporting zero overdue amount and cumulative compensation of only about RMB 603 million. Public materials do not explain the actual performance status of this matured loan population at that date. Further investigation is needed to determine whether these loans had been extended, restructured, compensated, or had already experienced underlying borrower default that was not reflected in the lender-facing “overdue” metric.**

It remains incorrect to subtract **RMB 603 million** from **RMB 6.26570 billion** and call the result an “undisclosed bad-debt gap.” The first number is cumulative compensation through 2019-10-31; the second is the later notice-appearance accumulated overdue amount for loans whose original contracts had matured by that date. The dates and statistical definitions are different.

The more useful question is:

> **Of the tens of billions of yuan of loans whose original contracts had already matured by 2019-10-31 and that later entered serious-default notices, how many had already experienced borrower default, how many had been absorbed by guarantee/compensation arrangements, and how many had been extended or restructured? How did Yooli’s internal underlying-delinquency and compensation data compare with what lenders saw publicly?**

That question is much more testable than simply reasoning backward from the later size of bad debt.

---

## 7. Evidence actually needed next

To move from a significant question to a firmer factual conclusion, the following materials are needed for loans already beyond final contractual maturity:

1. underlying-loan repayment schedules and actual cash-flow records;
2. first delinquency date;
3. guarantee/compensation date and actual amount paid;
4. extension or restructuring agreements and execution dates;
5. internal platform risk classifications and collection-status changes;
6. underlying-loan delinquency, compensation, and migration rates for 2018–2020.

If these materials show that large numbers of loans had already substantively defaulted in 2019 while ordinary lenders were still mainly shown “zero overdue,” the evidentiary chain concerning risk disclosure would be materially strengthened.

---

## 8. Statistical definitions and boundaries

- This analysis calculates the **final contractual maturity date**, not every installment due date. It is therefore conservative for identifying earlier installment delinquency.
- The 2,000 records in batch 214 lack a loan term in the original table and are excluded from maturity-date calculations.
- Amounts remain official serious-default notice amounts accumulated by **notice appearance**. They cannot be equated directly with unique outstanding principal.
- The strict fingerprint uses masked identity fields, loan start date, term, and amount. It is only a sensitivity test for completely identical cross-batch records and is not a substitute for a true unique borrower or unique claim ID.

Full matrices and scripts:

- [Maturity-date statistical matrix](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/maturity-matrix.md)
- [Maturity month × loan term × publication-batch matrix (CSV)](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/maturity-month-term-publication-matrix.csv)
- [Statistical script](https://github.com/stepfunc-droid/yooli-public-notice-archive/blob/master/statistics/scripts/build_maturity_matrix.py)