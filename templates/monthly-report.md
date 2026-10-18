# Monthly treasury and project report — YYYY-MM

**Status:** Proposed template. No actual financial figures are included.

## How to use this template

1. Copy this file to `reports/YYYY-MM.md` and identify the reporting scope below before filling it in. Keep the supporting transaction ledger and original records private.
2. Use reconciled records. **Unknown is not zero.** State any missing records or unresolved differences.
3. In a month with no activity, say there were no receipts or payments and still report opening and closing holdings. Say no funds were held only if the records establish that separately.
4. Have someone other than the preparer check the report. “Internally reviewed” means that check, not an independent accountant's review or audit.
5. Complete the checklist, then remove these instructions and the checklist from the published copy.

This is a voluntary management report of treasury movements, costs and project work, not a complete set of financial statements. It does not select a financial-reporting framework or determine tax treatment. Confirm the reporting owner and applicable requirements before preparing formal accounts or tax filings.

**Proposed host-based simplification:** if a fiscal host is adopted, link its ledger/report for funds it holds and publish only outcomes, planning comparisons, unresolved items and separate treasury reconciliation here. Do not combine host-held and independently held funds without explaining ownership and scope, or count transfers as new donations.

---

**Report status:** Draft / Internally reviewed / Published (choose one)

**Reporting period and cutoff timezone:** YYYY-MM-01 to YYYY-MM-DD; —

**Reporting scope:** whose funds and transactions are included; separate team, personal and host-held funds. Identify legal holders by an appropriate public description or private reference, without publishing account details. If ownership is unresolved, state that limitation.

**Assets and custody locations included:** — [use public reference IDs, not wallet or account identifiers]

**Method:** settled receipts and payments, reconciled by asset and custody location; unpaid obligations and planning estimates shown separately. Specify how pending settlements, channel funds and any scope changes are handled.

**Reporting currency for valuations, price source and timestamps:** —

**Sources / reconciliation date:** —

**Prepared by / internally checked by:** public handles or roles

## Summary

- **Reconciled closing holdings:** — [quantities and units by asset; valuation separately]
- **External receipts / payments this month:** — [by asset; exclude internal transfers and show exchanges separately]
- **Unpaid obligations:** — [amounts and currencies; identify disputed or uncertain claims]
- **Estimated amount available for new spending:** — [supported by the availability calculation below, or Unknown]
- **Open items:** — [see Unresolved items]

## Project outcomes

What the work and expenditure produced. Link to public evidence, including teaching and contributor support where available.

| Project | Work delivered | Public evidence | Who benefits | Related payment references |
| --- | --- | --- | --- | --- |
| — | — | — | — | — |

## Treasury reconciliation by asset

Repeat this table for **each asset and unit**, such as BTC or USD, within the defined ownership and reporting scope. Reconcile custody locations privately and then aggregate without counting a balance twice. Do not include total channel capacity or remote liquidity as owned funds. Disclose pending or inaccessible amounts separately.

**Asset / unit / scope:** —

| Line | Movement or balance | Native amount |
| --- | --- | ---: |
| A | Opening balance | — |
| B | + External receipts, excluding asset exchanges and transfers within scope | — |
| C | − External payments, excluding fees, asset exchanges and transfers within scope | — |
| D | − Fees paid | — |
| E | + Asset exchange inflows | — |
| F | − Asset exchange outflows | — |
| G | + Signed net transfers between custody locations within scope | — |
| H | + Signed, documented corrections | — |
| I | **Calculated closing balance: A + B − C − D + E − F + G + H** | — |
| J | Closing balance independently checked against custody records | — |
| K | **Unreconciled difference: J − I** | — |

Enter B–F as nonnegative amounts; the formula applies their addition or subtraction. Only G and H carry their own signs. Classify each movement once. Where evidence supports gross amounts, report gross receipts/payments and fees separately; do not subtract a fee again from a net amount. If the fee split is unavailable, state the net presentation and missing detail. Do not invent an allocation.

Exchanges have two asset movements: a bitcoin sale reduces BTC on F and increases fiat on E in the respective tables. Its proceeds are not a second donation. Transfers on G net to zero across the same ownership scope and asset once both sides settle; related fees remain on D. A transfer to another legal owner is not automatically internal. Pending transfers need a cutoff explanation.

Line H must identify each correction and its evidence; it is not a balancing figure. Explain any nonzero K and do not describe the affected balance as reconciled. Opening balances must agree to the previous report or show a documented correction and its effect. Keep unresolved differences visible across periods.

**Corrections, settlement timing and differences:** —

## Valuation and availability

Keep quantities separate from their value in the reporting currency. For each asset, **indicative closing value = closing quantity × stated price per unit**. A change in market price is not a receipt and does not enter the native-unit reconciliation. These values are management estimates, not adopted accounting carrying values, tax basis or guaranteed sale proceeds.

| Asset / fund | Reconciled closing quantity and unit | Price per unit, source and time | Indicative reporting-currency value |
| --- | ---: | --- | ---: |
| — | — | — | — |

**Amount available for new spending — Estimate or Unknown:** —

Support this amount with a private schedule of donor restrictions, amounts owed or held for others, incurred unpaid obligations, approved future commitments, and funds that cannot currently be used. Distinguish unrestricted holdings from spendable funds. Count overlapping exclusions only once: an unpaid invoice already included as a commitment must not be deducted again. Do not disregard an incurred obligation because internal approval is missing. Disclose disputed or uncertain claims. If obligations are in fiat and holdings in bitcoin, state the conversion assumption and expected fees; do not subtract unlike units or imply a fixed fiat amount is secured.

## External receipt detail

Reconcile these totals to B for each asset. “Donation” describes the support received here; it does not determine tax or financial-statement classification. Loans, repayable advances and other financing must not be labeled donation income. A pledge or award notice alone is not a receipt; amounts actually received under conditions belong in the reconciliation with their conditions and any potential repayment obligation disclosed.

| Receipt type | Native amount and unit | Restrictions / conditions | Evidence reference |
| --- | ---: | --- | --- |
| Supporter donations received | — | — | — |
| Grants received | — | — | — |
| Routing fees received | — | — | — |
| Other external receipts, identified separately by nature | — | — | — |

Publish aggregates only. Keep donor identities, full transaction identifiers, invoices and account details private. Combine small categories if needed to avoid identifying a donor.

## Payments by category and project

Reconcile payments to C and D for each asset. Identify loan repayments, asset purchases, refunds and operating costs separately; a payment is not necessarily an expense for the same period. Exchanges and internal transfers remain in their own reconciliation lines.

| Payment category | Project | Native amount paid and unit | Transaction-date reporting value and basis, if used | Purpose / public reference |
| --- | --- | ---: | --- | --- |
| — | — | — | — | — |

## Budget compared with actual

Use the same period, currency, scope and measurement on both sides. Compare a payment forecast with Actual paid, or a service-period cost estimate with supported Actual incurred. Explain timing differences, including prepaid annual subscriptions. A monthly planning allocation is not an actual monthly payment. Label a budget Approved only if the [decision log](../governance/decisions.md) supports that label; otherwise use Estimate.

| Category / period / measurement | Budget (Approved / Estimate) | Actual paid or incurred, explicitly identified | Variance: Actual − Budget | Explanation |
| --- | ---: | ---: | ---: | --- |
| — | — | — | — | — |

A positive variance means spending/cost above the comparison amount. Missing actuals remain Unknown, not zero.

## Unpaid obligations and future costs

Keep incurred obligations, unapproved claims and possible renewals distinct. Approval is an internal control, not the sole evidence of whether an amount is owed. Count an obligation once in the availability calculation.

| Item | Nature: incurred / approved future commitment / proposed / disputed | Amount and currency | Due / decision date | Approval and evidence status |
| --- | --- | ---: | --- | --- |
| — | — | — | — | — |

**Incoming support pledged but not received:** — [amount, conditions and evidence if known; no donor identities]. Keep this separate from outgoing obligations and do not include it in funds available to spend.

## Costs paid personally by volunteers (memo)

List supported project-related costs paid personally and not reimbursed, separating voluntary contributions from reimbursement claims and unresolved arrangements. Personal payment does not automatically establish a team reimbursement obligation, and missing internal approval does not prove no obligation exists. Check agreements and supporting records. Avoid counting the same cost twice if it later appears as a team reimbursement.

| Category / service period | Project share and currency | Basis: Estimate / Actual invoiced / Actual paid | Claim or contribution status; amount reimbursed to date |
| --- | ---: | --- | --- |
| — | — | — | — |

## In-kind access and credits (memo)

List the usable award period, expiry and supported spending displaced under the [budget's planning method](../finance/budget.md#proposed-savings-and-spending-controls). Pending applications reduce nothing. Free access does not enter the treasury movement table. Do not count advertised retail value as money received, subtract a credit twice, or assume an individual's benefit is a contribution to the team. Any formal noncash contribution recognition needs separate assessment under the applicable reporting framework.

## Unresolved items

| Item | Open since | Effect on reported figures | Next action / responsible role |
| --- | --- | --- | --- |
| — | — | — | — |

## Exceptions and corrections

- Policy exceptions and approval evidence: —
- Corrections to earlier reports, with the affected period and amounts: —
- Changes in reporting scope, measurement or valuation method: —

---

## Before publishing (delete from the published copy)

- [ ] Reporting owner, period, cutoff and scope are clear; personal and host-held funds are not silently combined.
- [ ] Each asset's calculated closing balance agrees to custody evidence, or the difference is disclosed; no balancing entries hide gaps.
- [ ] Transfers, exchanges, fees, donations and payments are counted once; prior-period balances and corrections are traceable.
- [ ] Valuations are separate from asset quantities and receipts; spendable amounts account for restrictions, obligations and access limits without duplicate deductions.
- [ ] Invoices, payments, service-period costs, forecasts and approvals are distinguished; variance signs and comparison periods are explicit.
- [ ] No donor identities, private financial documents, credentials or account/wallet identifiers are disclosed.
- [ ] Public links support the outcomes described; another person checked the report, with no professional assurance implied.
