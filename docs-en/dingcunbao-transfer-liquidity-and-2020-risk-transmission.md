# Dingcunbao Claim-Transfer Liquidity and Yooli's 2020 Risk-Transmission Mechanism

> Updated: 2026-10-16  
> Chinese original: [`有利网定存宝债转流动性与2020风险穿透机制.md`](../docs/有利网定存宝债转流动性与2020风险穿透机制.md)  
> This article separates two risks that are easily conflated in the Yooli case: **credit risk of underlying borrowers** and **liquidity risk in exiting Dingcunbao after the product service period.** Existing contracts, help pages, and 2020 public data indicate that Yooli had two layers of buffering before risk became visible: one was claim-transfer liquidity, and the other was compensation / credit enhancement supplied by asset-side partners and guarantors. The fact that both mechanisms came under pressure from late 2019 through mid-2020 provides a more complete explanation for the rapid shift from “still paying / low overdue” to severe transfer congestion and large lender-facing overdue.
>
> **Evidentiary boundary:** this article describes a transmission mechanism supported by contract structure and public data. Automatic claim transfers and reinvestment of repayments do not themselves prove a fund pool, borrowing from new lenders to repay old lenders, or illegal fund-raising. Those conclusions would require bank records, transaction-level assignment records, and underlying-loan ledgers.
>
> This English version is a research translation. If wording differs, the Chinese original controls.

## 1. First separate two concepts: a Dingcunbao “service period” was not the term of the underlying borrower loan

Yooli's official help page stated that Dingcunbao used a **service period and lock-up period**. When the service period ended:

- if the corresponding borrower loan had already matured, the lender received repayment;
- if the corresponding borrower loan had not matured, the platform initiated a claim transfer under the lender's authorization;
- whether transfer succeeded depended on another registered user being willing to acquire the claim.

Official help page:

- https://m.yooli.com/views/appCommon/help/plans.jsp

The surviving *Dingcunbao Lending Consultation and Service Agreement* is also explicit:

> when the service period expires, Yooli assists with transferring any remaining unmatured claims; the platform **does not guarantee that a claim transfer will be completed**, and claims that cannot be transferred remain with the lender until actual recovery.

Agreement:

- https://m.yooli.com/contract/dcbtzxy.do?typeId=-1

Thus a “3-month,” “6-month,” or “12-month” Dingcunbao service period did not mean that the underlying borrower loans had the same maturity. In many cases, cash exit depended on:

```text
Original lender holds an unmatured claim
        ↓
Dingcunbao service period ends
        ↓
Platform initiates claim transfer
        ↓
Another user acquires the claim
        ↓
Original lender receives cash and exits
```

Therefore, **even if every underlying borrower were still performing, Dingcunbao could experience “the service period ended but I cannot cash out” if demand from new assignees was insufficient.**

### Original-page evidence from 2019-11-18: “no promised transfer time” and “historically within one business day” appeared together

The project's restored Dingcunbao pages from **2019-11-18**, during normal operation, show this structure more clearly than later customer-service explanations.

For a one-month plan, the page said:

- if the underlying loan had not matured when the service period ended, a claim transfer was needed;
- transfer completion depended on market demand;
- **the platform did not guarantee transfer time**;
- if immediate transfer was impossible, the lender might continue holding the claim for a much longer period.

But the same page also stated:

> **“Historically, funds were received within one business day after the Dingcunbao service period ended.”**

The meta description also used phrases equivalent to “automatic lending, scheduled automatic transfer, monthly interest, and principal recovered at maturity.”

This evidence is important because it shows that, before full risk exposure, Yooli did disclose transfer-failure and long-holding risk. At the same time, historical operating experience and product language continuously reinforced an expectation of quick cash receipt after the service period ended. Both facts should be preserved.

Archives:

- https://wayback.yooli-action.online/dingcunbao/
- https://wayback.yooli-action.online/dingcunbao/detail/101.html

---

## 2. Earlier agreements made “automatic transfer at the end of the plan” a core operating feature

Historical versions of Yooli's Dingcunbao agreement described the structure even more directly.

Early versions defined Dingcunbao as an investment plan that automatically invested in loans covered by full principal-and-interest protection from partner institutions and **automatically transferred claims when the investment term ended**.

Those agreements also provided that:

1. during Dingcunbao, principal repaid by underlying borrowers could be automatically reinvested into new loan projects;
2. when the Dingcunbao term expired, Yooli could transfer unmatured underlying claims on the lender's behalf;
3. if claims still could not be transferred, they would revert to the lender and remain held until actual borrower repayment;
4. if an underlying borrower became delinquent and the partner institution **did not immediately perform its guarantee obligation**, that loan could leave the Dingcunbao plan and appear directly in the lender's account.

Historical agreements:

- https://www.yooli.com/static/laws/dcbxyStatic.jsp
- https://www.yooli.com/static/laws/dcbxyStaticV2.jsp
- https://www.yooli.com/static/laws/dcbxyStaticV3.jsp

Some earlier versions also described return of principal or principal and interest within three business days after Dingcunbao expiration, while separately providing special handling if assignment failed.

The daily “maturity experience” therefore depended on three different possible cash sources:

```text
A. normal repayment by underlying borrowers
B. compensation or repurchase by guarantors / partners
C. other lenders purchasing unmatured claims
```

The user saw a single “cash exit” result, but the back-end economic source could differ substantially.

---

## 3. There were at least two risk buffers, not only the guarantee layer

The asset-side investigation establishes that Tongsheng Microcredit, Chengxixiang, Guoyin Shengda, and others provided compensation at different times. Court decisions also show examples where underlying borrowers had defaulted before guarantors later compensated and pursued recovery.

Adding Dingcunbao's contractual mechanics produces a fuller picture:

```text
                  ┌────────────────────────┐
                  │ Layer 1: credit buffer │
Borrower defaults ─→ guarantee / compensation / repurchase
                  └────────────┬───────────┘
                               ↓
                    Lender can still receive money normally

                  ┌──────────────────────────┐
                  │ Layer 2: liquidity buffer│
Service period ends ─→ transfer claim to another user
                  └────────────┬─────────────┘
                               ↓
                    Original lender exits in cash
```

The two buffers could operate together.

For example, a borrower might already have defaulted but a guarantor could compensate, leaving the lender's cash flow looking normal. In another case the borrower loan might still be performing but unmatured when Dingcunbao ended; if another user bought the claim, the original lender could still exit smoothly.

Accordingly, **whether the lender could exit on time did not by itself reveal whether the underlying borrower was performing normally.**

---

## 4. The 2019 regulatory “three reductions” directly weakened the demand that Dingcunbao relied on for claim-transfer liquidity

By 2019 China's P2P sector was in explicit stock-reduction mode.

In July 2019 the national internet-finance and online-lending rectification authorities said that the second half of the year would continue strict implementation of:

- reduction in institution numbers;
- reduction in industry scale;
- reduction in participants;
- transformation and orderly exit as the principal direction.

Official Xinhua/CAC report:

- https://www.cac.gov.cn/2019-07/07/c_1124719562.htm

Industry data also show that active P2P lender numbers had fallen dramatically by end-2019. 01Caijing estimated about **810,000 active lenders in December 2019**, compared with about **3.15 million** a year earlier.

- https://www.01caijing.com/article/255952.htm

This does not quantify Yooli's own monthly inflows. But structurally, **when an entire sector was required to reduce investor participation and outstanding balances, an exit mechanism dependent on other users acquiring old claims would naturally become harder to sustain.**

Even without further asset-quality deterioration, fewer buyers in the claim-transfer market could produce queues after the service period ended.

---

## 5. Public evidence shows that the liquidity problem predated the full July 2020 crisis

In July 2020 media interviews, Yooli customer service acknowledged that:

- Dingcunbao claim transfers were processed according to service-period end date;
- Yooli was still processing some plans whose service periods had ended on **2020-01-01**;
- the platform said that fewer lenders and COVID-related borrower repayment problems had slowed transfers relative to the prior year.

Reports:

- https://news.stcn.com/sd/202007/t20200725_2166328.html
- https://static.nfnews.com/content/202007/25/c3813683.html

This is important because it shows that the “failure” did not suddenly begin in July 2020. **At least some users whose service periods had ended at the beginning of January were still unable to complete transfer and exit six months later.**

Media also carried lender statements that exit times began slowing materially around December 2019. Those statements cannot establish a universal platform-wide default date, but they are consistent with Yooli's own later acknowledgement of long transfer queues.

---

## 6. May–June 2020 brought a more serious change: not only transfers slowed, underlying collections also broke down

Public data changed sharply by end-June 2020.

Media citing National Internet Finance Association data reported:

- current borrowers at end-June: about **1,379,331**;
- only **5,556 fewer** than at end-May;
- in preceding months current borrowers had usually declined by roughly **70,000–80,000 per month**;
- overdue amount reached about **RMB 2.678 billion**;
- overdue increased by about **RMB 1.05 billion** from end-May;
- project overdue rate: about **13.60%**;
- amount overdue rate: about **20.22%**.

Sources:

- https://static.nfnews.com/content/202007/25/c3813683.html
- https://news.stcn.com/sd/202007/t20200725_2166328.html

Yooli stopped new loan disbursements on 2020-06-30.

At the time, the platform also stated that if borrowers referred by partner institutions failed to satisfy contractual conditions, those partners would repurchase and compensate the relevant assets.

From mid-2020 onward, the problem therefore cannot be explained merely as “there are no buyers in the claim-transfer market.” **Actual underlying borrower repayment and overdue performance were deteriorating at the same time.**

The process can be separated into two stages.

### Stage one: exit liquidity deteriorates first

```text
Industry “three reductions” and lower lending demand
        ↓
Unmatured claims become harder to transfer to the next user
        ↓
Dingcunbao queues form after service-period end
        ↓
Users first experience “maturity but no cash exit”
```

### Stage two: underlying credit risk also passes through

```text
Borrower delinquency rises rapidly
        ↓
Guarantee / compensation demand expands
        ↓
Some asset-side and guarantee institutions themselves face capital, litigation, or operating stress
        ↓
Existing risk buffers cannot absorb all default
        ↓
Overdue becomes visible directly on the lender side
```

Once these two processes interacted, transfer liquidity worsened further because fewer users were willing to acquire old claims, creating an obvious negative-feedback loop.

### Additional node: Dingcunbao still accepted new lending in November 2020 after new origination had stopped

A *21st Century Business Herald* test on **2020-11-23** found that Yooli still displayed 3-, 6-, 12-, and 24-month Dingcunbao plans accepting lender funds, with expected annual returns of roughly **6%–10%**.

This does not necessarily contradict the claim that new loan origination stopped on June 30. Historical Dingcunbao agreements allowed new funds to be used either for direct lending or for **acquiring claims already held by other lenders**. Current evidence therefore does not establish that Yooli resumed forming new borrower loans after June 30.

But it makes the transfer question more concrete: **how much of the new money entering Dingcunbao in the second half of 2020 was used to purchase old lenders' existing claims, and what was the delinquency, compensation, extension, or collection status of those claims at the time?**

See:

- [Where Did Dingcunbao Funds Go After Yooli Stopped New Loan Origination?](./fundraising-after-new-origination-stopped.md)

---

## 7. This explains a timing gap that otherwise looks contradictory

The current record shows:

- October 2019: public overdue still zero;
- cumulative compensation already about RMB 603 million;
- late 2019: user reports of slowing exits begin to appear;
- May–June 2020: overdue data rise sharply;
- July 2020: the repayment/exit crisis becomes widely public.

Once Dingcunbao's structure is included, the timing gap becomes easier to explain:

> **underlying borrower risk could first be absorbed by guarantee compensation, while maturity mismatch could be absorbed by claim transfers. As long as both mechanisms worked, the user experience could still resemble normal cash exit. When buyer demand fell, compensation pressure rose, and borrower repayment deteriorated further, risks previously distributed across different layers could pass through to lenders at the same time.**

Accordingly, a more precise formulation than “Yooli suddenly failed in 2020” is:

> **2020 was the period when risks became concentrated and visible on the lender side; it was not necessarily when all of the underlying risks first formed.**

---

## 8. The evidence also requires rejecting the oversimplified model that “all guarantors stopped paying at once”

Current public evidence does not support the idea that all guarantee companies stopped compensation on a single date in 2020.

In fact:

- Chengxixiang still received a renewed financing-guarantee license in January 2020;
- Shenzhen regulators' February 2021 publication of 2019 annual-review results still listed Chengxixiang as “passed”;
- Guoyin Shengda was approved in February 2020 to reduce registered capital from RMB 700 million to RMB 300 million; its license was later shown as valid through 2020-09-17, while its actual controller was publicly disclosed as a dishonest judgment debtor and subject to consumption restrictions;
- the Hemei system experienced severe financial distress in 2019–2020, but listed-company reports continued to mark its “compensation liability completed” field as “yes”; the roughly RMB 92 million Yooli-channel outstanding balance therefore cannot simply be interpreted as proof that Hemei continued guaranteeing every remaining loan;
- later Litong-related litigation suggests Yooli still sought compensation on some historical auto-loan assets after public risk exposure.

A more evidence-consistent model is:

> **guarantee coverage, compensation capacity, and exit timing differed across asset channels. What happened in 2020 was more likely a non-synchronous and uneven degradation of the broader risk-buffer network, rather than every guarantor shutting down simultaneously.**

See:

- [Yooli's Early External Asset Partners and Guarantee Network](./early-external-asset-partners-and-guarantee-network.md)
- [Yooli Asset-Side Guarantee and Recovery Network Investigation](./asset-side-guarantee-and-recovery-network.md)
- [Yooli Asset-Side and Guarantee-System Contraction Timeline](./asset-side-and-guarantee-system-contraction-timeline.md)

---

## 9. The most complete current model of 2020 risk transmission

```text
2018–2019
Underlying borrower defaults already exist
        ↓
Guarantor compensation / repurchase / recovery
        ↓
Lender side can still show low or zero overdue

2019
Industry “three reductions” and faster exit
        ↓
New lending demand and claim-assignment demand fall
        ↓
Liquidity for Dingcunbao maturity transfers weakens

Late 2019–early 2020
Some users begin queuing after service-period end
        ↓
Old claims become harder to place with new assignees

Early 2020
COVID shock + accumulated asset-quality problems
        ↓
Borrower repayment weakens and compensation demand rises
        ↓
Some asset-side / guarantee institutions face capital, judicial, and operating stress

May–June 2020
Underlying overdue rises rapidly
        +
Claim-transfer market already seriously congested
        ↓
Liquidity buffer and credit buffer both fail or weaken materially

2020-06-30
New loan origination stops
        ↓
Original automatic investment / transfer rhythm can no longer rely on continuing new business

July 2020 onward
Large transfer queues + lender-facing overdue becomes visible
        ↓
Discounted exits, look-through underlying claims, asset disposal, AMC and other wind-down routes emerge
```

This model fits the existing timeline better than either “COVID alone caused borrowers to stop paying” or “the guarantors suddenly stopped backstopping everything.”

---

## 10. One central question remains unanswered by public evidence

Dingcunbao's structure is not, by itself, unlawful. “Reinvest borrower repayments + transfer claims at service-period end” cannot simply be labeled a fund pool or new-money-for-old-money repayment.

The question that needs transaction-level evidence is:

> **Once claim transfer had already slowed materially in late 2019 and underlying defaults and compensation were rising rapidly into 2020, which old claims were being transferred to which new lenders? Were claims already overdue, already identified as high risk, or experiencing abnormal compensation still being used for automatic investment or claim transfer?**

The needed evidence is not more marketing material but transaction-level data:

1. the underlying loan ID corresponding to each Dingcunbao investment;
2. time, amount, and new underlying loan for each automatic reinvestment;
3. original holder, assignee, price, and time for every claim transfer;
4. actual repayment / delinquency status of the underlying loan at transfer;
5. whether the relevant guarantor had compensated, refused compensation, or lost guarantee liability;
6. daily new lender inflows, borrower repayments, guarantee compensation, and claim-transfer transaction amounts from 2019-12 through 2020-06.

Any authentic ledger of this kind could answer the central historical question:

> **Before 2020, how much of Yooli's “normal exit” came from actual borrower repayments, how much from guarantee compensation, and how much depended on the next lender acquiring the old claim?**

That is one of the most important remaining layers in reconstructing the Yooli event.