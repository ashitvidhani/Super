# Global Market-Pack Architecture and Cross-Jurisdiction Financial Intelligence Overlay

Overlay code: **GMP**  
Roadmap version: **Super Roadmap v1.1 — Global Market-Pack Architecture Overlay**  
Status: **Implemented in ledger; activation remains prerequisite-gated**

## Purpose

Teach reusable global financial-market architecture once, then implement jurisdictions through typed contracts, adapters, schemas, configuration, mappings, source registries and effective-dated rules. This does not create a separate full curriculum for each country.

## Count Allocation

- Full Spine / Specialization: +14
- Finance / Quant / HFT / Macro: +30
- Advanced AI / Agentic Finance: +6
- Total: +50

## Parent Placement Rules

- GMP-FS topics activate after API, database, data-engineering, distributed-systems and software-architecture foundations, but before major country-specific financial-platform implementations.
- GMP-FQ topics activate after the Financial Data Pipeline foundation and before or alongside the India + US Dashboard, Cross-Market Capital Growth Comparator, portfolio/risk engines, filing intelligence, macro intelligence and AI-native research systems.
- GMP-AI topics activate after RAG, document intelligence, NLP, retrieval evaluation and financial-agent foundations, but before autonomous multi-agent financial workflows.

---

## GMP-FS — Global Financial Data and Market Infrastructure

| ID | Topic | Exact parent module | Prerequisite placement |
|---|---|---|---|
| GMP-FS-01 | Country-pack interface and contract design | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After typed programming, API design, software architecture and interface-contract fundamentals. |
| GMP-FS-02 | Market adapter architecture and dependency injection | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-01 and dependency-injection, modularity and adapter-pattern foundations. |
| GMP-FS-03 | Pack registration, discovery and dynamic loading | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-01–02 and package/module loading, plugin architecture and configuration management. |
| GMP-FS-04 | Capability declarations, optional features and graceful fallback | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-01–03 and feature-flag, error-handling and resilience foundations. |
| GMP-FS-05 | Cross-market security and entity identifier architecture | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After database design, data modelling and identifier/key architecture; before instrument schemas. |
| GMP-FS-06 | Exchange, venue and instrument metadata schemas | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-05 and typed schema, relational/document database and validation foundations. |
| GMP-FS-07 | Corporate entity, security, listing and share-class relationship mapping | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-05–06 and graph/relational relationship modelling. |
| GMP-FS-08 | Global trading-calendar engine | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After date/time programming and GMP-FS-06 exchange metadata; before settlement/session computation. |
| GMP-FS-09 | Time-zone, UTC and daylight-saving normalization | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-08 and UTC/time-zone library fundamentals. |
| GMP-FS-10 | Settlement-cycle, business-day and market-session computation | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-08–09 and effective-dated rules/configuration design. |
| GMP-FS-11 | Data-source provenance, lineage and traceability | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After data-engineering pipelines, metadata, audit logging and reproducibility foundations. |
| GMP-FS-12 | Market-pack versioning and effective-date management | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-11 and schema/data versioning plus point-in-time data concepts. |
| GMP-FS-13 | Data entitlements, licensing metadata and access-control architecture | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-11–12 and authentication, authorization, secrets and policy fundamentals. |
| GMP-FS-14 | Country-pack contract testing, validation and compatibility testing | Layer 2 — Full Spine / Specialization → Global Financial Data and Market Infrastructure | After GMP-FS-01–13 and unit, integration, property-based and regression testing foundations. |

---

## GMP-FQ — Cross-Jurisdiction Financial Normalization and Market Intelligence

| ID | Topic | Exact parent module | Prerequisite placement |
|---|---|---|---|
| GMP-FQ-01 | Local GAAP, IFRS and US GAAP mapping principles | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After accounting and financial-statement foundations; after Financial Data Pipeline base ingestion. |
| GMP-FQ-02 | Financial-statement taxonomy normalization | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-01, filing ingestion and schema-mapping foundations. |
| GMP-FQ-03 | Fiscal-year, quarter and reporting-period normalization | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-02 and date/effective-period modelling. |
| GMP-FQ-04 | Reporting-unit and financial-statement currency normalization | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-02–03 and currency/unit conversion fundamentals. |
| GMP-FQ-05 | Restatements, amended filings and point-in-time handling | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FS-11–12 and GMP-FQ-02–04. |
| GMP-FQ-06 | Limits of cross-market accounting comparability | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-01–05; before cross-market valuation and AI comparison outputs. |
| GMP-FQ-07 | Base-currency and reporting-currency architecture | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After FX, returns and portfolio-accounting foundations; coordinated with GMP-FS-12. |
| GMP-FQ-08 | Hedged versus unhedged return calculations | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-07, FX returns and hedging-instrument basics. |
| GMP-FQ-09 | Inflation-adjusted cross-country return comparison | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-07 and inflation/index-number foundations. |
| GMP-FQ-10 | Local risk-free-rate proxy selection | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After fixed-income, rates and benchmark-selection foundations. |
| GMP-FQ-11 | Sovereign yield-curve normalization | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-10 and yield-curve construction/interpolation foundations. |
| GMP-FQ-12 | Purchasing-power and real-return interpretation | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-07–11 and macro/inflation foundations. |
| GMP-FQ-13 | Investor-residency assumption model | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After portfolio user-profile/assumption-registry design; before tax calculations. |
| GMP-FQ-14 | Dividend withholding-tax assumptions | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-13; implemented as time-versioned scenarios, not legal advice. |
| GMP-FQ-15 | Capital-gains and securities-transaction-tax assumptions | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-13; after transaction/PnL accounting basics. |
| GMP-FQ-16 | Brokerage, exchange fees, stamp duties and trading-cost models | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After market microstructure, backtesting-cost and execution-cost foundations. |
| GMP-FQ-17 | Capital controls, convertibility and repatriation constraints | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After FX, international markets and jurisdiction-risk foundations. |
| GMP-FQ-18 | Central-bank data-source adapters | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After Financial Data Pipeline adapters and GMP-FS-01–14; before normalized macro intelligence. |
| GMP-FQ-19 | National statistical-office and government-data adapters | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After Financial Data Pipeline adapters and GMP-FS-01–14. |
| GMP-FQ-20 | Local liquidity, credit and capital-flow indicators | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-18–19 and macro/liquidity indicator foundations. |
| GMP-FQ-21 | Cross-country macro-regime normalization | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-09–12 and GMP-FQ-18–20. |
| GMP-FQ-22 | Cross-market valuation comparison | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-01–12 and valuation/factor foundations; before comparator/dashboard implementation. |
| GMP-FQ-23 | Accounting-quality, disclosure-quality and governance adjustments | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-01–06 and governance/forensic-accounting foundations. |
| GMP-FQ-24 | Sovereign, political and jurisdiction-risk integration | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After sovereign-risk, macro and scenario-analysis foundations. |
| GMP-FQ-25 | Liquidity-adjusted market comparison | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After market microstructure, liquidity metrics and GMP-FQ-16. |
| GMP-FQ-26 | Currency-aware portfolio attribution | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-07–12 and portfolio attribution foundations. |
| GMP-FQ-27 | Cross-market portfolio constraints and allocation rules | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-13–17, GMP-FQ-24–26 and portfolio optimization foundations. |
| GMP-FQ-28 | Research, analysis and regulated investment-advice boundaries | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After financial research workflow and compliance fundamentals; before external product outputs. |
| GMP-FQ-29 | Jurisdiction-aware data-use and redistribution restrictions | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FS-11–13 and data-licensing fundamentals. |
| GMP-FQ-30 | Time-versioned compliance assumptions, disclosures and audit records | Layer 3 — Finance / Quant / HFT / Macro → Cross-Jurisdiction Financial Normalization and Market Intelligence | After GMP-FQ-28–29, GMP-FS-12–13 and audit-log/versioning foundations. |

---

## GMP-AI — Jurisdiction-Aware Financial AI

| ID | Topic | Exact parent module | Prerequisite placement |
|---|---|---|---|
| GMP-AI-01 | Multilingual financial-document ingestion | Layer 4 — Advanced AI / Agentic Finance → Jurisdiction-Aware Financial AI | After NLP, OCR/document parsing, embeddings and financial-document ingestion foundations. |
| GMP-AI-02 | Local financial terminology and entity resolution | Layer 4 — Advanced AI / Agentic Finance → Jurisdiction-Aware Financial AI | After GMP-AI-01, named-entity recognition and GMP-FS-05–07. |
| GMP-AI-03 | Jurisdiction-aware source routing | Layer 4 — Advanced AI / Agentic Finance → Jurisdiction-Aware Financial AI | After RAG/tool-routing foundations, GMP-FS-03–04 and GMP-FQ-18–19. |
| GMP-AI-04 | Country-pack-aware retrieval, reasoning and tool selection | Layer 4 — Advanced AI / Agentic Finance → Jurisdiction-Aware Financial AI | After GMP-AI-01–03, RAG evaluation and agent-tool orchestration. |
| GMP-AI-05 | Compliance-constrained agent outputs | Layer 4 — Advanced AI / Agentic Finance → Jurisdiction-Aware Financial AI | After GMP-FQ-28–30 and AI safety/output-policy foundations. |
| GMP-AI-06 | Citation, audit and jurisdiction-level reasoning traceability | Layer 4 — Advanced AI / Agentic Finance → Jurisdiction-Aware Financial AI | After GMP-AI-01–05, provenance/citation evaluation and GMP-FS-11–13. |

---

## Dependency Map

### Module dependencies

1. **GMP-FS** depends on typed programming, APIs, databases, data engineering, distributed systems, authentication/authorization, testing and software architecture.
2. **GMP-FQ** depends on the Financial Data Pipeline base, GMP-FS contracts/metadata/versioning, accounting, FX, fixed income, macro, portfolio, valuation, market microstructure and compliance foundations.
3. **GMP-AI** depends on RAG, NLP, document intelligence, entity resolution, agent routing/evaluation, GMP-FS provenance/contracts and GMP-FQ compliance/normalization.

### Project dependencies

| Project | Activation gate | Primary topic dependencies |
|---|---|---|
| GMP-P01 | After GMP-FS architecture foundations are taught | GMP-FS-01–07, GMP-FS-11–14 |
| GMP-P02 | After calendar/time/rates/cost foundations | GMP-FS-08–13; GMP-FQ-07–17; GMP-FQ-18–21 |
| GMP-P03 | After P01 and P02 are stable and the Financial Data Pipeline base exists | GMP-FS-01–14; GMP-FQ-01–30; India and US official/public adapters |
| GMP-P04 | Only after P03 proves India–US extensibility | P01–P03 plus one limited GCC or Singapore configuration/adapter set |
| GMP-P05 | Built incrementally, final lock after P01–P04 and jurisdiction-aware AI | GMP-FS-14; GMP-FQ-28–30; GMP-AI-05–06; P01–P04 |

### Product activation sequence

1. Reusable pack architecture
2. India Pack
3. United States Pack
4. India–US normalization and comparison
5. One limited regional pilot
6. Production regional packs only when justified by users, pilots, partners, lawful data access and commercial demand

No GMP work interrupts Phase 1.

---

## Project Deliverables

### GMP-P01 — Country Pack SDK and Schema

Outputs: country-pack interface, adapter contracts, registry, capability declarations, typed schemas, version handling, sample-pack template, validators and new-jurisdiction documentation. Minimum Level 2; designed toward Level 3–4.

### GMP-P02 — Global Market Calendar and Normalization Engine

Outputs: exchange sessions, time-zone/DST normalization, holidays, settlement cycles, business-day calculations, currency conversion, inflation normalization, risk-free assumptions and tax/cost scenario engine. Minimum Level 2; designed toward Level 3–4.

### GMP-P03 — India–United States Reference Pack Implementation

Outputs: IndiaDataAdapter, USDataAdapter, exchange metadata, filing adapters, official macro adapters, calendars, FX/inflation comparison, accounting mappings, cross-market analytics and licensing/provenance disclosures. This is the first complete proof that the pack framework works. Minimum Level 2; designed toward Level 3–4.

### GMP-P04 — Limited Regional Pack Pilot

One deliberately limited GCC or Singapore pilot, implemented only after P03 is stable. It proves that a third jurisdiction can be added without rewriting the core. Minimum Level 2.

### GMP-P05 — Cross-Jurisdiction Validation, Governance and Compliance Test Suite

Outputs: schema-contract, point-in-time, calendar, currency, accounting, tax, lineage, licensing, disclosure, AI citation/source-routing and regression tests plus audit reports. Minimum Level 2; designed toward Level 3–4.

---

## Duplication and Conflict Audit

| Existing roadmap capability | Apparent overlap | Audit decision |
|---|---|---|
| Financial Data Pipeline timestamp normalization | GMP-FS-09 | Not a duplicate. Existing text is a project capability; GMP-FS-09 is the reusable cross-jurisdiction architecture and tested atomic learning topic. |
| Financial Data Pipeline audit trail/data versioning | GMP-FS-11–13 | Not a duplicate. GMP formalizes provenance, effective dating, entitlements and licensing metadata at country-pack level. |
| India + US Dashboard / Comparator currency and inflation comparison | GMP-FQ-07–12 | Not a duplicate. Existing projects consume the normalized methods; GMP teaches and implements the reusable engine. |
| Macro Dashboard RBI/Fed adapters | GMP-FQ-18–21 | Not a duplicate. The dashboard remains an application; GMP creates standardized local-source adapter contracts and cross-country normalization. |
| Stock X-Ray / filing reader financial-statement handling | GMP-FQ-01–06 | Not a duplicate. GMP supplies point-in-time taxonomy/accounting normalization across jurisdictions. |
| Sovereign Risk Dashboard | GMP-FQ-24 | Not a duplicate. The existing dashboard is an application; GMP-FQ-24 defines integration into cross-market valuation/allocation workflows. |
| Existing RAG, cited answers and AI Research Copilot | GMP-AI-01–06 | Not a duplicate. GMP adds multilingual, jurisdiction-aware routing, compliance constraints and jurisdiction-level traceability. |
| Existing India/US adapters | GMP-P01/P03 | No project replacement. P01 is the reusable SDK; P03 is the reference implementation; existing Financial Data Pipeline remains the data backbone. |
| Cross-Market Capital Growth Comparator | GMP-P02/P03 | No replacement. The comparator consumes the normalization/calendar/reference-pack services. |

**Deduplication result:** zero topic deletions, zero project deletions, zero identifier conflicts and zero phase-number conflicts. All 50 additions remain atomic because prior entries were broad capabilities or downstream applications, not equivalent reusable cross-jurisdiction topics.

---

## Deferred Non-Counted Backlog

### Regional Market Pack Product Expansion Backlog

- India — first full implementation
- United States — first full implementation
- GCC — deferred expansion
- United Kingdom — deferred expansion
- European Union / EEA — deferred expansion
- Japan — deferred expansion
- Singapore — deferred expansion
- Hong Kong — deferred expansion
- Other developed markets — future
- Other emerging markets — future

Country-specific holidays, rates, forms, exchange lists and tax percentages are normally versioned configuration/data, not separate roadmap topics.

---

## Institutional Teaching Standard for Every GMP Topic

1. Primitive reality and why the problem exists
2. Layman intuition
3. Financial-market and engineering context
4. Formal terminology and model
5. Architecture or mathematical representation
6. Real India example
7. Real United States example
8. Cross-jurisdiction contrast
9. Implementation design
10. Data structures, interfaces or formulas
11. Legal, licensing and compliance boundaries
12. Failure modes and edge cases
13. Point-in-time and versioning concerns
14. Testing and validation
15. Performance, scalability and reliability implications
16. Institutional workflow relevance
17. Common mistakes
18. Twisted interview or design questions
19. Practical implementation exercise
20. Project integration
21. Mastery test
22. Revision summary
23. Memory trigger
24. Weak-spot audit

Every topic must connect to code, data, platform architecture, analytics, governance or product implementation.

---

## Professional Project Standard

Every GMP project must include problem/user framing, functional and non-functional requirements, system/data architecture, contracts, source and assumption registries, licensing/provenance disclosure, effective-dated schemas, typed modular code, unit/integration/regression testing, property-based testing where useful, point-in-time correctness, benchmarks, performance budgets, security/secrets boundaries, RBAC where relevant, audit logs, observability, structured logging, metrics, recovery behaviour, CI/CD, reproducible environments, containerization where appropriate, API/developer/user documentation, ADRs, example datasets, explicit data labels, deployment/demo workflows, case studies, limitations, risk register, postmortem and licensed-data upgrade path.

---

## Maturity and Market Readiness

- All five projects: minimum Level 2.
- P01, P02, P03 and P05: designed toward Level 3–4.
- Level 5 cannot be claimed without licensed data, redistribution permission, commercial agreements, professional legal/compliance review, production security, operational support and real institutional deployment.
- Technical roadmap completion does not itself prove commercial approval. External validation, pilots, real users, security testing, reliability history and lawful data rights remain mandatory.

---

## Authentic Data Lock

**Authentic data first, expensive data later.** Explicitly distinguish official/real, delayed, EOD, self-logged, user-uploaded, vendor-permitted, synthetic and licensed institutional data. Never imply equivalence between public/retail data and institutional real-time licensed data.

---

## Execution Protection

Phase 1 remains 14/42 completed. Topic 15 — Source Transformation is next. The 15-phase sequence is unchanged and no GMP activation occurs inside the current electronics study sequence.
