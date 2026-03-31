# Project Phoenix
## The Agentic Greenfield Pipeline for Legacy Modernization

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18904231.svg)](https://doi.org/10.5281/zenodo.18904231)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Runtime](https://img.shields.io/badge/runtime-phoenix--runtime-orange)](https://github.com/semanticintent/phoenix-runtime)

**Don't translate legacy code. Extract the intent. Rebuild from zero.**

> *"The code is not the asset. The business rules are the asset."*

---

## Abstract

**Project Phoenix** is a seven-agent agentic pipeline that transforms legacy systems
into modern, greenfield applications. Instead of translating old code line-by-line,
Phoenix extracts the business logic — the rules, workflows, and intent buried inside
decades of legacy code — and rebuilds from zero.

The name comes from the mythological bird (Bennu, ~1500 BCE) that burns itself to
ash and is reborn. The old system dies. The knowledge lives.

**Author:** Michael Shatny
**ORCID:** [0009-0006-2011-3258](https://orcid.org/0009-0006-2011-3258)
**Date:** March 2026
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
**Website:** [semanticintent.ai](https://semanticintent.ai)

---

## The Old Model vs. The New Model

| | Traditional Migration | Phoenix Pipeline |
|---|---|---|
| **Approach** | Translate COBOL → Java | Extract intent → Build fresh |
| **Technical Debt** | Carried forward | Zero |
| **Timeline** | 18–36 months | 3–6 months |
| **Team** | 200+ consultants | Small team + agent fleet |
| **Cost** | $50M–$500M | Orders of magnitude less |
| **Failure Rate** | 70% stall or fail | Validated at every gate |

---

## The Seven-Agent Pipeline

```
A-00 Signal Extraction
  ↓
A-01 Business Logic Extractor → /workflows/*.sil
  ↓
A-02 UI Archaeologist → /screens/*.sil
  ↓
A-03 Requirements Synthesizer → /specs/*.sil
  ↓
A-04 Solution Architect → /architecture/*.sil
  ↓
A-05 Builder (6 passes, human gate each) → production codebase
  ↓
A-06 Validator & Certifier → certification document
```

| Agent | Name | Produces |
|-------|------|----------|
| A-00 | Signal Extraction | Mission brief — the heads-up |
| A-01 | Business Logic Extractor | ASCII workflow traces |
| A-02 | UI Archaeologist | ASCII wireframes |
| A-03 | Requirements Synthesizer | Semantic intent specs |
| A-04 | Solution Architect | Stack + implementation blueprints |
| A-05 | Builder | Production codebase — 6 passes |
| A-06 | Validator & Certifier | Certification document |

Full agent prompts in [`docs/phoenix/agents/`](docs/phoenix/agents/).

---

## EMBER — Semantic Intent Language

Every artifact every agent produces is written in `.sil` format.

```
CONSTRUCT  workflow
ID         cart.checkout
VERSION    1
─────────────────────────────────────────
entry:  POST /cart/submit
actor:  authenticated user

  validateCart(cartId, userId)
  calculateTotal(items, promoCode)
  chargePayment(total, method)      → Stripe
  createOrder(cartId, chargeId)     → DB write
  sendConfirmation(userId, orderId) → SendGrid

out:    orderId, 200 OK
error:  payment failure → 402, order not created

confidence:  high
```

Human readable. Agent parseable. Git diffable. Permanent.

Full specification: [`docs/phoenix/EMBER-SIL-SPEC.md`](docs/phoenix/EMBER-SIL-SPEC.md)

---

## Runtime

The Phoenix Runtime is the CLI orchestration layer for the pipeline.

**→ [github.com/semanticintent/phoenix-runtime](https://github.com/semanticintent/phoenix-runtime)**

```bash
npm install @semanticintent/phoenix-runtime

phoenix init my-project
phoenix run a-00
phoenix status
phoenix gate pass-1 --approve
phoenix run a-06
```

---

## The Human Layer

Agents execute. Humans decide.

At every pass in A-05 and before A-06 runs, a human reviews
output and signs off. Not optional. Not bypassable. The gates
are where tribal knowledge enters and judgment calls get made
that no agent can make.

---

## Repository Structure

```
project-phoenix/
├── README.md                    # This file
├── EMBER-CITATION.cff           # EMBER spec citation metadata
├── ZENODO-ARCHIVING.md          # Deposit guide for EMBER + runtime
├── docs/
│   └── phoenix/
│       ├── README.md            # Pipeline overview
│       ├── EMBER-SIL-SPEC.md    # EMBER language specification
│       └── agents/
│           ├── A-00-SIGNAL-EXTRACTION.md
│           ├── A-01-BUSINESS-LOGIC-EXTRACTOR.md
│           ├── A-02-UI-ARCHAEOLOGIST.md
│           ├── A-03-REQUIREMENTS-SYNTHESIZER.md
│           ├── A-04-SOLUTION-ARCHITECT.md
│           ├── A-05-BUILDER.md
│           └── A-06-VALIDATOR-CERTIFIER.md
└── runtime/
    └── README.md                # → pointer to phoenix-runtime repo
```

---

## Ecosystem

```
Methodology-as-Infrastructure   DOI: 10.5281/zenodo.18946631
  ↓
Project Phoenix (this repo)     DOI: 10.5281/zenodo.18904231
  ├── EMBER .sil spec           DOI: [pending]
  └── phoenix-runtime           DOI: [pending]
       github.com/semanticintent/phoenix-runtime
```

**Related:**
- [Cormorant Foraging Framework](https://github.com/semanticintent/cormorant-foraging-framework)
- [6D Foraging Methodology](https://github.com/semanticintent/6d-foraging-methodology)
- [CAL Runtime](https://github.com/semanticintent/cal-runtime) — sibling DSL
- [semanticintent.ai](https://semanticintent.ai) — product site

---

## Citation

```bibtex
@misc{shatny2026phoenix,
  author = {Shatny, Michael},
  title = {Project Phoenix: The Agentic Greenfield Pipeline for Legacy Modernization},
  year = {2026},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.18904231},
  url = {https://github.com/semanticintent/project-phoenix},
  note = {ORCID: 0009-0006-2011-3258}
}
```

---

## License

CC BY 4.0 — share and adapt with attribution.

---

*"You don't migrate a Phoenix. It burns and rises."*
