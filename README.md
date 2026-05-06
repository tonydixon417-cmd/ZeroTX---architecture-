# Contrail Equity Strategies — AI Accountability Standards

**Author:** Anthony Cyle Dixon
**Organization:** Contrail Equity Strategies LLC
**Published:** May 2026

> *"The problem isn't that AI dreams. The problem is it doesn't know when it's dreaming."*
> — Tony Dixon

---

## What This Repository Is

This repository contains three open standards for AI accountability, drift detection, and human-AI oversight. They are published openly to establish prior art, enable citation, and contribute a framework to the growing conversation about responsible AI deployment.

These are not theoretical papers. Each standard addresses a structural problem that is already causing harm in live AI deployments today.

---

## The Three Standards

### 1. AI Black Box Standard (AIBB)
**Latest:** `AIBB_Whitepaper_v2.4.md`
**Previous:** `AIBB_Whitepaper_v1.1.md`

The AI equivalent of the aviation Flight Data Recorder. Four mandatory logging components — Output Log, Confidence State Log, Session Boundary Log, Drift Event Log — deployed as an external sidecar, never inside the system being monitored. Three compliance tiers built on Reason's Swiss Cheese model of accident causation.

**The core problem it solves:** When an AI system fails, there is currently no immutable record of what it did, what it said it was confident about, or how it drifted. The AIBB changes that.

**v2.4 adds:** Swiss Cheese model as academic foundation for the tier architecture. Aviation mandate pattern (FDR → CRM → EU AI Act) as historical precedent. Component mapping table showing structural match between aviation FDR/CVR and AIBB's four logging components. Academic citation registry.

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

**v1.3 adds:** Full integration of 50 years of aviation human factors research. Bainbridge's Ironies of Automation (1983) as the loop's self-reinforcing mechanism. 77% vigilance failure statistic (Mosier et al., 1994) as empirical baseline for the Rubber Stamp Signature. Aviation Mandate Pattern as regulatory precedent.

**The core problem it solves:** "A human was in the loop" is not a safety standard. It is a statement of presence, not engagement.

---

### 3. ZeroTX Architecture
**File:** `ZeroTX_Whitepaper_v2.0.md`

Zero-Transmission Architecture — all AI session processing runs client-side, in the browser. No data ever transmitted to a server. HIPAA-safe by design, not by contract. No BAA required.

**The core problem it solves:** Every AI tool that processes sensitive data creates a transmission event. ZeroTX eliminates the transmission entirely — the data never leaves the user's device.

**Relevant to:** Healthcare, legal, therapy, executive teams, any context where data sovereignty is non-negotiable.

---

## How These Standards Relate

```
AIBB          →  The evidentiary layer  (logs what happened)
Loop Detector →  The diagnostic layer  (identifies the failure pattern)
ZeroTX        →  The sovereignty layer (ensures data never leaves the boundary)
Tivrex        →  The user-facing tool  (session-level drift detection — tivrex.app)
```

These are not competing standards. They are designed to operate as a stack — each layer handling a distinct problem, none overlapping.

---

## Aviation as the Academic Foundation

All three standards are grounded in fifty years of aviation human factors research — an industry that has already solved the human-machine accountability problem, at enormous cost, and documented the solutions rigorously.

Key frameworks applied:
- **Swiss Cheese Model** (Reason, 1990) — AIBB tier architecture
- **Ironies of Automation** (Bainbridge, 1983) — Loop Detector self-reinforcement mechanism
- **Out of the Loop Performance Problem** — Abdication Loop precedent
- **CRM Closed-Loop Communication** — Tivrex Readback protocol
- **The Mandate Pattern** — FDR/CVR → CRM → EU AI Act

Aviation did not voluntarily build these systems. Crashes forced them. The AIBB, Loop Detector, and ZeroTX exist so AI does not have to learn the same lessons the same way.

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

## Citation

```
Dixon, A.C. (2026). AI Black Box Standard (AIBB) v2.4.
Dixon, A.C. (2026). The Loop Detector v1.3.
Dixon, A.C. (2026). ZeroTX Architecture v2.0.
Contrail Equity Strategies LLC. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-
```

---

## License

Published under open standard license.
Free to cite, reference, and build upon with attribution.
© 2026 Anthony Cyle Dixon / Contrail Equity Strategies LLC

---

*The document stands at the podium.*
