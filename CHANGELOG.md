# Changelog

All notable changes to Project Phoenix will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.1.0] - 2026-03-31

### Added
- A-00 Signal Extraction as the new first pipeline stage — produces mission brief and signal `.sil` files before code analysis begins
- EMBER artifact format — all agents read and write `.sil` files as their canonical artifact format
- Reference to [`@semanticintent/phoenix-runtime`](https://www.npmjs.com/package/@semanticintent/phoenix-runtime) — the open-source npm package that orchestrates the pipeline

### Changed
- Pipeline updated from six agents to seven (A-00 through A-06)
- Agent numbering convention updated from 1–6 to A-00 through A-06 for consistency with the runtime implementation
- PIPELINE.md and README.md updated throughout to reflect the seven-agent structure

---

## [1.0.0] - 2026-03-07

### Added
- Initial public release of the Project Phoenix methodology
- Complete documentation of the six-agent pipeline:
  - Agent 1: Business Logic Extractor
  - Agent 2: Interface Archaeologist
  - Agent 3: Requirements Synthesizer
  - Agent 4: Solution Architect
  - Agent 5: Builder Fleet
  - Agent 6: Validator & Certifier
- Human Layer documentation (AI Software Lead role, gate model)
- Origin story (Phoenix myth, 1500 BCE Bennu bird through modern methodology)
- Economics analysis (traditional migration vs. Phoenix pipeline)
- Cormorant Stack integration documentation
- Two Faces strategy (standalone methodology + integrated framework layer)
- Citation metadata (CITATION.cff) with references to:
  - Cormorant Foraging Framework (DOI: 10.5281/zenodo.18210081)
  - 6D Foraging Methodology (DOI: 10.5281/zenodo.18209946)
  - PACE Pattern (DOI: 10.5281/zenodo.18049371)
- Creative Commons Attribution 4.0 International license

### Core Thesis
- "The code is not the asset. The business rules are the asset."
- Legacy modernization via intent extraction, not code translation
- Greenfield rebuild with zero inherited technical debt
- Human validation gates between every pipeline stage

### Documentation Structure
```
project-phoenix/
+-- README.md                 # Methodology overview
+-- PIPELINE.md               # The six agents in detail
+-- HUMAN-LAYER.md            # The human decision layer
+-- ORIGIN.md                 # The Phoenix myth and metaphor
+-- ECONOMICS.md              # Cost and timeline analysis
+-- CITATION.cff              # Machine-readable citation metadata
+-- CHANGELOG.md              # This file
+-- CONTRIBUTING.md           # Contribution guidelines
+-- ARCHIVING.md              # Zenodo archiving guide
+-- LICENSE                   # CC BY 4.0 license
```

---

## Future Releases

Future versions will be documented here as the methodology evolves through:
- Empirical validation from Phoenix engagements
- Refinements to agent specifications
- Community contributions and feedback
- Integration enhancements with Cormorant stack

Each significant update will receive a new version number and DOI on Zenodo.

---

*For the latest version, visit [phoenix.cormorantforaging.dev](https://phoenix.cormorantforaging.dev)*
