# Project Phoenix
## The Agentic Greenfield Pipeline for Legacy Modernization

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18904231.svg)](https://doi.org/10.5281/zenodo.18904231)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![GitHub](https://img.shields.io/badge/GitHub-semanticintent%2Fproject--phoenix-blue)](https://github.com/semanticintent/project-phoenix)

**Don't translate legacy code. Extract the intent. Rebuild from zero.**

> *"The code is not the asset. The business rules are the asset."*

---

## Abstract

**Project Phoenix** is a seven-agent agentic pipeline that transforms legacy systems into modern, greenfield applications. Instead of translating old code line-by-line, Phoenix extracts the business logic -- the rules, workflows, and intent buried inside decades of legacy code -- and rebuilds from zero.

The name comes from the mythological bird (Bennu, ~1500 BCE) that burns itself to ash and is reborn. The old system dies. The knowledge lives.

Legacy modernization has been stuck for decades because the industry confused the implementation with the intent. AI changes the equation -- not by translating old code, but by understanding what the code was trying to do, then building it fresh.

**Author:** Michael Shatny
**ORCID:** [0009-0006-2011-3258](https://orcid.org/0009-0006-2011-3258)
**Date:** March 2026
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
**Website:** [phoenix.cormorantforaging.dev](https://phoenix.cormorantforaging.dev)

---

## The Old Model vs. The New Model

| | Traditional Migration | Phoenix Pipeline |
|---|---|---|
| **Approach** | Translate COBOL -> Java | Extract intent -> Build fresh |
| **Technical Debt** | Carried forward | Zero |
| **Timeline** | 18-36 months | 3-6 months |
| **Team** | 200+ consultants | Small team + agent fleet |
| **Cost** | $50M-$500M | Orders of magnitude less |
| **Failure Rate** | 70% stall or fail | Validated at every gate |

---

## The Seven-Agent Pipeline

```
[A-00] Signal Extraction --> [A-01] Extractor --> [A-02] Archaeologist --> [A-03] Synthesizer
                                                                                  |
[A-06] Validator <-- [A-05] Builder <-- [A-04] Architect <---------------------+
```

| Agent | Role | Output |
|-------|------|--------|
| **A-00 Signal Extraction** | Project Context -> Mission Brief | Signal .sil files, mission brief |
| **A-01 Business Logic Extractor** | Source Code -> Business Requirements | Rules catalog, workflow maps, edge cases |
| **A-02 Interface Archaeologist** | UI/UX -> User Intent Model | Screen inventory, journey maps, role matrix |
| **A-03 Requirements Synthesizer** | Logic + Interface -> Unified Spec | Single source of truth, gap analysis |
| **A-04 Solution Architect** | Requirements -> Stack & Blueprint | Tech stack, API contracts, build plan |
| **A-05 Builder Fleet** | Blueprint -> Working Software | Production codebase, CI/CD, documentation |
| **A-06 Validator & Certifier** | New System <-> Original Requirements | Regression proof, coverage report |

Each agent is detailed in [PIPELINE.md](PIPELINE.md).

All agents read and write `.sil` artifact files — structured, human-readable documents in [EMBER format](https://github.com/semanticintent/phoenix-runtime). The artifact trail is the audit log.

**Reference implementation:** [`@semanticintent/phoenix-runtime`](https://www.npmjs.com/package/@semanticintent/phoenix-runtime) — orchestrates the pipeline, manages `.sil` state, enforces human gates.

---

## The Human Layer

Agents execute. Humans decide.

At every stage, the AI Software Lead validates outputs, resolves ambiguities, interviews stakeholders, and makes the judgment calls that no agent can:

- **Stakeholder interviews** -- capturing tribal knowledge
- **Ambiguity resolution** -- deciding what undocumented behavior means
- **Business sign-off** -- confirming agent outputs match reality
- **Go/no-go decisions** -- human gates between pipeline stages

The human layer is not optional. It is the difference between automation and transformation.

Details in [HUMAN-LAYER.md](HUMAN-LAYER.md).

---

## The Phoenix Metaphor

The Phoenix myth (Bennu bird, Egypt, ~1500 BCE) is not about preservation. It is about deliberate destruction followed by intentional rebirth:

1. **The fire is voluntary** -- the Phoenix chooses to burn. In software: the deliberate decision to stop maintaining the old system.
2. **The ashes carry the essence** -- not the feathers or the nest, but the identity. In software: the business rules survive, the code does not.
3. **The rebirth is complete** -- no hybrid Phoenix. A greenfield build, not a migration.

Full origin story in [ORIGIN.md](ORIGIN.md).

---

## Cormorant Stack Integration

Phoenix is the terminal layer of the Cormorant Foraging stack:

```
     Cormorant Foraging
    (The Moon -- 3D Foundation)
   /         |         \
Sound     Space      Time
(Chirp)   (Perch)    (Wake)
   \         |         /
    \        |        /
     +-------+-------+
     |   Layer 1     |
     |   DRIFT       |    Measure the gap
     |  (See Gap)    |
     +-------+-------+
             |
     +-------+-------+
     |   Layer 2     |
     |   Fetch       |    Decide to act
     |  (Close Gap)  |
     +-------+-------+
             |
     +-------+-------+
     |   Layer inf   |
     |   GESA        |    Learn across episodes
     |  (Learn Why)  |
     +-------+-------+
             |
     +-------+-------+
     |   Phoenix     |
     |  (Rebirth)    |    Transform the system
     +---------------+
```

Phoenix is invoked when the DRIFT is so extreme that no incremental action can close it -- when the system itself is the problem. You don't optimize a burning building. You let it burn, preserve what matters, and rebuild.

---

## Two Faces of Phoenix

Phoenix exists in two forms:

### Face One: The Standalone Methodology
**[semanticintent.dev/phoenix](https://semanticintent.dev/phoenix)**

Phoenix as a self-contained legacy modernization methodology. No framework dependencies. No prerequisite knowledge. A CTO, consulting partner, or developer can read it cold and understand the entire proposition in five minutes.

### Face Two: The Integrated Framework Layer
**[phoenix.cormorantforaging.dev](https://phoenix.cormorantforaging.dev)**

Phoenix as the terminal layer of the Cormorant Foraging stack. Full architectural integration showing how 3D sensing, DRIFT measurement, Fetch scoring, and GESA learning all feed into the Phoenix decision.

Same Phoenix. Same six agents. Same thesis. Two doors into the same room.

---

## Economics

| | Traditional Migration | Phoenix Pipeline |
|---|---|---|
| **Timeline** | 18-36 months | 3-6 months |
| **Team size** | 200+ consultants | Small team + agent fleet |
| **Budget** | $50M-$500M | Orders of magnitude less |
| **Failure rate** | 70% stall or fail | Validated at every gate |
| **Technical debt** | Carried forward | Zero |
| **Architecture** | Modern wrapper around legacy complexity | Built for the next decade |

Details in [ECONOMICS.md](ECONOMICS.md).

---

## Repository Structure

```
project-phoenix/
+-- README.md                 # This file - framework overview
+-- PIPELINE.md               # The six agents in detail
+-- HUMAN-LAYER.md            # The human decision layer
+-- ORIGIN.md                 # The Phoenix myth and metaphor
+-- ECONOMICS.md              # Cost and timeline analysis
+-- CITATION.cff              # Machine-readable citation metadata
+-- CHANGELOG.md              # Version history
+-- CONTRIBUTING.md           # How to contribute
+-- ARCHIVING.md              # Zenodo archiving guide
+-- LICENSE                   # CC BY 4.0 license
```

---

## Connection to Ecosystem

Project Phoenix is the transformation layer of the Semantic Intent ecosystem:

```
Semantic Intent (Philosophy)
  |
Cormorant Foraging (3D Framework) -- DOI: 10.5281/zenodo.18210081
  +-- PACE Pattern              -- DOI: 10.5281/zenodo.18049371
  +-- 6D Methodology            -- DOI: 10.5281/zenodo.18209946
  +-- DRIFT, Fetch (Action Layers)
  |
Project Phoenix (Transformation) <-- You are here
```

**Related Projects:**
- [Cormorant Foraging Framework](https://github.com/semanticintent/cormorant-foraging-framework)
- [6D Foraging Methodology](https://github.com/semanticintent/6d-foraging-methodology)
- [PACE Pattern](https://github.com/semanticintent/pace-pattern)
- [Semantic Intent SSOT](https://semanticintent.dev/papers/semantic-intent-ssot)
- [Case Study: UC-024 -- The Obsolescence Cascade](https://uc-024.stratiqx.com)

---

## Citation

If you use or reference Project Phoenix in your work, please cite:

### APA Style

Shatny, M. (2026). Project Phoenix: The Agentic Greenfield Pipeline for Legacy Modernization. Zenodo. https://doi.org/10.5281/zenodo.18904231

### BibTeX

```bibtex
@misc{shatny2026phoenix,
  author = {Shatny, Michael},
  title = {Project Phoenix: The Agentic Greenfield Pipeline for Legacy Modernization},
  year = {2026},
  publisher = {Zenodo},
  url = {https://github.com/semanticintent/project-phoenix},
  doi = {10.5281/zenodo.18904231},
  note = {ORCID: 0009-0006-2011-3258}
}
```

---

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** -- copy and redistribute in any medium or format
- **Adapt** -- remix, transform, and build upon for any purpose

Under the following terms:
- **Attribution** -- You must give appropriate credit, provide a link to the license, and indicate if changes were made.

---

## Author

**Michael Shatny**
ORCID: [0009-0006-2011-3258](https://orcid.org/0009-0006-2011-3258)

---

*"You don't migrate a Phoenix. It burns and rises."*
