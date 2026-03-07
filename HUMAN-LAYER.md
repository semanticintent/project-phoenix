# The Human Layer

> *Agents execute. Humans decide.*

## Why Humans Are the Critical Path

Project Phoenix is a six-agent pipeline. But the seventh participant -- the human -- is the most important one. AI agents can extract business logic, map interfaces, synthesize requirements, design architectures, build code, and validate results. What they cannot do:

- **Interview stakeholders** who carry tribal knowledge
- **Resolve ambiguity** when the code contradicts the business intent
- **Make judgment calls** about which business rules are still relevant
- **Sign off** on the specification before building begins
- **Decide go/no-go** at every gate in the pipeline

These aren't limitations of current AI. They're structural properties of the problem. Legacy systems exist in an organizational context that no codebase can fully capture.

---

## The AI Software Lead

In a Phoenix engagement, the human role is the **AI Software Lead** -- a senior practitioner who:

1. **Orchestrates** the six agents across the pipeline
2. **Validates** outputs at every stage before the next agent begins
3. **Supplements** agent findings with stakeholder interviews and domain expertise
4. **Resolves** conflicts between what the code does and what the business needs
5. **Makes** the architectural decisions that require judgment, not just analysis

This isn't a project manager role. It requires deep technical understanding combined with business acumen -- the ability to read an agent's business rules catalog and know whether it captured the right intent.

---

## Human Touchpoints in the Pipeline

| Pipeline Stage | Human Responsibility |
|---|---|
| **Agent 1: Extractor** | Validate business rules against stakeholder knowledge. Flag obsolete vs. essential rules. |
| **Agent 2: Archaeologist** | Confirm user journeys match actual workflows. Identify undocumented processes. |
| **Agent 3: Synthesizer** | Review unified spec for completeness. Resolve ambiguity flags. |
| **Agent 4: Architect** | Approve tech stack and architecture. Confirm organizational alignment. |
| **Agent 5: Builder** | Review critical code paths. Validate implementation matches specification. |
| **Agent 6: Validator** | Final sign-off on regression results. Accept or reject gap exceptions. |

---

## What Agents Can't Know

Every legacy system contains knowledge that lives outside the code:

- **Tribal knowledge** -- "We do it this way because of a regulatory change in 2012 that nobody documented"
- **Political context** -- "That module exists because two departments couldn't agree on a shared process"
- **Future intent** -- "We've been meaning to change that workflow but never had the budget"
- **Edge cases from experience** -- "That validation rule exists because of a specific incident with a specific client"

The AI Software Lead bridges the gap between what the agents extract from code and what the organization actually needs.

---

## The Gate Model

Phoenix operates on a **gate model** -- no agent's output passes to the next stage without human review and approval.

```
[Agent 1] -> GATE -> [Agent 2] -> GATE -> [Agent 3] -> GATE
                                                           |
[Agent 6] <- GATE <- [Agent 5] <- GATE <- [Agent 4] <- GATE
```

At each gate, the AI Software Lead can:
- **Approve** -- output is complete and accurate, proceed
- **Supplement** -- output needs additional context from stakeholders
- **Revise** -- agent missed something, re-run with additional guidance
- **Escalate** -- fundamental ambiguity requires business owner decision

This ensures that no compounding errors propagate through the pipeline.

---

*"The agents see the code. The human sees the context."*
