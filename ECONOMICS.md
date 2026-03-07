# The Numbers

> *Orders of magnitude. Not marginal improvement.*

## Two Models, Compared

| Dimension | Traditional Migration | Phoenix Pipeline |
|---|---|---|
| **Approach** | Translate code line-by-line | Extract business intent, rebuild from zero |
| **Timeline** | 18-36 months (often 5+ years) | 3-6 months |
| **Team Size** | 200+ consultants and contractors | Small team + agent fleet |
| **Budget** | $50M-$500M | Fraction of traditional cost |
| **Technical Debt** | Carried forward from legacy system | Zero -- greenfield architecture |
| **Failure Rate** | 70% stall or fail | Validated at every gate |
| **Business Disruption** | Years of parallel operations | Months, with continuous validation |
| **Output Quality** | Yesterday's architecture in a new language | Modern stack, modern UX, modern patterns |

---

## Why the Economics Shift

The cost structure of legacy modernization has been dominated by **labor** -- hundreds of consultants reading, understanding, and rewriting code over years. This is fundamentally a **comprehension problem**: how do you understand what 2 million lines of COBOL actually do?

AI agents solve the comprehension problem at machine speed. What took a team of 50 analysts six months to catalog, an agent can extract in hours. This collapses the cost curve.

### Time Compression

| Phase | Traditional | Phoenix |
|---|---|---|
| Discovery & Analysis | 3-6 months | Days (Agents 1-2) |
| Requirements & Design | 3-6 months | 1-2 weeks (Agents 3-4) |
| Build | 6-18 months | 1-3 months (Agent 5) |
| Testing & Validation | 3-6 months | 2-4 weeks (Agent 6) |
| **Total** | **18-36 months** | **3-6 months** |

### Team Compression

Traditional migration requires large teams because **comprehension doesn't parallelize well** with humans. You can't put 200 people on reading the same codebase and get 200x understanding.

AI agents parallelize comprehension naturally. The Business Logic Extractor can process the entire codebase simultaneously. The Builder Fleet can construct backend, frontend, database, and infrastructure in parallel.

The human team in a Phoenix engagement is small by design:
- 1 AI Software Lead (orchestration, validation, stakeholder engagement)
- 1-2 domain experts (tribal knowledge, business sign-off)
- 1 infrastructure engineer (deployment, environments)

---

## Risk Profile

Traditional migration carries **compounding risk** -- errors in the translation phase propagate through build and testing, often discovered too late to fix without significant rework.

Phoenix carries **gated risk** -- each stage is validated before proceeding:

- Errors caught at extraction don't become architectural flaws
- The specification is approved before a single line of code is written
- Agent 6 regression-tests against the original business rules, not the original code
- The gap exceptions list is explicit -- you know exactly what's different and why

---

## The Real Question

The economics of Phoenix aren't about saving money on a migration project. They're about changing **what's possible**.

Systems that were "too expensive to modernize" -- the ones organizations have been maintaining for decades because the migration cost exceeded the maintenance cost -- are now within reach. The calculus changes when you can extract the intent in days instead of months.

The $1.7 trillion annual legacy maintenance spend isn't a fixed cost. It's an opportunity waiting for the right economics.

---

*"The question isn't whether you can afford to modernize. It's whether you can afford not to."*
