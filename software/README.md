# Planned accounting software

**Status:** Proposed brief, October 17, 2026. No B.C.A. application, prototype, or release exists. No implementation or scaffold is authorized by this review.

**Proposed purpose:** general-purpose open-source tools that help anyone keep private books and publish deliberate, useful summaries. The team could be the first user. This is public software work, not a funded bookkeeping service reserved for members. Do not list it as an existing project in the SPI inquiry or grant applications. The [funding plan](../funding/README.md) should fund demonstrable public work; a future software request needs its own scope and evidence.

**Team-supplied context, October 17, 2026:** the team teaches by building in public, reports that a Lightning node has launched, plans Bitcoin donations, and intends to hold its treasury in bitcoin. These statements supply a use case, not reconciled balances, a live donation-channel confirmation, or evidence that this accounting software exists. **Proposed:** support Bitcoin-denominated treasury records alongside fiat expense valuation, with public synthetic teaching examples. Keep channel principal, routing fees, donations, and custody transfers distinct.

## Where it should live

**Proposed:** keep public financial records and this brief here; begin software in a separate public repository when the team authorizes implementation and chooses its license. Cross-link the two. No repository is being created or moved now.

| Structure | Advantage | Cost / risk |
| --- | --- | --- |
| Records and code together | One place to find formats and try the team's reporting workflow; fewer repositories. | Code issues and CI can overwhelm money/policy review. Contributors may mistake organizational records for fixtures. Path-specific review and CI rules would be needed. |
| Records here; software separate | Code releases, CI, security reports, and contributor traffic have their own workflow. Funding and policy decisions stay visibly separate. | Needs links and versioned format documentation to prevent drift. Separation alone does not prevent financial-data leaks. **Recommended.** |

If the team later chooses one repository, separate code from records, run code CI only on synthetic fixtures, and require the [decision process](../governance/decisions.md) for policy or money changes even when bundled with a code PR. Never run public CI against real books.

## Proposed ignore-rule change, deferred

The current [`.gitignore`](../.gitignore) has unanchored `private/`, `receipts/`, and `invoices/` patterns, which match directories at any depth; `.env.*` also matches `.env.example`. That could hide future source or synthetic-fixture directories. Git's [pattern rules](https://git-scm.com/docs/gitignore) confirm this behavior (checked October 17, 2026).

If software starts **in this repository**, propose replacing those directory patterns with root-anchored rules, keeping the secret-file protections, and adding the example exception after the environment exclusions:

```gitignore
/private/
/receipts/
/invoices/
.env
.env.*
!.env.example
*.key
*.pem
.DS_Store
```

**Proposed handling rule:** confidential files stay outside this checkout or, for local worksheets, only under root `private/`. The root `receipts/` and `invoices/` exclusions remain legacy safeguards, not recommended storage locations. Any tracked `.env.example` must contain placeholders only. Review already-tracked files separately: ignoring does not untrack them. Before changing patterns, inspect newly visible paths for private material. **Do not apply this change now**; it waits for implementation here or a separate explicit decision. Ignore rules are not access control.

## Reuse before building

Official project documentation, license files, and GitHub maintenance evidence below were checked **October 17, 2026**. This is a source survey, not a tested compatibility or security assessment. “SAT” below means a user-defined commodity for satoshis, not automatic wallet integration. Privacy describes where data can be processed; it is not a no-telemetry audit of every dependency or plugin.

| Tool / format | License | Currency / Bitcoin fit | Privacy model | Maintenance evidence and sources |
| --- | --- | --- | --- | --- |
| Beancount | GPL-2.0-only | Multi-currency double-entry text; named commodities can represent BTC or SAT, with explicit costs/prices. No native Lightning reconciliation inferred. | Local text files and CLI; keep optional importers and price fetchers under review. | [Project/license](https://github.com/beancount/beancount), [syntax](https://beancount.github.io/docs/beancount_language_syntax/); latest default-branch [commit checked](https://github.com/beancount/beancount/commit/9747213802acb733ce53acc6e963f5961f47d6cd): Aug 23, 2026. |
| Fava | MIT; its Beancount dependency keeps its own license | Browser reports and editing for Beancount, inheriting its currency model. | Runs against local books, with a localhost web interface; exposing it requires a separate access-control design. | [Project/license and local usage](https://github.com/beancount/fava); [commit checked](https://github.com/beancount/fava/commit/fa7be27ffcd4f8b75e07b2af7dcccbe9edd1c298): Oct 7, 2026. |
| beangulp / beanquery | Each GPL-2.0-only | Beancount statement-import framework / SQL-like ledger queries; currency handling depends on ledger and importer mappings. | Local Python tooling; an importer or extension can introduce external access. | [beangulp metadata](https://raw.githubusercontent.com/beancount/beangulp/master/pyproject.toml), [beanquery metadata](https://raw.githubusercontent.com/beancount/beanquery/master/pyproject.toml); latest commits checked [May 30](https://github.com/beancount/beangulp/commit/d5672c9dbb317842e0f24f1ed7f4b57fa53fa1c6) / [Jun 11, 2026](https://github.com/beancount/beanquery/commit/62b6abba7f560e2d5e1dce231b55571b84fdf31f). |
| hledger; journal / CSV | GPL-3.0-or-later | Multi-currency double entry, configurable commodities including BTC/SAT, CSV import/export, CLI/TUI/web reports. Related to Ledger format; not identical to every Ledger or Beancount construct. | Local journal and tools; web mode introduces a server surface. | [Project/license/features](https://github.com/hledgerorg/hledger); stable [1.52.4](https://github.com/hledgerorg/hledger/releases/tag/1.52.4), Sep 10, 2026; [install page](https://hledger.org/install.html) also lists 2.0 previews. |
| Ledger; journal format | BSD-3-Clause | Arbitrary commodities and prices can represent fiat, BTC, and SAT; flexible command-line reports. | Local text files; external quote commands are an optional integration to assess. | [License](https://raw.githubusercontent.com/ledger/ledger/main/LICENSE.md), [manual](https://ledger-cli.org/doc/ledger3.html); latest [commit checked](https://github.com/ledger/ledger/commit/faecd27cec670e128018dd92c8490a5b23f55660): Sep 22, 2026. |
| Core Lightning bookkeeper | MIT-style project license; `ccan/` modules have separate licenses | Node income/expense events in millisatoshis and coin identifiers; CSV export. Useful for routing and fees; not a general fiat ledger. | Bookkeeper runs with the node. Exports include sensitive identifiers/descriptions and must remain private. | [License](https://raw.githubusercontent.com/ElementsProject/lightning/master/LICENSE), [income RPC](https://docs.corelightning.org/reference/bkpr-listincome), [CSV RPC](https://docs.corelightning.org/reference/bkpr-dumpincomecsv); [v26.06.9](https://github.com/ElementsProject/lightning/releases/tag/v26.06.9), Oct 7, 2026. |
| BTCPay Server reporting | MIT | On-chain wallet/payment reports and invoice exports include payment currencies, rates, and fees; supports Bitcoin/Lightning payment workflows. Reports are inputs to books, not a complete organizational ledger. | Self-hosted; a chosen third-party host and connected rate/payment services change the privacy boundary. | [Project/license](https://github.com/btcpayserver/btcpayserver), [reports](https://docs.btcpayserver.org/Reporting/), [invoice export](https://docs.btcpayserver.org/Users/invoices/); [v2.4.5](https://github.com/btcpayserver/btcpayserver/releases/tag/v2.4.5), Oct 6, 2026. |
| btc-accounting | MIT | Bitcoin Core or phoenixd CSV to CAMT.053 statements, with fiat conversion and optional gain/loss calculations. An interoperability lead to evaluate, not a validated tax solution. | Local CLI, but some workflows query mempool.space and Kraken; review modes before giving it private wallet data. | [Project/license and network behavior](https://github.com/Sjors/btc-accounting); latest [commit checked](https://github.com/Sjors/btc-accounting/commit/9d75ac88f7d6a5c735c73873f8f07ffde3bc6d98): Jul 5, 2026. No latest GitHub release returned by the release endpoint; maturity needs further evaluation. |

Commit and release dates are evidence of activity, not promises of continued maintenance. No tool was installed, run against financial records, or connected to a wallet for this review. No complete LND accounting adapter was validated. Recheck versions, licensing of included components, and node-export completeness before implementation.

## Smallest useful gap to prove

**Proposed:** first try hledger's existing CSV import and reports with a synthetic version of our workflow. Compare Beancount plus Fava if a browser review screen is needed. Use the existing engines for balancing and arithmetic. Prefer file interoperability initially; do not copy or link GPL code into a package labeled solely 0BSD without evaluating the resulting license obligations. The [licensing brief](../governance/licensing.md) governs that decision.

Only build an adapter or report formatter if the trial exposes a specific missing step: a local, reviewable path from private expense/payment exports to reconciled project totals and a sanitized monthly Markdown report. First check whether an upstream mapping or contribution solves it. A new accounting engine, wallet, payment processor, or tax-filing system is not justified by this survey.

The team's first workflow could be:

1. Import the privately completed [cost worksheet](../finance/budget.md#line-item-worksheet) as planning data, keeping **Estimate** separate from documented costs incurred and payments made. Record confirmed tool-access savings in a cost-relief memo; personal awards are not automatically contributions to the team or treasury receipts. Any noncash contribution recognition needs a separate assessment under the applicable reporting framework.
2. Match expense records, approvals, project allocation, and private source exports by stable internal reference. Separate donations, routing fees, custody transfers, reimbursements, and commitments; repeated exports must not duplicate entries. Review fees, failed/pending payments, and node balances explicitly.
3. Generate only the allowlisted aggregate fields in the [monthly report](../templates/monthly-report.md), retaining unknowns and unresolved differences. Reconcile before a human reviews and publishes; publication and approval are never automatic. If a fiscal host supplies the ledger, import its records and produce only the supplement described in the [expense policy](../governance/expense-policy.md).

## Proposed privacy and release requirements

Keep each person's books separate from the organization's. Use local-first storage, no telemetry by default, optional network access disclosed before use, and backups under the user's control. Reporting must work without uploading books to an AI service. The accounting tool should consume exports or narrowly scoped read access, never require spending keys or permission to move money. Keep full identifiers and source records private; public output should be an explicit allowlist, with a preview and human review.

Use decimal or integer monetary representations with explicit units and conversion provenance. Preserve millisatoshi precision where the source supplies it; never silently relabel sats as BTC or treat movements between our own accounts as donations. Keep management-report valuations separate from tax basis and retain source records for later classification. All examples, tests, CI artifacts, screenshots, and issue reproductions must be synthetic. Once code exists, establish and document a private security-reporting route before a public release; do not invent a contact or claim one is monitored now.

**Proposed shipping disclaimer:** “Banana Certified” is a joke, not a professional accounting certification. No professional certification is claimed. This software is not tax, legal, or financial advice.
