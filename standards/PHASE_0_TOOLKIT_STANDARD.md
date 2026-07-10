# Phase 0 Toolkit Standard

The Phase 0 Mathematics + Probability Simulation Toolkit is the baseline project quality standard for all serious projects in the Super ecosystem.

This standard was created after the Phase 0 capstone was upgraded from a working roadmap project into a professional open-source/package-grade repository.

The purpose of this standard is simple:

A project is not complete just because the code works.

A serious Super project should be understandable, testable, reproducible, documented, and externally reviewable.

---

## Baseline Principle

Every serious Super project should aim to be:

- Working
- Tested
- Documented
- Reproducible
- GitHub-ready
- Externally understandable
- Roadmap-linked
- Professionally structured

The goal is that another serious engineer, AI engineer, quant, finance professional, or systems developer can open the repository and understand:

- What the project does
- Why it exists
- How to install it
- How to run it
- How to test it
- What assumptions it makes
- How the code is structured
- How it connects to the larger Super ecosystem

---

## Minimum Standard for Serious Projects

A serious Super project should include the following where relevant.

### 1. Clean Repository Structure

The project should have a clear structure such as:

```text
project-name/
├── README.md
├── pyproject.toml or requirements.txt
├── src/ or package_name/
├── tests/
├── docs/
├── examples/
├── main.py or CLI entry point
├── CHANGELOG.md
├── LICENSE
└── .gitignore
```

The exact structure can change depending on the project type, but the repository should not be a loose collection of random scripts.

---

### 2. Professional README

The README should explain:

- Project purpose
- Roadmap context
- Features
- Installation steps
- How to run
- How to test
- Project structure
- Documentation links
- Current status
- Limitations where relevant
- Future integration role

The README should help an external reader understand the project without private explanation.

---

### 3. Dependency Setup

Use one of the following depending on project maturity:

- `pyproject.toml`
- `requirements.txt`
- `package.json`
- `Cargo.toml`
- `CMakeLists.txt`
- Other standard dependency/build files depending on language

For Python projects, prefer `pyproject.toml` when the project is package-grade.

---

### 4. Virtual Environment Support

For Python projects, include setup instructions such as:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -e ".[dev]"
```

The project should be reproducible on a clean machine.

---

### 5. Professional `.gitignore`

The repo should ignore:

- Virtual environments
- Cache files
- Build artifacts
- Coverage files
- IDE files
- OS files
- Temporary outputs
- Large generated files where appropriate

---

### 6. Tests

Every serious project should have tests where relevant.

For Python projects:

```bash
python -m pytest
```

Tests should cover:

- Normal cases
- Edge cases
- Invalid inputs
- Important calculations
- Core workflows

---

### 7. Edge-Case Testing

Projects should not only test happy paths.

Examples of edge cases:

- Empty inputs
- Invalid dimensions
- Negative values where invalid
- Zero values where invalid
- Boundary values
- Mismatched array lengths
- Numerical stability cases
- Missing data
- Wrong file format
- Bad configuration

---

### 8. Coverage Gate Where Useful

For package-style Python projects, use coverage where useful:

```bash
pytest --cov=package_name --cov-report=term-missing
```

A minimum coverage gate can be used where appropriate.

The Phase 0 toolkit used:

```text
80% minimum coverage gate
```

Coverage is not a replacement for good tests, but it helps prevent careless gaps.

---

### 9. GitHub Actions CI Where Useful

For serious projects, add GitHub Actions or equivalent CI.

CI should usually check:

- Installation
- Tests
- Coverage
- Basic linting where relevant
- Multi-version compatibility where useful

Example checks:

```text
push to main
pull request to main
run pytest
run coverage
```

---

### 10. Documentation Folder

A serious project should include a `docs/` folder where useful.

Possible documentation files:

```text
docs/
├── API_REFERENCE.md
├── ARCHITECTURE.md
├── FORMULA_SHEET.md
├── PROJECT_EXPLANATION.md
├── FUTURE_INTEGRATION_NOTES.md
└── LIMITATIONS.md
```

Not every project needs every file, but serious projects should not rely only on code comments.

---

### 11. API Reference Where Relevant

If the project exposes reusable functions, classes, or modules, add an API reference.

The API reference should explain:

- Function purpose
- Inputs
- Outputs
- Errors
- Example usage
- Notes or assumptions

---

### 12. Architecture Documentation

Every serious project should explain its architecture.

Architecture docs should cover:

- Folder structure
- Module responsibilities
- Data flow
- Dependency flow
- Entry points
- Testing structure
- Future integration role

---

### 13. Changelog

Add `CHANGELOG.md` for serious projects.

It should track:

- Initial release
- Major features
- Refactors
- Bug fixes
- Documentation upgrades
- Professionalization passes

---

### 14. License

Add a license where public/open-source sharing is intended.

For most learning and open-source proof-of-work projects, MIT License is acceptable unless another license is intentionally chosen.

---

### 15. Examples and Demos

Add runnable examples where useful.

Examples help users understand:

- How to call functions
- How modules work together
- What outputs look like
- How the project connects to real use cases

Examples may live in:

```text
examples/
```

or inside a CLI/demo runner.

---

### 16. Main Entry Point or CLI

Where relevant, add:

```text
main.py
```

or a proper CLI.

The entry point should let someone quickly run the project without reading the entire codebase.

Example:

```bash
python main.py
python main.py --demo probability
python main.py --demo portfolio
```

---

### 17. Final Verification Before Locking

Before a project is considered locked, verify:

```bash
git status
python -m pytest
pytest --cov=package_name --cov-report=term-missing
python main.py
```

The exact commands vary by project, but the principle is:

Do not lock a serious project until it has been tested, documented, committed, pushed, and verified.

---

## Tier Rules

### Tier 3 Learning Projects

Minimum expectation:

- Clean repo
- README
- Examples where useful
- Tests where useful
- GitHub-ready structure

Tier 3 projects do not always need full CI, coverage, API docs, or architecture docs unless they become portfolio projects.

---

### Tier 2 Supporting Projects

Tier 2 projects should follow the Phase 0 Toolkit Standard unless intentionally marked experimental.

Expected:

- Good README
- Clean structure
- Tests
- Documentation
- Examples
- Changelog
- License where public
- CI where useful
- Architecture notes where useful

---

### Tier 1 Flagship Projects

Tier 1 projects must exceed the Phase 0 Toolkit Standard.

In addition to the baseline standard, they should include:

- Real-world authenticity
- Data-source disclosure
- Adapter-based architecture
- Validation checks
- Reports
- Workflows
- Assumption tracking
- Limitations section
- Readiness gates
- Future licensed-data upgrade path where relevant
- Monitoring/logging where relevant
- User-facing outputs where relevant
- Expert-reviewable documentation

---

## What This Standard Prevents

This standard prevents projects from becoming:

- Loose scripts
- Unclear notebooks
- Untracked experiments
- Unexplained code dumps
- Unverified calculations
- Unreproducible demos
- Portfolio projects that outsiders cannot understand

---

## Final Rule

A serious Super project is not finished until it can answer:

Can another serious person open this repository and understand what it does, how it works, how to run it, how it is tested, what assumptions it makes, and how it connects to the larger system?

If the answer is no, the project is not finished yet.