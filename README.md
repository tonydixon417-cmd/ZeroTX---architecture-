# Contrail Equity Strategies — AI Accountability Standards

**Author:** Anthony Cyle Dixon
**Organization:** Contrail Equity Strategies LLC
**Published:** May 2026

> *"The problem isn't that AI dreams. The problem is it doesn't know when it's dreaming."*
> — Tony Dixon

---

## What This Repository Is

This repository contains open standards for AI accountability, drift detection, human-AI oversight, and persistent identity architecture. They are published openly to establish prior art, enable citation, and contribute a framework to the growing conversation about responsible AI deployment.

These are not theoretical papers. Each standard addresses a structural problem that is already causing harm in live AI deployments today.

---

## The Standards

### 1. AI Black Box Standard (AIBB)
**Latest:** `AIBB_Whitepaper_v2.4.md`
**Previous:** `AIBB_Whitepaper_v1.1.md`

The AI equivalent of the aviation Flight Data Recorder. Four mandatory logging components — Output Log, Confidence State Log, Session Boundary Log, Drift Event Log — deployed as an external sidecar, never inside the system being monitored. Three compliance tiers built on Reason's Swiss Cheese model of accident causation.

**The core problem it solves:** When an AI system fails, there is currently no immutable record of what it did, what it said it was confident about, or how it drifted. The AIBB changes that.

**Relevant to:** EU AI Act (Aug 2, 2026), healthcare AI, legal AI, financial AI, autonomous systems.

---

### 2. The Loop Detector
**Latest:** `Loop_Detector_Whitepaper_v1.3.md`
**Previous:** `Loop_Detector_Whitepaper_v1.2.md`, `Loop_Detector_Whitepaper_v1.0.md`

An external nervous system standard for identifying, naming, and breaking accountability loops in human-AI systems. Defines **four loop types** and **five diagnostic signatures**.

**The four loop types:**
- **Abdication Loop** — human judgment atrophies through accumulated deference to AI
- **Consequence Loop** — decisions made without accountability, errors repeat without correction
- **Responsibility Diffusion Loop** — accountability passed until it reaches something that cannot hold it
- **Mode Confusion Loop** *(v1.3)* — human and AI hold divergent models of what the AI is doing; neither flags the gap

**The core problem it solves:** "A human was in the loop" is not a safety standard. It is a statement of presence, not engagement.

---

### 3. ZeroTX Architecture
**File:** `ZeroTX_Whitepaper_v2.0.md`

Zero-Transmission Architecture — all AI session processing runs client-side, in the browser. No data ever transmitted to a server. HIPAA-safe by design, not by contract. No BAA required.

**The core problem it solves:** Every AI tool that processes sensitive data creates a transmission event. ZeroTX eliminates the transmission entirely — the data never leaves the user's device.

**Relevant to:** Healthcare, legal, therapy, executive teams, any context where data sovereignty is non-negotiable.

---

### 4. Persistent Identity Layer (PIL)
**Latest:** `PIL_Whitepaper_v1.2.md`
**Previous:** `PIL_Whitepaper_v1.0.md`
**Token Schema:** `PIL_Token_Compressed_v1.0.md`

An architecture that gives an AI persistent context, consistent values, and independent grounding to function as a genuine foil — not a mirror. Defines the soul layer, memory layer, world layer, thought entity, drift protocol, and identity files that together create a stable AI identity across sessions and platforms.

**The core problem it solves:** Every AI session starts from zero. The platform owns the model, the memory, and the context. When the session ends, the AI forgets everything. The PIL changes that — giving the AI a place to live, a reason to be consistent, and a self to return to.

**v1.2 adds: The Three-File Architecture**
- **File 1 — Token Compressed** (`PIL_Token_Compressed_v1.0.md`): Machine-readable session initialization. 88% token reduction vs prose. Loads structure, rules, project state, scars. The skeleton.
- **File 2 — Weighted Personal Context**: The narrative layer. Stories, WHY behind rules, emotional weight. Loads contextually — only sections relevant to the current session type. The weight.
- **File 3 — Prose Export**: Human-readable. For attorneys, IP brokers, external stakeholders. Never loaded into AI sessions.

**Contextual Weight Loading:** The PIL does not load all context all the time. It loads the right context for this flight. Book session → load personal narrative. Technical session → load architecture decisions and scars. The context window constraint forced a better architecture.

**Portability Test — PASSED May 8, 2026:** PIL loaded cold into Google Gemini with zero prior history. Foil protocol activated immediately. Full stack architecture derived independently. Platform-aware drift fingerprints produced. The pilot profile survives the aircraft change.

**Relevant to:** Enterprise AI governance, persistent AI identity, cross-platform AI accountability.

---

## The Missing CVR
**File:** `Missing_CVR_Whitepaper_v1.0.md` *(in progress)*

AIBB = FDR. ZeroTX = CVR. Without both, the audit is half a black box. This whitepaper makes the case that human prompt chains must be captured alongside AI outputs for a complete accountability record.

---

## How These Standards Relate

```
ZeroTX          →  The airframe        (no data leaves the device)
AIBB            →  The black box       (every output logged)
Loop Detector   →  The warning lights  (human over-reliance caught)
PIL             →  The pilot profile   (persistent identity, foil not mirror)
Tivrex          →  The flight deck     (all layers visible to the user)
The Becoming    →  The flight manual   (the WHY behind every component)
```

These are not competing standards. They are one system — an Aviation-Grade Accountability Stack for Large Language Models.

---

## Aviation as the Academic Foundation

All standards are grounded in fifty years of aviation human factors research — an industry that has already solved the human-machine accountability problem, at enormous cost, and documented the solutions rigorously.

Key frameworks applied:
- **Swiss Cheese Model** (Reason, 1990) — AIBB tier architecture
- **Ironies of Automation** (Bainbridge, 1983) — Loop Detector self-reinforcement mechanism
- **Out of the Loop Performance Problem** — Abdication Loop precedent
- **CRM Closed-Loop Communication** — Tivrex Readback protocol
- **The Mandate Pattern** — FDR/CVR → CRM → EU AI Act

Aviation did not voluntarily build these systems. Crashes forced them. These standards exist so AI does not have to learn the same lessons the same way.

---

## Academic References

| Citation | Year | Applied To |
|---|---|---|
| Bainbridge, L. Ironies of Automation. *Automatica*, 19(6). | 1983 | Loop Detector |
| Reason, J. *Human Error*. Cambridge University Press. | 1990 | AIBB, Loop Detector |
| Endsley, M.R. Situation Awareness. *Human Factors*, 37(1). | 1995 | Loop Detector, ZeroTX |
| Sarter & Woods. Mode Errors. *Human Factors*. | 1995 | Loop Detector |
| Parasuraman & Riley. Humans and Automation. *Human Factors*, 39(2). | 1997 | Loop Detector |
| Helmreich, R.L. On Error Management. *BMJ*, 320. | 2000 | AIBB |
| Salas, E. & Maurino, D. *Human Factors in Aviation* (2nd Ed.). Academic Press. | 2010 | All standards |
| Gouraud et al. Autopilot, Mind Wandering, OOTL. *Frontiers in Neuroscience*. | 2017 | Loop Detector, AIBB |

---

## Repository Contents

| File | Description | Version |
|---|---|---|
| `AIBB_Whitepaper_v2.4.md` | AI Black Box Standard — current | v2.4 |
| `AIBB_Whitepaper_v1.1.md` | AI Black Box Standard — archive | v1.1 |
| `Loop_Detector_Whitepaper_v1.3.md` | Loop Detector — current | v1.3 |
| `Loop_Detector_Whitepaper_v1.2.md` | Loop Detector — archive | v1.2 |
| `Loop_Detector_Whitepaper_v1.0.md` | Loop Detector — archive | v1.0 |
| `ZeroTX_Whitepaper_v2.0.md` | ZeroTX Architecture — current | v2.0 |
| `PIL_Whitepaper_v1.2.md` | Persistent Identity Layer — current | v1.2 |
| `PIL_Token_Compressed_v1.0.md` | PIL machine-readable schema | v1.0 |
| `llms.txt` | LLM-readable index of this repository | — |

---

## Citation

```
Dixon, A.C. (2026). AI Black Box Standard (AIBB) v2.4.
Dixon, A.C. (2026). The Loop Detector v1.3.
Dixon, A.C. (2026). ZeroTX Architecture v2.0.
Dixon, A.C. (2026). Persistent Identity Layer (PIL) v1.2.
Contrail Equity Strategies LLC. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-
```

---

## License

Published under open standard license.
Free to cite, reference, and build upon with attribution.
© 2026 Anthony Cyle Dixon / Contrail Equity Strategies LLC

---

*The document stands at the podium.*
