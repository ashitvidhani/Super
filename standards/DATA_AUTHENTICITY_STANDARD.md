# Data Authenticity Standard

The Data Authenticity Standard applies to all Super projects that use financial, economic, market, industrial, AI, simulation, or user-uploaded data.

The purpose is to make every data-driven project honest, reproducible, legally safer, and externally understandable.

---

## Core Principle

Authentic data first. Expensive data later.

A project can be serious even without institutional licensed data, but it must clearly disclose what kind of data is being used.

Never pretend that public, delayed, synthetic, self-logged, or user-uploaded data is the same as real-time licensed institutional data.

---

## Data Labels

Every dataset used in a serious Super project should be labeled clearly.

Recommended labels:

```text
OFFICIAL_PUBLIC
EXCHANGE_PUBLIC
COMPANY_REPORTED
REGULATORY_PUBLIC
GOVERNMENT_PUBLIC
CENTRAL_BANK_PUBLIC
USER_UPLOADED
SELF_LOGGED
DELAYED_EOD
LOW_COST_VENDOR
SYNTHETIC
SIMULATED
MANUALLY_CURATED
BROKER_API_PERMITTED
LICENSED_INSTITUTIONAL
UNKNOWN_OR_UNVERIFIED
```

---

## Meaning of Each Label

| Label | Meaning |
|---|---|
| `OFFICIAL_PUBLIC` | Public data from an official source |
| `EXCHANGE_PUBLIC` | Public data from an exchange or exchange-published source |
| `COMPANY_REPORTED` | Data from company filings, annual reports, quarterly reports, or announcements |
| `REGULATORY_PUBLIC` | Public regulatory filings or disclosures |
| `GOVERNMENT_PUBLIC` | Government-published datasets |
| `CENTRAL_BANK_PUBLIC` | Central-bank datasets such as RBI or Fed sources |
| `USER_UPLOADED` | Data uploaded by the user |
| `SELF_LOGGED` | Data manually logged over time by the project owner |
| `DELAYED_EOD` | Delayed or end-of-day data |
| `LOW_COST_VENDOR` | Data from a paid or free API/vendor with permitted use |
| `SYNTHETIC` | Artificially generated data |
| `SIMULATED` | Data produced by a simulator |
| `MANUALLY_CURATED` | Manually assembled dataset |
| `BROKER_API_PERMITTED` | Data from broker/API access where permitted by terms |
| `LICENSED_INSTITUTIONAL` | Professional licensed data with commercial or institutional permissions |
| `UNKNOWN_OR_UNVERIFIED` | Data whose source or rights are not clearly verified |

---

## Required Disclosure

Every serious data-driven project should disclose:

- Data source
- Data label
- Data frequency
- Time range
- Whether it is real, delayed, synthetic, or user-provided
- Known limitations
- Usage rights or uncertainty around usage rights
- Whether redistribution is allowed
- Whether it is suitable for production use

Example:

| Dataset | Source | Label | Frequency | Limitation |
|---|---|---|---|---|
| US macro data | FRED | `OFFICIAL_PUBLIC` | Monthly / quarterly | Revisions possible |
| Company filings | SEC EDGAR | `REGULATORY_PUBLIC` | Event-based | Parsing complexity |
| Backtest prices | User CSV | `USER_UPLOADED` | Daily | User responsible for quality |
| Order book replay | Generated simulator | `SYNTHETIC` | Event-based | Not real exchange data |

---

## Legal and Licensing Rule

Do not build serious projects on data that is legally unclear, scraped without permission, or restricted from reuse.

For public proof-of-work projects:

Prefer:

- Official public data
- Regulatory filings
- Government datasets
- Central-bank datasets
- User-uploaded data
- Synthetic simulation data
- Clearly permitted APIs
- Low-cost vendors with clear terms

Avoid:

- Unlicensed redistribution
- Unofficial scraping as a foundation
- Hidden data sources
- Terms-of-service violations
- Pretending restricted data is freely usable
- Using convenience APIs as if they are institutional-grade sources

---

## Public vs Commercial Use

A dataset may be acceptable for:

```text
personal learning
research prototype
educational demo
```

but not acceptable for:

```text
commercial product
redistribution
paid client reports
institutional deployment
```

Projects should clearly separate:

- Learning use
- Research use
- Personal use
- Public GitHub demo use
- Commercial use
- Institutional use

---

## India Data Standard

For India-focused systems, prefer:

- NSE/BSE public reports where permitted
- Exchange filings
- Corporate announcements
- Annual reports
- Quarterly reports
- Investor presentations
- RBI DBIE and RBI publications
- SEBI public disclosures
- Government datasets
- Public macroeconomic datasets
- User-uploaded data
- Self-logged data
- Low-cost/legal vendor APIs where permitted

Be careful with:

- Scraped exchange data
- Unclear vendor rights
- Redistribution of market data
- Real-time data claims
- Options/tick/order-book data without proper license

---

## US Data Standard

For US-focused systems, prefer:

- SEC EDGAR filings
- SEC XBRL company facts
- FRED / ALFRED macro data
- Official government datasets
- Company filings
- Public annual and quarterly reports
- Low-cost vendors where terms allow
- User-uploaded data
- Self-logged data

Be careful with:

- Free APIs with unclear commercial rights
- Unofficial market-data scraping
- Redistribution restrictions
- Real-time data claims without license

---

## HFT / Microstructure Data Standard

For HFT and market microstructure projects, Stage 1 should usually use:

- Synthetic limit order book data
- Simulated order flow
- Generated replay files
- Public sample datasets if legally usable
- User-provided replay data if rights are clear

Clearly state:

```text
This simulation does not use licensed real exchange tick/order-book data.
```

Later institutional versions may require:

- Licensed tick data
- Licensed order-book data
- Exchange data agreements
- Redistribution permissions
- Professional market-data vendor contracts

---

## Data Quality Checks

Where relevant, projects should check:

- Missing values
- Duplicate rows
- Invalid timestamps
- Timezone consistency
- Currency consistency
- Unit consistency
- Outliers
- Corporate-action adjustment
- Split/dividend handling
- Schema correctness
- Stale data
- Unexpected gaps
- Survivorship bias
- Lookahead bias
- Revision history where relevant

---

## Point-in-Time Discipline

For backtesting, quant research, macro research, and financial intelligence systems, avoid using future information accidentally.

Projects should consider:

- When data became available
- Filing date vs report period date
- Revision date
- Announcement date
- Ex-dividend date
- Split date
- Index membership date
- Strategy decision timestamp

The project should not use information that would not have been known at the decision time.

---

## Data Versioning

Serious systems should eventually track:

- Data snapshot date
- Source version
- File hash where useful
- Ingestion timestamp
- Cleaning version
- Schema version
- Code version
- Output version

This supports reproducibility.

---

## User-Uploaded Data Rule

If a project accepts user-uploaded data, it should state:

- User is responsible for data accuracy
- User is responsible for usage rights
- Project validates structure but cannot guarantee truth
- Outputs depend on uploaded data quality

---

## Synthetic Data Rule

Synthetic data is allowed and useful, especially for:

- HFT simulation
- Order-book replay
- Stress testing
- Monte Carlo systems
- Scenario analysis
- Early prototypes
- Educational systems

But it must be clearly labeled.

Example:

```text
This result is based on synthetic simulated order flow and should not be interpreted as real exchange behavior.
```

---

## Data Source Table Template

Every serious data-driven project should include a table like this:

| Data | Source | Label | Rights / Usage | Limitation |
|---|---|---|---|---|
|  |  |  |  |  |

---

## Limitations Template

Every serious data-driven project should include a limitations section.

Example:

```text
Limitations:

- Uses public or delayed data, not licensed institutional real-time feeds.
- Does not redistribute commercial market data.
- Some datasets may contain revisions.
- Backtest results may be affected by survivorship bias if the universe is incomplete.
- Synthetic simulations are not equivalent to real exchange order-book data.
- Outputs are for research and educational purposes, not investment advice.
```

---

## Upgrade Path

Projects should clearly state what improves if upgraded to licensed or institutional data.

Examples:

- Real-time market feeds
- Tick-level history
- Order-book depth
- Historical options chains
- Professional corporate actions
- Survivorship-complete databases
- Institutional news feeds
- Analyst estimates
- Redistribution rights
- Commercial data-vendor contracts

---

## Final Rule

A serious Super project should never hide its data quality.

If the data is public, say public.  
If it is delayed, say delayed.  
If it is synthetic, say synthetic.  
If it is user-uploaded, say user-uploaded.  
If it is licensed, say licensed.

Trust comes from honesty, not pretending.