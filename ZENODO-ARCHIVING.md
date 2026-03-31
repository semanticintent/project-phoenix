# Zenodo Archiving Guide
**Phoenix Runtime + EMBER .sil Specification**

Two separate deposits. Two separate DOIs.
Follow this guide for each one.

---

## Deposit 1 — EMBER Language Specification

### What to deposit
The EMBER .sil language specification — the format,
the five constructs, the rules, the examples.

**Primary file:** `docs/phoenix/EMBER-SIL-SPEC.md`
**Citation file:** `EMBER-CITATION.cff`
**Also include:** `docs/phoenix/agents/` — the seven agent prompts
that produce and consume .sil artifacts

### Zenodo metadata

```
Title:
  EMBER: Semantic Intent Language Specification (.sil)

Authors:
  Michael Shatny (ORCID: 0009-0006-2011-3258)

Description:
  EMBER is the artifact representation language of Project Phoenix.
  Defines the .sil (Semantic Intent Language) file format — five
  constructs (SIGNAL, WORKFLOW, SCREEN, SPEC, EPISODE) for carrying
  methodology artifacts across a seven-agent legacy modernization
  pipeline. The second instantiation of the Methodology-as-Infrastructure
  pattern: where CAL (.cal) is methodology-as-executor, EMBER (.sil) is
  methodology-as-memory. Produced March 2026.

Version:    0.1.0
License:    MIT
Date:       2026-03-31

Resource type: Software / Specification

Keywords:
  dsl, semantic-intent-language, sil, ember, legacy-modernization,
  methodology-as-infrastructure, artifact-representation, agent-pipeline,
  phoenix, business-logic-extraction

Related identifiers:
  Is part of → 10.5281/zenodo.18904231  (project-phoenix)
  Cites      → 10.5281/zenodo.18946631  (methodology-as-infrastructure)
  Cites      → 10.5281/zenodo.18905197  (CAL language spec)
  Cites      → 10.5281/zenodo.17114972  (semantic intent SSOT)
```

---

## Deposit 2 — Phoenix Runtime

### What to deposit
The runtime architecture specification and CLI design.
At v0.1.0 this is the architecture sketch — deposit now to
timestamp the design. Re-deposit at v1.0.0 when npm published.

**Primary file:** `runtime/RUNTIME-SKETCH.md`
**Citation file:** `runtime/CITATION.cff`
**Also include:** `docs/phoenix/` — full agent prompt library

### Zenodo metadata

```
Title:
  Phoenix Runtime: Orchestration Layer for the
  Seven-Agent Legacy Modernization Pipeline

Authors:
  Michael Shatny (ORCID: 0009-0006-2011-3258)

Description:
  Phoenix Runtime is the CLI orchestration layer for Project Phoenix.
  Manages .sil artifact state, enforces human gates, injects episode
  context into every agent run. Model-agnostic — produces contextualized
  prompts rather than calling AI APIs. Seven agents: A-00 Signal
  Extraction through A-06 Validator & Certifier. Built on EMBER
  Semantic Intent Language (.sil). TypeScript, MIT license.
  npm: @semanticintent/phoenix-runtime. Produced March 2026.

Version:    0.1.0
License:    MIT
Date:       2026-03-31

Resource type: Software

Keywords:
  legacy-modernization, agent-pipeline, business-logic-extraction,
  ember, sil, semantic-intent, methodology-as-infrastructure,
  phoenix, cli, typescript, npm

Related identifiers:
  Is part of → 10.5281/zenodo.18904231  (project-phoenix)
  Cites      → 10.5281/zenodo.18946631  (methodology-as-infrastructure)
  Cites      → 10.5281/zenodo.18905193  (CAL runtime)
  Cites      → 10.5281/zenodo.18905197  (CAL language spec)
```

---

## GitHub → Zenodo Integration

If you have Zenodo GitHub integration enabled on project-phoenix:

1. Go to https://zenodo.org/account/settings/github/
2. Confirm `semanticintent/project-phoenix` is enabled
3. Create a release for each deposit:

**Release 1 — EMBER spec:**
```
Tag:    ember-v0.1.0
Title:  EMBER: Semantic Intent Language Specification v0.1.0
```

**Release 2 — Runtime:**
```
Tag:    runtime-v0.1.0
Title:  Phoenix Runtime v0.1.0
```

Zenodo will auto-mint a DOI per release.
Update CITATION.cff files with the assigned DOIs after minting.

---

## DOI Update Checklist

After both DOIs are minted, update these files:

- [ ] `EMBER-CITATION.cff` — add EMBER DOI
- [ ] `runtime/CITATION.cff` — add runtime DOI
- [ ] `docs/phoenix/EMBER-SIL-SPEC.md` — add DOI badge
- [ ] `runtime/RUNTIME-SKETCH.md` — add DOI badge
- [ ] `docs/phoenix/README.md` — add both DOI badges
- [ ] `cal-site/docs/ember.md` — add DOI badge to EMBER page
- [ ] `semanticintent-ai` README or about page — reference both
- [ ] Zenodo cross-reference: add each DOI as related to the other

---

## Expected DOI Count After These Deposits

```
Existing:  8 DOIs
New:       2 DOIs (EMBER spec + Phoenix runtime)
Total:    10 DOIs
```

The body of work at 10 DOIs:
  Semantic Intent SSOT
  Project Phoenix
  PACE Pattern
  6D Foraging Methodology
  Cormorant Foraging Framework
  CAL Runtime
  CAL Documentation
  Methodology-as-Infrastructure
  Methodology Drift
  EMBER Spec             ← new
  Phoenix Runtime        ← new

---

*Archiving guide produced March 2026*
*Follow the same pattern used for CAL runtime deposits*
