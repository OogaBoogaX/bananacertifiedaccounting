# Project expense policy

**Status:** proposed, for team and prospective-sponsor review. **Not adopted.**

**Prepared:** October 17, 2026.

**Adoption:** none recorded. To adopt, record the team's decision (and any sponsor review) in the [decision log](decisions.md).

This proposal describes how project funds could be managed. It does not authorize spending, appoint anyone, or promise reimbursement. If a sponsor is accepted, its agreement and expense rules govern the funds it holds, and they override this policy where the two differ.

Before the first report, identify whose assets, transactions and obligations are being reported. Wallet access, custody, legal ownership and authority to spend are separate questions. Keep the supporting ledger and account records private, with a traceable connection to each public aggregate. The proposed public report is a management report; formal accounting and tax treatment depend on the legal holder, jurisdiction and applicable reporting requirements.

## Purpose and scope

Initially, funds would support documented expenses for approved public projects, mainly AI development tools. The following are outside this initial expense-only proposal:

- salaries and contractor compensation;
- unrestricted contributor allowances;
- distribution of surplus funds.

Future paid work would need a separate decision and appropriate agreements.

## Principles

- **Project purpose.** Every cost supports identified public project work.
- **Approval before commitment.** No one commits funds, or a sponsor, without approval.
- **Evidence.** Every payment has a receipt or invoice and an approval record.
- **No self-approval.** No one approves a claim or purchase that benefits them.
- **Open summaries, private records.** Totals are public. Invoices and personal details are not.

## Roles to fill

- **Project liaison (if a sponsor is adopted):** communicates with the sponsor and maintains the agreed project scope and budget.
- **Records coordinator:** keeps invoices, approvals, and payment records in restricted storage, and prepares public summaries.
- **Expense reviewer:** checks project purpose, available funds, and supporting records. The reviewer must be someone other than the person who benefits from the expense.

These are proposed responsibilities, not appointments. One person may hold more than one administrative role, provided independent review is preserved and the sponsor permits it. No approval limits or review counts have been adopted. The [Proposed decision process](decisions.md#proposed-decision-process) suggests a review rule for money and commitments; it does not authorize expenses today.

## Spending process

1. **Request.** Describe the project purpose, provider, expected amount, currency, and any recurring commitment or renewal date.
2. **Approve.** Get approval under the agreed budget and, for sponsor-held funds, the sponsor's rules before committing funds. Record who approved it, when, and for how much. No one may sign or accept contracts on a sponsor's behalf without its authorization.
3. **Buy.** Prefer project-specific billing. For mixed personal and project use, follow the allocation rules in the [budget](../finance/budget.md#shared-and-mixed-use-costs).
4. **Document.** Keep the evidence listed below.
5. **Pay or reimburse.** Use the approved channel only: payment from a team-controlled project fund, sponsor payment, or reimbursement. No such arrangement is established by this proposal.
6. **Record and reconcile.** Record invoices, obligations, approvals and payments separately. Mark a payment as paid only with settlement evidence; keep incurred unpaid costs visible even when approval is missing or disputed. Reconcile records before publishing totals.

## Documentation

For each expense, keep in restricted storage:

- an itemized invoice or receipt showing vendor, date, amount, and currency;
- for usage-based charges, the provider's usage export or statement for the period;
- the project share and how it was estimated, for mixed-use costs;
- the approval record;
- the payment or reimbursement confirmation;
- if currencies differ, the amount actually charged in the payment currency, or the rate and source used for conversion.

Give each expense a public reference ID, for example `BCA-2026-11-01` (year, month, sequence). Public reports can then cite the ID instead of private details.

## Reimbursement

- Submit a claim with the documentation above through the approved channel. The time limit for claims is **not yet set**.
- A reviewer may approve a claim in full, approve only the documented project share, or decline it with a reason.
- Do not assume that earlier personal costs will be reimbursed by the team or a future sponsor. Check any existing agreements and claims; new discretionary reimbursement needs approval, and payment from sponsor-held funds needs the sponsor's agreement. Absence of internal approval is not proof that no obligation exists.
- A reimbursement repays approved, documented project costs; it is not a general allowance. Its tax treatment depends on the recipient and applicable rules and is not determined by this policy.

## Recurring and variable costs

- Agree on a monthly budget, and on usage limits, before funding recurring services. Use provider spending caps or alerts where they are available.
- Costs above the agreed limits need additional approval before they are incurred, or as soon as possible if they could not be foreseen. Report them either way.
- Where providers allow it, more than one authorized person should be able to manage or cancel a project-billed account, so a subscription is not stranded if someone becomes unavailable. Account credentials never go in this repository.
- Review renewals before they occur, and cancel services that are no longer needed.
- Unspent funds remain subject to ownership, donor restrictions and existing obligations. An account balance is not automatically available to spend. Do not distribute a surplus to contributors under this expense-only proposal.

## Conflicts of interest

A conflict exists when a person involved in approving or reviewing an expense could personally benefit beyond the project purpose. Examples:

- approving one's own reimbursement;
- choosing a vendor that employs the person or in which they have a financial interest;
- payments to a family member or close associate.

When a conflict exists, the person discloses it, does not take part in the approval, and the record notes the disclosure. If no unconflicted reviewer is available, defer the expense, or ask the sponsor how to proceed.

## Exceptions

Exceptions to this policy should be rare. Each one needs:

- a written reason;
- approval by an unconflicted reviewer;
- a note in the next monthly report.

The team cannot waive a sponsor's rules. Ask the sponsor instead.

## Refunds, credits, and corrections

- Refunds and credits attributable to a project-funded payment must be traced back to the same fund. A provider credit is not a cash refund. Record how it was applied and avoid counting the original cost and its reversal twice.
- Correct a material published error promptly with a dated correction identifying the affected report and figures. Preserve the original version and explanation, carry the correction into the next report, and do not silently rewrite past reports or leave readers relying on a known error until month end.

## Reporting

Publish aggregate monthly receipts, payments, holdings, unpaid obligations and completed work using the [monthly report template](../templates/monthly-report.md). Show reporting-currency valuations separately from asset quantities, and support any spendable-funds estimate with restrictions and obligations. Do not use treasury receipts/payments as a substitute for an income statement. Donor identities, original receipts, tax forms, banking details, credentials, and private correspondence stay outside this repository.

## Proposed Bitcoin and Lightning receipts and treasury rules

The team reported on October 17, 2026 that its Lightning node has launched, bitcoin donations will be accepted, and its treasury will be held in bitcoin. Those are team-supplied facts and direction, recorded in the [funding plan](../funding/README.md#existing-donation-features). The following controls remain **Proposed**; no custody appointment, balance, receipt, conversion, or spending approval is implied.

- **Custody before collection.** Record the legal owner of each fund, authorized operators, recovery arrangements, and an independent records reviewer privately before publishing donation instructions. Keep project funds distinguishable from personal funds and sponsor-held funds. Store keys, backups, wallet addresses, node identifiers, and account access outside this public repository. Select controls the actual wallet/node supports; do not assume Lightning funds can use the same approval mechanism as an on-chain wallet. Separate approval to spend from technical ability to spend.
- **Confirm receipts.** Record settled amounts as Received; a generated invoice, pledge, or game event is not settlement evidence. Keep native amounts, settlement times, restrictions or refund conditions, source references, fees and supporting records privately. Classify supporter contributions, routing fees, loans, repayable advances and transfers separately. Reconcile node/payment-system records against treasury holdings; the activity feed is not the accounting ledger. Establish whether earlier test payments were real funds, refunds or synthetic events before setting an opening balance.
- **Bitcoin treasury.** Reconcile native quantities separately from reporting-currency valuations, with a stated price source and timestamp. Receipt-date values and period-end values serve different purposes; neither automatically establishes tax basis or an adopted accounting carrying value. Preserve acquisition, transfer and disposal history for the accountant. Show management valuations as estimates and price movements separately from receipts. Identify restrictions, liabilities and inaccessible funds before estimating what can be spent.
- **Conversion and payment.** Holding the treasury in bitcoin does not authorize a sale or exchange. Before an approved payment, document the payment currency, any conversion, operator authorization, units, rate source, fees and actual proceeds. Record both asset movements without treating conversion proceeds as a second donation. Recordkeeping must also support assessment of gains, losses and other tax effects; paying a vendor directly in bitcoin does not remove that need. Confirm a future sponsor's accepted methods and ownership boundary in writing.
- **Public reporting.** Publish period totals for receipts by type, payments, fees and holdings, with units and measurement methods. Separate funding placed in a node from routing fees, and identify whether that funding is a contribution, loan or transfer. Keep donor identities and transaction-level identifiers private; combine small categories when necessary to avoid identifying a donor. Report conditions and restrictions without revealing private details.
- **Giving language.** Do not represent direct support as eligible for a U.S. charitable contribution deduction or issue charitable tax receipts; no qualifying charitable recipient has been established for this channel. A factual acknowledgement of funds received is different from certifying deductibility. Other jurisdictions, business deductions and recipient tax treatment require their own assessment ([IRS charitable-contribution guidance](https://www.irs.gov/taxtopics/tc506), checked October 17, 2026). Calling a payment a donation does not establish that it is tax-free to its recipient. A future sponsor's authorized channel would need separate terms.

The proposed transaction records follow the information needs described in [IRS digital-asset guidance](https://www.irs.gov/filing/digital-assets), checked October 17, 2026: units, transaction dates, values and basis evidence matter for U.S. tax reporting. This source does not establish that any particular team member or fund is a U.S. taxpayer. Determine the holder and applicable jurisdiction before choosing accounting or tax treatment.

### Open questions on node funds and routing income

- Who legally owns and controls the node, on-chain funds, channel balances, and backups? Are any funds personal, borrowed, restricted, or owed back to someone?
- What is the reconciled opening balance, including any earlier real test gifts, refunds, and fees? What date separates testing from supporter donations?
- Which local channel balances belong to the treasury, and which funds are unavailable? Do not treat total channel capacity or remote liquidity as treasury assets.
- Has the node earned routing fees? If so, how are routing revenue, rebalancing costs, chain fees, and other operating costs reconciled separately from donations and contributed channel capital?
- Which legal/accounting arrangements govern custody, conversions, and any routing activity? What donor acknowledgement, record retention, and reporting requirements apply?

The public-source evidence for these distinctions is [Banana Pay Server's architecture](https://github.com/OogaBoogaX/bananapayserver/blob/965bfc0b966642ff261cffc5b4e8a15ac15fe830/docs/architecture.md) and [Lightning Foundry's economics documentation](https://github.com/OogaBoogaX/lightningfoundry/blob/bd9e67f6659bff89c0a13a977f8c64e1313d12e2/docs/economics.md), inspected October 17, 2026. They describe software and intended records; they do not establish actual balances or ownership.

## Proposed simplification if a fiscal host is adopted

Use a host's ledger, claim submission, approvals, and receipts as the source of truth for funds it holds. Retain this document only for team-specific project allocation, conflicts, spending proposals, and the boundary with independently held bitcoin. Replace duplicate claim/reimbursement instructions with links to the signed host terms after adoption. Keep private copies or exports needed for continuity, and reconcile transfers between the host and any separate treasury. Do not remove this policy or treat a host as selected before a recorded decision.

## Review

Review this policy when a sponsor is accepted, when project scope changes, when paid development is proposed, or after the first three months of actual reporting.
