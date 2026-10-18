# Project expense budget

**Status:** planning estimate. **Not approved**, not a spending allowance, and not an accounting ledger.

**Estimate supplied by the team:** October 17, 2026. It is not itemized from invoices.

**Planning currency:** USD, to confirm before a formal application.

This file is the authoritative source for budget figures in this repository. Other documents should link here rather than restate the details.

## Current estimate

The team estimates project-related AI costs at **$2,500–$5,000 per month**. This is a rough planning range, not a forecast cap. The figure covers the team as a whole; it is not a per-contributor allowance.

| Planning view | Amount | Meaning |
| --- | ---: | --- |
| Lower end of stated monthly range | $2,500 | Not an established minimum operating cost |
| Upper end of stated monthly range | $5,000 | Not an approved cap or guaranteed maximum |
| Annualized range | $30,000–$60,000 | Monthly range × 12; not a twelve-month forecast |

What the estimate does **not** include or establish:

- No donation revenue, grant award, opening balance, or expense transaction is recorded here.
- Sponsor fees, payment fees, hosting, domains, and other project costs are not included.
- It is not yet known whether API usage and compute are inside the range or would come on top of it.
- Costs volunteers currently pay personally do not automatically become debts of a future sponsor or organization.

Annualization arithmetic: $2,500 × 12 = $30,000 and $5,000 × 12 = $60,000. This expresses the scale of the estimate; it does not establish twelve months of committed costs.

## Allow for payment and conversion costs

The current range excludes payment, conversion and node-operation costs. Itemize those separately before setting a fundraising target. Keep liquidity placed in channels distinct from operating costs: moving existing treasury bitcoin into a channel is not by itself an expense. Record associated fees separately and establish the ownership and availability of node funds under the [treasury proposal](../governance/expense-policy.md#proposed-bitcoin-and-lightning-receipts-and-treasury-rules).

SPI is deferred. Any future host fee belongs in a separate scenario based on confirmed terms, not in the present operating estimate. For a single percentage fee charged on gross receipts, the planning formula is **gross receipts needed = net expense requirement ÷ (1 − fee rate)**, before other charges. Do not assume multiple fees have the same charging base or treat a bitcoin valuation as guaranteed fiat proceeds.

## Cost types

| Category | Typical pattern | In the current estimate? | Notes |
| --- | --- | --- | --- |
| AI subscriptions | Recurring, fixed per plan or seat | Yes | May be personal plans also used for project work |
| AI API usage | Recurring, varies with usage | To confirm | A likely source of month-to-month variation |
| Related compute | Varies; may be occasional | To confirm | For example, cloud instances for testing |
| Hosting and domains | Recurring | No | Not yet estimated |
| Other occasional costs | One-off | No | Approve individually under the [expense policy](../governance/expense-policy.md) |

## Shared and mixed-use costs

**Proposed allocation rules; not adopted.**

Allocate costs in this order of preference:

1. **Project-specific billing.** A plan or API key used only for project work, billed separately. Allocate its documented cost to that work; allocation does not itself approve reimbursement or establish sponsor eligibility.
2. **Documented project share.** A plan used for both personal and project work. Charge only a reasonable project share, and record how it was estimated (usage logs, a time estimate, or similar). Never charge the full personal bill automatically.
3. **Organization-wide tools.** Tools that serve several projects. Divide the cost by a stated method, and count each subscription once, not once per project.

If money is restricted to one project, charge it only that project's attributable share.

## Supporting the estimate with records

1. Gather two or three recent months of invoices and usage exports in restricted storage, not in this repository.
2. For each cost, record the fields in the worksheet below, and use a public reference ID instead of account details.
3. Check for overlapping plans, and for the same subscription counted by more than one person or project.
4. Separate observed costs for completed service periods from forecasts and from payment timing. Label historical figures **Actual invoiced/incurred** or **Actual paid**, with the period and evidence. A monthly average or allocation used for future planning remains an **Estimate**.
5. Publish only category/project summaries here with an "updated" date, and keep the completed line-item worksheet and evidence private.
6. Propose an initial budget from the itemized figures. It becomes approved only when the decision is recorded in the [decision log](../governance/decisions.md).

### Line-item worksheet

| Ref | Category | Provider / plan | Cost pattern | Projects | Monthly amount | Basis | Project share | Status |
| --- | --- | --- | --- | --- | ---: | --- | --- | --- |
| — | AI subscriptions | To confirm | Recurring, fixed | To confirm | Not itemized | — | To confirm | Not approved |
| — | AI API usage | To confirm | Usage-based | To confirm | Not itemized | — | To confirm | Not approved |
| — | Related compute | To confirm | To confirm | To confirm | Not itemized | — | To confirm | Not approved |
| — | Hosting, domains, other | To scope | To confirm | To confirm | Not estimated | — | To confirm | Not approved |

*Monthly amount* is a planning amount before project allocation. *Basis* identifies the estimate method and supporting historical service/payment periods, if any. An annual subscription divided by 12 is a monthly planning allocation, not twelve monthly payments. This is a blank schema, not a request to publish line items. Copy the [private worksheet template](../templates/ai-cost-worksheet.md) under `private/` before filling it in. Keep billing-account owners, invoices, and reimbursement details out of public summaries.

## Proposed savings and spending controls

Record awarded free access or credits in an **in-kind cost-relief memo** and reduce the estimate only for spending they actually displace. Until awarded and usable, a benefit is Potential and reduces nothing. Keep the recipient, applicable project share, start/end dates and restrictions privately; publish only the period and supported savings. An individual's free plan is not automatically a contribution received by a team entity. This memo is a planning treatment, not a conclusion about recognition of noncash contributions or tax treatment, which depends on the recipient, terms and applicable reporting rules. Do not count advertised retail value as a receipt or subtract a benefit twice from a bill already shown net of credits.

For each period: **revised estimated cash need = itemized estimated project cost − confirmed eligible cost displaced**, with the reduction limited to the cost actually avoided. Expiry restores the uncovered cost unless another decision is made. The unitemized headline estimate above remains unchanged until the team supplies the underlying figures.

For usage-based accounts, choose a documented limit before use, check whether the provider's control is a hard cap or only an alert, and confirm which plans, projects, and taxes it covers. Assign an account steward and an independent reviewer before activation. Set alerts early enough to stop avoidable usage, review exports during the month, and record renewal/cancellation dates. A notification alone is not a spending stop. Verify the actual provider settings privately; no provider or control is assumed available here.

## Decisions needed

- Separate essential recurring costs from optional extra capacity.
- Decide which services should move to project-specific billing.
- Agree on the method for documenting the project share of mixed-use plans.
- Set an initial budget, a process for changing it, and who approves changes.
- Establish payment, conversion and node-operation costs before setting a fundraising target; include host fees only if a hosting route is later chosen.
- Decide what gets cut first when available funding is below the approved budget.

Report actual activity with the [monthly report template](../templates/monthly-report.md) once records exist.
