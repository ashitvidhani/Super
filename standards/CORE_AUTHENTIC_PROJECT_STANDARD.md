# Core-Authentic Real-World Project Standard

The Core-Authentic Real-World Project Standard applies mainly to serious Tier 1 and selected Tier 2 projects in the Super ecosystem.

It extends the Phase 0 Toolkit Standard.

The Phase 0 Toolkit Standard makes a project clean, tested, documented, reproducible, and GitHub-ready.

The Core-Authentic Standard makes a project believable, useful, and serious enough for expert review in real-world domains such as finance, quant research, market intelligence, HFT simulation, AI research, macro analysis, and industrial intelligence.

---

## Core Principle

Build the core first. Licensed data scales the core later.

A project does not need expensive institutional data on day one to be serious.

But it must be honest about:

- What data it uses
- What the data can prove
- What the data cannot prove
- What assumptions are being made
- What is synthetic
- What is delayed
- What is public
- What is user-uploaded
- What is self-logged
- What would require licensed data later

The project should never pretend to be more institutional than it actually is.

---

## What Core-Authentic Means

A Core-Authentic project is not just a toy demo.

It should have:

- Real use case
- Clean architecture
- Legal data approach
- Data-source disclosure
- Reproducible pipeline
- Validation checks
- Clear assumptions
- Limitations section
- Useful output
- Professional documentation
- Future upgrade path

It should be serious enough that a domain expert can understand the logic and say:

This is not complete institutional infrastructure yet, but the core thinking and architecture are genuine.

---

## Required Components

A Core-Authentic project should include the following where relevant.

---

## 1. Real-World Use Case

The project should clearly answer:

- Who is this for?
- What problem does it solve?
- What decision does it support?
- What workflow does it improve?
- What would make it useful in practice?

Bad framing:

```text
This project analyzes stocks.
```

Better framing:

```text
This project helps compare India and US equities using valuation, fundamentals, risk, drawdown, currency, inflation, and macro regime assumptions.
```

---

## 2. Data-Source Disclosure

Every data-driven project should clearly disclose its data sources.

Examples:

- Official public datasets
- Exchange filings
- Annual reports
- Quarterly reports
- Corporate announcements
- SEC EDGAR
- FRED
- RBI public datasets
- User-uploaded CSV files
- Self-logged snapshots
- Synthetic simulation data
- Delayed/EOD data
- Low-cost vendor APIs
- Future licensed institutional feeds

Each source should be labeled honestly.

Example table:

| Source | Type | Use | Limitation |
|---|---|---|---|
| SEC EDGAR | Official public | US filings | Filing delay and parsing complexity |
| FRED | Official public | US macro data | Some series may revise over time |
| User CSV | User-uploaded | Portfolio or prices | User responsible for data quality |
| Synthetic LOB | Synthetic | HFT simulation | Not real exchange order-book data |

---

## 3. Data Authenticity Labels

Data should be labeled by type.

Recommended labels:

```text
OFFICIAL_PUBLIC
EXCHANGE_PUBLIC
COMPANY_REPORTED
USER_UPLOADED
SELF_LOGGED
DELAYED_EOD
LOW_COST_VENDOR
SYNTHETIC
SIMULATED
LICENSED_INSTITUTIONAL
UNKNOWN_OR_UNVERIFIED
```

A serious project should not mix these casually.

Example:

```text
This backtest uses delayed/EOD public data and is not an institutional tick-level execution backtest.
```

---

## 4. Adapter-Based Architecture

Data systems should use replaceable adapters wherever possible.

Example structure:

```text
data_adapters/
├── india_data_adapter.py
├── us_data_adapter.py
├── sec_edgar_adapter.py
├── fred_adapter.py
├── user_csv_adapter.py
├── synthetic_data_adapter.py
└── licensed_data_adapter_placeholder.py
```

The goal is to allow future upgrades without rewriting the entire system.

Bad design:

```text
Hard-code one data source everywhere.
```

Good design:

```text
Use adapter interfaces so public data, user-uploaded data, vendor data, and licensed data can be swapped later.
```

---

## 5. Validation Checks

A Core-Authentic project should include checks such as:

- Missing-value detection
- Duplicate detection
- Date/timestamp validation
- Schema validation
- Unit validation
- Currency validation
- Outlier checks
- Corporate-action adjustment checks
- Source reliability checks
- Data freshness checks
- Lookahead-bias checks where relevant
- Survivorship-bias checks where relevant

The exact checks depend on the project.

---

## 6. Assumption Tracking

Any serious analytics project should clearly list assumptions.

Examples:

- Transaction cost assumption
- Slippage assumption
- Tax assumption
- Currency conversion assumption
- Inflation adjustment assumption
- Risk-free rate assumption
- Data-frequency assumption
- Liquidity assumption
- Execution assumption
- Model confidence assumption

Assumptions should be visible in outputs or documentation.

---

## 7. Limitations Section

Every Core-Authentic project should clearly state limitations.

Examples:

- Uses EOD data, not tick data
- Uses public filings, not institutional feeds
- Does not include survivorship-complete universe yet
- Does not model taxes fully
- Does not model real order-book liquidity
- Does not include redistribution rights for commercial data
- Uses synthetic data for microstructure simulation
- Not investment advice
- Not production trading infrastructure

Limitations increase trust when written honestly.

---

## 8. Reproducible Outputs

The project should produce outputs that can be reproduced.

Examples:

- Reports
- CSV outputs
- JSON outputs
- Charts
- Logs
- Backtest summaries
- Risk summaries
- Simulation summaries
- Research notes

If results change, the project should make it clear why.

---

## 9. Audit Trail Where Relevant

For serious systems, keep track of:

- Input data source
- Run timestamp
- Config used
- Parameters used
- Output generated
- Errors/warnings
- Version of code or model
- Data snapshot date

This is especially important for finance, AI, backtesting, and research systems.

---

## 10. Professional Reports

Where relevant, outputs should be understandable by humans.

Examples:

- Markdown reports
- HTML reports
- PDF reports
- Dashboard summaries
- Backtest tear sheets
- Risk reports
- Data-quality reports
- Thesis reports
- Macro regime reports

A serious project should not only print raw arrays unless that is the correct technical output.

---

## 11. Workflow Orientation

A real project should support a workflow.

Examples:

Financial Data Pipeline:

```text
ingest → validate → clean → store → report → export
```

Backtesting Platform:

```text
load data → define strategy → run backtest → calculate risk → generate report → review assumptions
```

AI Research Copilot:

```text
upload document → parse → retrieve evidence → answer with citations → show confidence → log output
```

HFT Simulator:

```text
load event stream → replay order book → process strategy orders → match fills → calculate PnL → generate audit log
```

---

## 12. Readiness Levels

Core-Authentic projects should clearly indicate maturity.

Recommended maturity ladder:

| Level | Name | Meaning |
|---|---|---|
| Level 0 | Learning Project | Concept understood, simple implementation |
| Level 1 | Working Prototype | End-to-end demo on sample/public/synthetic data |
| Level 2 | Core-Authentic Research System | Legal data, validation, assumptions, reports, docs |
| Level 3 | Product-Grade Beta | UI/API, deployment, feedback, monitoring |
| Level 4 | Institutional-Ready System | Security, governance, audit logs, pilots |
| Level 5 | Licensed Institutional System | Licensed feeds, redistribution rights, commercial contracts |

Most serious Super projects should initially target Level 2.

Selected flagship projects can later move toward Level 3 or Level 4.

---

## 13. Future Licensed-Data Upgrade Path

For finance and market systems, clearly state what licensed data would improve.

Examples:

- Real-time exchange feeds
- Tick/order-book data
- Historical options data
- Professional news feeds
- Corporate actions database
- Survivorship-complete equities database
- Institutional estimates
- Redistribution rights
- Vendor contracts

A project can be serious without these on day one, but it should know where they fit.

---

## 14. Compliance Boundaries

Finance and market-related systems should include disclaimers such as:

- Educational and research use
- Not investment advice
- No guarantee of accuracy
- Data limitations apply
- Not suitable for live trading without further validation
- Licensing restrictions may apply
- User responsible for external data rights

This protects the project and improves professionalism.

---

## 15. Expert-Reviewability

A Core-Authentic project should be understandable by a serious reviewer.

A reviewer should be able to inspect:

- README
- Architecture docs
- Data source notes
- Assumptions
- Limitations
- Tests
- Examples
- Reports
- Code structure
- Future roadmap

If an expert cannot understand what the project does, it is not yet ready.

---

## Example: Core-Authentic vs Toy Project

Toy project:

```text
Downloads stock data and plots moving averages.
```

Core-Authentic project:

```text
Ingests legally permitted India/US market data through adapters, validates schema and missing values, tracks assumptions, runs strategy tests with transaction costs and benchmark comparison, generates reproducible reports, discloses data limitations, and documents the path to licensed data.
```

---

## Final Rule

A Core-Authentic project does not need to be institutionally complete on day one.

But it must be:

- Honest
- Structured
- Validated
- Useful
- Reproducible
- Documented
- Upgradeable

If the core is genuine, licensed data and institutional infrastructure can be added later.