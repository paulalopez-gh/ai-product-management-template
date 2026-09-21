# Juno PM — AI Copilot for RocketShip’s Product Org

> An AI Associate PM that turns Slack/Notion/Jira chaos into a prioritised top-3 risk list every morning.

_Paula J. López · AI PM Cohort · Sep 2026_

Repo: https://github.com/paulalopez-gh/ai-product-management-template

This repo is my final project for the AI Product Management Certification — **Juno PM**. Each module’s artefact lives in its own folder; this README is the dashboard and the pitch.

---

## Module artefacts

### M1 · Prompting
- **System prompt** — [`01-prompting/system-prompt.md`](01-prompting/system-prompt.md)
- **Prototype** — https://lovable.dev/preview/r5mhhmt3kgKlWdHVV3SDlyIKeqZpWt3Q

### M2 · Strategy
- **Decision matrix** — [`02-strategy/decision-matrix.md`](02-strategy/decision-matrix.md)
- **AI Strategy one-pager** — [`02-strategy/strategy-one-pager.md`](02-strategy/strategy-one-pager.md)

### M3 · RAG / AI PRD
- **AI PRD** — [`03-rag-prd/prd.md`](03-rag-prd/prd.md)

### M4 · AI-Native UX
- **AI user flow** — [`04-ai-ux/user-flow.md`](04-ai-ux/user-flow.md)
- **Trust-gap mitigations** — [`04-ai-ux/trust-gaps.md`](04-ai-ux/trust-gaps.md)

### M5 · Agentic Workflows
- **Agent Workflow Spec (AWSpec)** — [`05-agentic-workflows/awspec.md`](05-agentic-workflows/awspec.md)
- **Agent Control Panel** — [`05-agentic-workflows/agent-control-panel.md`](05-agentic-workflows/agent-control-panel.md)

### M6 · Evals &amp; Guardrails
- **Eval stack** — [`06-evals/eval-stack.md`](06-evals/eval-stack.md)
- **Human evaluation rubric** — [`06-evals/human-rubric.md`](06-evals/human-rubric.md)

---

## PM Execution Plan

### Where Juno is today
- End-to-end MVP fully designed and documented, including strategy, PRD, AI-native UX, agent architecture, evaluation framework, and governance model.
- The prototype validated the core product hypothesis: evidence-based prioritization reduces dependency on opinion-driven decision making.
- Copilot architecture defined with Human-in-the-Loop controls, ensuring the PM remains the final decision maker before any write or publish action.
- Evaluation framework prepared, including a golden dataset, human review rubric, and release gates. User validation is the next milestone.

### What ships next (next 2 sprints)
- Sprint 1: 
Implement the RAG layer connected to real data sources.
Replace placeholder retrieval components with a production-ready vector store.
Activate automated citation and grounding verification checks.

-Sprint 2
Execute the first round of human evaluations.
Build the initial golden dataset of prioritization scenarios.
Launch a controlled beta with PMs to validate recommendation quality and adoption.

### What I watch (dashboards)
- Daily: thumbs-down rate, regen rate, hand-off rate.
- Weekly: human-rubric mean per dimension; refusal hit-rate; cost per run.
- Per release: golden-set accuracy; format/citation/refusal pass rate.
- User experience: Thumbs-up rate; regenerate rate; abandon rate.
- Operational: p95 latency; cost per run; confidence-score distribution.

### Red lines (what blocks shipping)
- Missing or fabricated citations.
- Hallucinated priorities or customer signals.
- Any PII leakage.
- Human evaluation score below 4.0/5 on Accuracy or Safety.
- Confidence below 70% without PM review and escalation.

### Governance
- Compliance: Explicit exclusion of contracts, executive DMs, and unauthorized data sources; PII protection and redaction requirements.
- Safety: Automatic escalation for legal, regulatory, and low-confidence cases; refusal policies for contracts and sensitive content.
- Reliability: 90-second hard timeout; automatic abort after repeated tool failures.
- Trust: Every recommendation must be traceable to evidence; no external action can be executed without human approval.

---

## Build Insights

- **Friction point.** Retrieving the right evidence is the biggest challenge (source traceability).
- **Key learning.** The problem is not that AI occasionally hallucinates, but that it does so in a highly convincing manner. And it is very difficult for the user to regain trust, especially with predictive models.
- **Aha moment.** No AI system will achieve its goal without a PM behind it making daily decisions to balance latency, cost, and accuracy.


## Repo structure

```
juno-pm/
├── README.md                          ← this dashboard + pitch
├── 01-prompting/
│   ├── system-prompt.md               ← M1: Juno's system prompt
│   └── lovable-prototype.md           ← M1: prototype link + debrief
├── 02-strategy/
│   ├── decision-matrix.md             ← M2: build / buy / fine-tune / partner call
│   └── strategy-one-pager.md          ← M2: AI strategy one-pager
├── 03-rag-prd/
│   └── prd.md                         ← M3: AI PRD with retrieval requirements
├── 04-ai-ux/
│   ├── user-flow.md                   ← M4: AI-native user flow
│   └── trust-gaps.md                  ← M4: trust-gap mitigations
├── 05-agentic-workflows/
│   ├── awspec.md                      ← M5: Agent Workflow Spec
│   └── agent-control-panel.md         ← M5: Agent Control Panel
└── 06-evals/
    ├── eval-stack.md                  ← M6: layered eval stack
    └── human-rubric.md                ← M6: human evaluation rubric
```

---

_Certification submission — AI Product Management Certification._
