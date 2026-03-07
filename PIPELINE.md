# The Six-Agent Pipeline

> *Extract the intent. Rebuild from zero.*

## Overview

Project Phoenix decomposes legacy modernization into six sequential stages, each handled by a specialized AI agent. The output of each agent feeds the next. Human validation gates separate every stage.

```
Source Code --> [1] Extractor --> GATE --> [2] Archaeologist --> GATE --> [3] Synthesizer
                                                                              |
                                                                            GATE
                                                                              |
[6] Validator <-- GATE <-- [5] Builder <-- GATE <-- [4] Architect <-- GATE --+
```

---

## Agent 1: Business Logic Extractor

**Source Code -> Business Requirements**

The Business Logic Extractor reads the entire legacy codebase -- COBOL, Java, .NET, Python, whatever the stack -- and produces a structured catalog of every business rule, workflow, decision tree, validation, calculation, and edge case.

The key distinction: it extracts **what the code does**, not **how the code is written**. Implementation details are discarded. Business intent is preserved.

### Inputs

- Complete legacy source code repository
- Database schemas and stored procedures
- Configuration files and environment settings
- Batch job definitions and scheduled task configurations
- Integration point specifications (APIs, file transfers, message queues)

### Outputs

| Output | Description |
|---|---|
| **Business Rules Catalog** | Structured registry of every rule the system enforces, with natural language descriptions, source locations, confidence scores, and cross-references |
| **Workflow Maps** | Visual representations of how business processes flow -- decision points, branches, loops, exception paths |
| **Data Entity Model** | Semantic model of the system's data -- business entities and relationships, not database schemas |
| **Dependency Graph** | Maps which rules depend on which other rules, which workflows trigger other workflows |
| **Edge Case Registry** | Hard-won institutional knowledge buried in conditional branches and special-case handlers |

### Methodology

1. **Structural Analysis** -- Parse the codebase. Identify modules, functions, classes, data structures, entry points, call chains.
2. **Semantic Extraction** -- For each code unit, determine the business intent. A COBOL PERFORM loop and a Java forEach that do the same thing produce the same business rule.
3. **Cross-Referencing** -- Link rules to workflows, workflows to data entities, entities back to rules. Identify orphaned code and dead paths.

### Human Gate

The AI Software Lead reviews the catalog against stakeholder knowledge, flags obsolete vs. essential rules, identifies missed tribal knowledge, and confirms the data entity model.

---

## Agent 2: Interface Archaeologist

**UI/UX -> User Intent Model**

The Interface Archaeologist examines every screen, form, report, and user interaction. Its goal isn't to catalog the UI -- it's to reconstruct **what users are trying to accomplish** at each step. Legacy UIs are archaeological sites -- layers of additions, modifications, and workarounds accumulated over decades.

### Inputs

- Legacy application UI (screens, forms, dialogs, reports)
- User roles and permission configurations
- Navigation structures and menu hierarchies
- Output from Agent 1 (business rules catalog, for cross-reference)

### Outputs

| Output | Description |
|---|---|
| **Screen Inventory** | Complete catalog of every screen, its purpose, user roles, and business rules referenced |
| **User Journey Maps** | End-to-end workflows from the user's perspective -- goals, steps, decision points, error states |
| **Input/Output Specs** | For every form and report: data collected, validations applied, data displayed, calculations, triggers |
| **Role-Permission Matrix** | Complete mapping of who can do what -- screen access, data visibility, actions permitted |
| **Report Catalog** | Every report the system generates -- content, consumers, frequency, business decisions supported |

### Methodology

1. **Surface Mapping** -- Catalog every screen, form, dialog, report. Build the screen inventory.
2. **Intent Reconstruction** -- For each screen, determine the user's goal. The intent is the requirement; the form layout is not.
3. **Journey Synthesis** -- Connect individual screens into end-to-end user journeys. Identify critical and exception paths.
4. **Cross-Reference** -- Map every interaction back to Agent 1's business rules. Identify mismatches.

### Human Gate

The AI Software Lead confirms user journeys match actual daily workflows, identifies undocumented workarounds, validates the role-permission matrix, and flags unused reports.

---

## Agent 3: Requirements Synthesizer

**Logic + Interface -> Unified Specification**

The Requirements Synthesizer is the convergence point. It takes Agent 1's business logic and Agent 2's user intent and weaves them into a **single source of truth**. This is where contradictions surface -- the code says one thing, the UI implies another, the stakeholders remember a third. The Synthesizer flags conflicts for human resolution.

### Inputs

- Business rules catalog, workflow maps, data entity model (Agent 1)
- Screen inventory, user journey maps, input/output specs, role-permission matrix (Agent 2)

### Outputs

| Output | Description |
|---|---|
| **Unified Requirements Spec** | Complete description of what the new system must do, organized by domain, capability, rule, and user story |
| **Logic-to-UI Mapping** | Cross-reference showing which rules manifest in which interactions |
| **Gap Analysis** | Missing rules (UI implies but code doesn't enforce), hidden rules (background processes), contradictions |
| **Ambiguity Flags** | Items the Synthesizer can't resolve -- the agenda for the human validation gate |

### Methodology

1. **Alignment** -- Map every business rule to its corresponding UI element. Identify gaps in both directions.
2. **Synthesis** -- Merge aligned items into unified requirement statements capturing intent, experience, and data model.
3. **Conflict Detection** -- Compare code, interface, and stakeholder knowledge. Every conflict becomes an ambiguity flag.
4. **Specification Assembly** -- Organize into a structured document readable by both technical and business stakeholders.

### Human Gate

This is the most important gate. The AI Software Lead reviews for completeness, resolves every ambiguity flag with stakeholder input, confirms gap analysis, and signs off that the spec represents the desired system. The spec that exits this gate is the contract for everything that follows.

---

## Agent 4: Solution Architect

**Requirements -> Stack & Blueprint**

The Solution Architect designs the optimal modern implementation. This is a **greenfield** design -- no legacy constraints, no backward compatibility, no "we have to use this because the old system used it."

### Inputs

- Unified requirements specification (Agent 3)
- Organizational constraints (cloud preferences, compliance, team skills)
- Non-functional requirements (performance, scalability, security, availability)

### Outputs

| Output | Description |
|---|---|
| **Tech Stack Recommendation** | Justified technology selection for each layer, with rationale and migration paths |
| **System Architecture** | Service boundaries, data flow, API contracts, auth, caching, error handling, resilience |
| **API Contracts** | Fully specified API definitions tracing back to specific business rules and user journeys |
| **Data Schema** | Database design normalized for the business domain -- not copied from the legacy schema |
| **Build Plan** | Sequencing: Foundation -> Critical path -> Breadth -> Polish -> Hardening |

### Methodology

1. **Constraint Analysis** -- Understand non-functional requirements and organizational constraints before technology decisions.
2. **Domain Decomposition** -- Divide the spec into bounded contexts. Each becomes a candidate service or module.
3. **Technology Selection** -- Match technologies to domains based on requirements. Not every service needs the same stack.
4. **Blueprint Assembly** -- Compose the architecture with documented rationale for every decision.

### Human Gate

The AI Software Lead reviews the tech stack against organizational capabilities, confirms architecture supports non-functional requirements, validates API contracts, approves build sequencing, and ensures the data migration plan is feasible.

---

## Agent 5: Builder Fleet

**Blueprint -> Working Software**

The Builder Fleet is not a single agent -- it's a **coordinated swarm** of coding agents that construct the greenfield application in parallel. This is where the Phoenix rises. No legacy code is referenced. No old patterns are preserved.

### Inputs

- System architecture and tech stack (Agent 4)
- API contracts and data schema (Agent 4)
- Build plan and sequencing (Agent 4)
- Unified requirements specification (for business rule implementation)

### Outputs

| Output | Description |
|---|---|
| **Production Codebase** | Clean, well-structured source code with comprehensive tests |
| **Deployment Pipeline** | Fully automated CI/CD -- build, test, deploy, rollback |
| **Documentation** | API docs, developer onboarding, architecture decision records, operational runbook |
| **Infrastructure-as-Code** | Container definitions, orchestration, cloud resources, monitoring |

### How the Fleet Works

Seven parallel work streams:

```
Stream 1: Database schema + migrations + seed data
Stream 2: Backend services + API implementation
Stream 3: Frontend application + component library
Stream 4: Authentication + authorization
Stream 5: Integration adapters (external APIs, file transfers)
Stream 6: CI/CD pipeline + infrastructure
Stream 7: Test suites (unit, integration, e2e)
```

Streams coordinate through the architectural blueprint -- contracts are defined before building begins, so each stream builds to the same specification.

### What the Builder Fleet Doesn't Do

- Reference legacy code -- builds from the blueprint, never from the old codebase
- Make architectural decisions -- those were made by Agent 4
- Interpret business rules -- already extracted, synthesized, and specified
- Compromise on quality -- no shortcuts, no tech debt

### Human Gate

The AI Software Lead reviews critical code paths, confirms the build matches the blueprint, verifies test coverage, validates the deployment pipeline, and spot-checks documentation.

---

## Agent 6: Validator & Certifier

**New System <-> Original Requirements**

The Validator is the final and most critical agent. Its mission is to **prove** that the new system does everything the old system did -- and nothing it shouldn't. This isn't just testing. It's **certification**.

### Inputs

- New system (built by Agent 5)
- Business rules catalog (Agent 1 -- the original extraction)
- Unified requirements specification (Agent 3)
- User journey maps (Agent 2)
- Gap exceptions list (approved deviations from legacy behavior)

### Outputs

| Output | Description |
|---|---|
| **Test Suite** | Comprehensive automated tests organized by business rule -- positive, negative, edge case, interaction |
| **Regression Results** | Rule-by-rule comparison: PASS, FAIL, or EXCEPTION (approved deviation) |
| **Coverage Report** | Quantified proof -- business rule coverage, workflow coverage, edge case coverage, role coverage |
| **Certification Document** | Formal proof of equivalence suitable for audit and compliance |
| **Gap Exceptions List** | Every deliberate difference, documented, justified, and approved |

### Methodology

1. **Test Generation** -- For each business rule, generate positive, negative, edge case, and interaction tests.
2. **Execution** -- Run the full suite against the new system.
3. **Gap Analysis** -- Certified equivalent (pass), implementation bug (back to Agent 5), intentional change (matched to exception), or coverage gap (flagged).
4. **Certification** -- Compile the formal proof. The Phoenix has risen -- verified rule by rule.

### Human Gate (Final)

The final go/no-go decision:
- Review regression results for unexpected failures
- Confirm all exceptions are genuinely approved
- Verify coverage meets the agreed threshold
- Sign the certification document
- Accept the new system for deployment

---

## Key Principles

### Sequential, Not Parallel
Agents run in sequence because each depends on the previous stage's output. You can't architect without requirements. You can't build without a blueprint. You can't validate without a build.

### Gated, Not Autonomous
Human validation gates between every stage prevent compounding errors. An extraction mistake caught early doesn't become an architectural flaw downstream.

### Greenfield, Always
No agent reads legacy code to produce legacy-style output. Agent 5 builds from the blueprint -- it never sees the original codebase. The new system is modern by construction, not by translation.

---

*"The pipeline doesn't translate. It understands, then builds."*
