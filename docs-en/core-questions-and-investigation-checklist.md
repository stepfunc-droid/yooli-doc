# Current Core Questions and Investigation Checklist

> Updated: 2026-10-14  
> Chinese original: [`当前核心问题与调查清单.md`](../docs/当前核心问题与调查清单.md)  
> This is not a list of conclusions and does not presuppose a characterization of Yooli. It is a working list of the questions the project most needs to answer: what is already known, what remains missing, and which evidence would materially narrow the investigation.  
> This English version is a research translation. If wording differs, the Chinese original controls.

## 1. What did Yooli’s “zero overdue” figure in October 2019 actually mean?

This remains the central question.

As of 2019-10-31, Yooli publicly reported zero overdue projects and zero overdue amount, while cumulative guarantee compensation had already reached about **RMB 603 million**. This means “zero overdue” cannot simply be read as “all underlying borrowers were repaying normally.” A more plausible mechanism is that if guarantees, compensation, or other arrangements ensured that lenders received scheduled payments, the lender-facing overdue metric could remain zero even when underlying borrowers had defaulted.

The unresolved issue is how much underlying risk this accounting/disclosure structure obscured from ordinary lenders. When a user saw “zero overdue,” could that user reasonably understand that a substantial volume of underlying default and compensation pressure already existed?

Related analyses:

- [Yooli Serious-Default Borrower Notice Statistics and the “Zero Overdue” Question](./severe-default-notice-statistics-and-zero-overdue.md)
- [Yooli “Compliance / Pilot” Promotion and Risk Disclosure](./compliance-pilot-promotion-and-risk-disclosure.md)

## 2. What was the actual 2019 status of the roughly RMB 6.266 billion of later serious-default loans whose original contracts had already matured?

This is one of the most important new lines of inquiry.

Among loans later appearing in Yooli’s serious-default notices, original contracts corresponding to about **RMB 6.26570 billion** in later notice-appearance accumulated overdue amount had final contractual maturity dates no later than **2019-10-31**. About **RMB 2.57891 billion** had reached final contractual maturity by the end of 2018.

At the same time, Yooli was still reporting zero overdue amount on 2019-10-31 and cumulative compensation of about RMB 603 million.

It would be incorrect to say that Yooli already had RMB 6.266 billion of bad debt in 2019. Those later-noticed loans may have undergone extensions, restructurings, ordinary repayments, guarantee compensation, or other arrangements, and the RMB 6.26570 billion and RMB 603 million figures use different dates and statistical definitions and cannot simply be subtracted.

But the factual question is now very specific: **what was the actual status on 2019-10-31 of loans that had already passed their original final maturity date and later became serious-default assets?**

If they had been extended, where are the extension agreements and when were they signed? If they had been compensated, by whom, when, and for how much? If borrowers had already defaulted, when did the platform internally identify that default?

Related analysis:

- [Yooli Serious-Default Loans: Contract Maturity and Publication-Lag Analysis](./severe-default-loan-maturity-and-publication-lag.md)

## 3. Why did risk become visible so rapidly from late 2019 into 2020?

The public figures deteriorated very quickly.

In October 2019 Yooli still reported zero overdue and about RMB 603 million of cumulative compensation. By July 2020, public overdue amount was about **RMB 2.678 billion** and cumulative compensation about **RMB 4.891 billion**. By the end of March 2021, Yooli itself said bad debt was close to **RMB 7 billion** and the underlying-loan overdue rate was close to **90%**.

The issue is not simply that “bad debt later became large.” The question is when the risk actually formed. Did asset quality deteriorate dramatically in a short period during 2020, or had substantial risk already accumulated earlier but been absorbed or delayed through compensation, claim transfer, extensions, restructuring, or other mechanisms that kept lender-facing performance looking normal?

Monthly underlying delinquency migration, compensation, extension, and collection data would materially clarify this timeline.

Related analyses:

- [Yooli’s Last Public Operating Data](./last-public-operating-data.md)
- [Yooli Event Timeline](./yooli-event-timeline.md)

## 4. How much underlying borrower default was absorbed by the compensation system?

Yooli long displayed two facts at the same time: very low or zero lender-facing overdue, while cumulative compensation kept increasing.

Those facts are not necessarily contradictory, but they expose an important distinction: **whether lenders received money on time is not the same question as whether underlying borrowers paid on time.**

The project therefore needs to know how many borrowers had already defaulted in 2018–2019, how much of that default was absorbed by guarantors or asset partners, whether compensation capacity was sufficient to cover the underlying risk at the time, and when that capacity began to become materially constrained.

If the 2020 crisis was substantially the point when mechanisms that had previously absorbed default could no longer do so, that would explain the event better than looking only at why the disclosed overdue number changed.

## 5. Was there too large a gap between Yooli’s public messaging and the risks an ordinary lender could realistically see?

During 2018–2019, Yooli continued to emphasize compliance, connection to industry or regulatory systems, bank depository, registered capital and risk resistance, filing or pilot prospects, and descriptions such as “safe, authentic and trustworthy.”

Those statements do not automatically constitute false advertising, and many had some public factual basis. But when placed beside “zero overdue,” a more practical question emerges: if underlying default and compensation pressure were already rising, how much of that deterioration could an ordinary lender actually perceive from the platform’s public pages and communications?

This is why the project distinguishes between “whether the platform disclosed something” and “whether the overall disclosure was sufficient for an ordinary user to understand the substantive risk.”

Related analyses:

- [Yooli “Compliance / Pilot” Promotion and Risk Disclosure](./compliance-pilot-promotion-and-risk-disclosure.md)
- [Yooli’s “150,000 Fully Repaid” Figure and the Payout Boundary](./full-recovery-cohort-and-payout-boundary.md)

## 6. How many real, independently recoverable assets remained during the wind-down?

The readable overdue amount accumulated by notice appearance across the later serious-default publications is about **RMB 9.794 billion**, but that is not a unique-principal figure and is not the live bad-debt balance at one point in time.

Cross-batch duplicate appearances exist. A strict fingerprint sensitivity analysis removes some exact duplicates, but masked identities and changing remaining balances mean the archive still cannot deduplicate to a true unique-claim ID.

So a core wind-down question remains unresolved: **how many independent claims still existed, what was their remaining principal, how much had already been recovered historically, and how much could realistically still be recovered?**

This directly affects the economic value of later claim-recognition, discounted exit, self-collection, and asset-disposal schemes.

Related analysis:

- [Yooli Debt-Claim Recognition and Terminal Risk Transfer](./debt-claim-substitution-and-terminal-risk-transfer.md)

## 7. What do the existing audit and compliance reports actually prove, and what do they not prove?

The project has financial audits, a special audit, and a lawyer’s compliance assessment. These are important sources, but their evidentiary scope should not be enlarged beyond what they actually examined.

The special audit used a defined scope and sampling procedures; the compliance assessment likewise was not a forensic, transaction-by-transaction look-through of every underlying borrower, related party, asset-side relationship, and cash flow.

Accordingly, the project does not treat those reports as proving that a fund pool, self-financing, undisclosed related-party transactions, or other problems could not have existed. Nor does it infer the opposite merely because Yooli later encountered a crisis.

Questions of that kind require full cash-flow records, related-party look-through analysis, underlying-loan repayment records, and internal risk classifications.

## 8. Who paid lenders during the time gap between borrower default and formal guarantor compensation?

Public court decisions now show that in some consumer-loan samples, **the first missed borrower payment and the guarantor’s formal compensation were separated by months or even longer**.

That means the simplified explanation “the borrower defaulted, the guarantor immediately compensated, so lender-side overdue stayed at zero” does not explain every sample.

What is needed for the same underlying loan is a three-part record:

- when and how much the borrower actually paid each period;
- when and how much the lender actually received each period;
- when and how much any guarantor, cooperation reserve, repurchase party, or other entity filled the gap.

If the lender continued to receive scheduled payments while the borrower had stopped paying and the guarantor had not yet formally compensated, the source of that **funding bridge** must be identified. Current public materials do not establish that the platform itself advanced the funds, maintained a fund pool, or used new lender money to pay earlier lenders.

Related analysis:

- [Yooli Guarantee-Compensation Delays and the “Zero Overdue” Funding-Bridge Question](./guarantee-compensation-delay-and-zero-overdue-funding-bridge.md)

## 9. What did new Dingcunbao funds buy after 2020-06-30?

Yooli publicly said that it stopped new loan disbursements on 2020-06-30, yet a media test on **2020-11-23** still found 3-, 6-, 12-, and 24-month Dingcunbao plans open for participation.

Those facts are not necessarily inconsistent because the Dingcunbao agreement allowed new funds to **acquire existing claims on the platform**.

The question must therefore be answered claim by claim:

- was the money used for a newly originated loan or to acquire an old claim?
- if an old claim, when was the original loan first disbursed?
- who was the prior claim holder?
- what was the transfer price?
- had the underlying borrower already experienced overdue, compensation, extension, or collection events at the time of transfer?
- what risk information did the new assignee see?

Related analysis:

- [Where Did Dingcunbao Funds Go After Yooli Stopped New Loan Origination?](./fundraising-after-new-origination-stopped.md)

## 10. Who was the third-party asset-management company in the wind-down, and what were the acquisition price and cash flows?

Public announcements from 2021–2022 establish that the third-party asset-management company was not merely an abstract label. It had a formal cooperation agreement with Yooli, actually funded claim acquisitions, and later participated in acquisition, substitution, and re-transfer of claims in the locality-based recognition mechanism.

Yet the most important transaction terms remain undisclosed:

- full company name and unified social credit code;
- shareholders and actual controller;
- whether it was related to platform shareholders, executives, or historical asset-side institutions;
- total face amount purchased and average discount;
- payment route;
- actual post-acquisition recoveries;
- asset-quality differences before and after locality-based claim substitution.

Any authentic cooperation-agreement cover/signature page, claim-transfer order, payment record, or claim schedule could turn this anonymous disposal chain into a concrete transaction involving an identifiable legal entity and price.

Related analysis:

- [Yooli Debt-Disposal Authorization and the Third-Party AMC Mechanism](./debt-disposal-authorization-and-third-party-amc.md)

## 11. What did the cluster of early-2020 asset-side and guarantee-side changes actually do to the system’s risk-absorption capacity?

Several independent events are now confirmed: Guoyin Shengda’s capital reduction, Puhui Kuaixin’s capital reduction, liquidation of Shenzhen Honghe Boji Commercial Factoring, multiple Chengxixiang recovery cases transferred to police after courts said the company “may be suspected of a crime,” and judicial auction of Hemei Zhike equity.

Those events **cannot be turned into a single causal chain merely because they occurred close in time**, and they do not establish coordinated asset transfer.

They do show, however, that around the time Yooli’s public risk exposure accelerated, several important asset-origination, guarantee, and credit-enhancement nodes were themselves undergoing capital, judicial, or operating stress.

The evidence actually needed is business-level data for those entities:

- monthly compensation paid and uncompensated balances;
- when new cooperation stopped;
- when compensation obligations were reduced or ceased in practice;
- actual recovery proceeds from collection/litigation;
- whether capital reductions, liquidations, and judicial events affected existing guarantee obligations.

Related analysis:

- [Yooli Asset-Side and Guarantee-System Contraction Timeline](./asset-side-and-guarantee-system-contraction-timeline.md)

## 12. How large was the time gap between what regulators knew and what ordinary lenders could see on Yooli’s public website?

Surviving website snapshots show that after risk had already become publicly severe in July 2020, Yooli’s “material events” page still displayed all seven categories as “none” in archived versions from September 2020, December 2020, and March 2021. The audit-information page also continued mainly to display 2018 audit and compliance materials.

That **does not by itself establish a legal disclosure violation**, because Yooli may have provided information through the app, internal messages, offline communications, or regulatory reporting channels.

The evidence needed is therefore regulator-side material:

- inspection, meeting, risk-warning, and rectification documents from 2019–2021;
- Yooli’s major-operating-risk reports and their submission dates;
- monthly underlying-overdue, compensation, and balance data reported to regulators and the National Internet Finance Association;
- the time lag between those data and what ordinary users actually saw on the website, app, and internal-message system.

Related analysis:

- [Post-2020 Risk Exposure: Disclosure-Page Lag and Material-Event Questions](./2020-disclosure-lag-and-material-event-questions.md)

## What is most missing now?

If the next stage of evidence gathering can be compressed into one sentence, it is this:

> **Connect the numbers visible outside the platform with what actually happened to each underlying loan.**

The most valuable materials are underlying-loan repayment cash flows, first delinquency dates, extension and restructuring agreements, guarantee and compensation details, collection records, internal risk-classification changes, and original IDs or full ledgers capable of identifying unique claims.

Once even part of that chain is available, many issues that are currently only significant questions can be converted into specific time facts: what the platform knew, what it disclosed, and what ordinary lenders could not see.

---

This checklist should continue to narrow as evidence improves. Questions that become resolved can be removed and genuinely new questions added. The objective is not to make the list longer, but to make the investigation progressively more specific.