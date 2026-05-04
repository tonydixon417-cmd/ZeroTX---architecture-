# AI Accountability Standards
**Published by Contrail Equity Strategies LLC**
*Author: Anthony Cyle Dixon — Springfield, Missouri*

---

## What This Is

This repository contains three independent but related standards for human-AI accountability.

They were developed in response to a single observation: the systems we are building to deploy AI have no black box, no external oversight layer, and no architecture that prevents sensitive data from leaving the device. Aviation solved these problems fifty years ago. AI hasn't solved them yet.

These standards are the proposed framework for doing so.

---

## The Three Standards

---

### 1. Zero-Transmission Architecture (ZeroTX)
**File:** `ZeroTX_Whitepaper_v2.0.md`

**The one sentence:** All user data processing occurs on the user's device. No user content is transmitted to application servers.

ZeroTX is a design principle for AI-adjacent applications that handle sensitive data. Under ZeroTX, the application vendor never receives user content — which means HIPAA's Business Associate rule is never triggered, no BAA is required, and a breach of the application server exposes nothing.

This is not compliance by contract. It is compliance by architecture.

**Who it's for:** Healthcare, legal, financial, enterprise — any context where data confidentiality is required and the current answer is a legal agreement with a vendor you hope doesn't get breached.

**Verification:** Any developer can confirm ZeroTX compliance in under two minutes using browser Developer Tools → Network tab. No trust required.

---

### 2. The AI Black Box Standard (AIBB)
**File:** `AIBB_Whitepaper_v1.1.md`

**The one sentence:** Every significant AI output, confidence state, session boundary, and drift event must be logged in an immutable, human-readable format — and a designated human with defined authority must be responsible for that log.

The AIBB standard is modeled on aviation's flight data recorder and crew resource management framework. AI systems operating in consequential contexts — medicine, law, finance, military, infrastructure — have no black box and no defined accountability structure. The AIBB proposes both.

Key components:
- Four logging requirements: Output, Confidence State, Session Boundary, Drift Events
- Tiered alert architecture: Green / Yellow / Red — modeled on aviation checklists
- The Chief AI Accountability Officer (CAAO) — a structurally independent human role with unilateral authority to halt AI processes
- Sidecar implementation architecture — no hardware required
- Certification framework modeled on the Ken Austin / NIBI methodology licensing model

**Who it's for:** Any organization deploying AI in contexts where a wrong answer has real consequences and no current system exists to catch the drift before it becomes the outcome.

---

### 3. The Loop Detector
**File:** `Loop_Detector_Whitepaper_v1.2.md`

**The one sentence:** Every system that deploys AI has the same structural vulnerability — the feedback mechanism that would catch an error lives inside the system making the error.

The Loop Detector defines three accountability failure types that emerge when AI is deployed without external oversight:

- **The Abdication Loop** — human judgment progressively replaced by machine output until the capacity for independent judgment atrophies
- **The Consequence Loop** — decisions made without accountability, errors repeat without correction, no one owns the outcome
- **The Responsibility Diffusion Loop** — accountability passed from human to human to system until it reaches something that cannot hold it and disappears

Each loop type is defined by five diagnostic signatures. The paper includes a full case study of Cigna's PXDX automated denial system — 300,000 claims denied in two months at 1.2 seconds per review — as a confirmed closed-loop example with all five signatures present.

The Loop Detector operates as an external nervous system — beside the AI system, not inside it. Internal monitors inherit the blind spots of the system they monitor.

**Who it's for:** Education, healthcare, legal, military, enterprise compliance — any organization where humans are rubber-stamping machine output and calling it oversight.

---

## How They Work Together

These are three distinct standards. They can be adopted independently. But they are designed to reinforce each other.

**ZeroTX** solves the transmission problem — sensitive data never leaves the device.

**AIBB** solves the logging problem — every significant AI decision is recorded in an immutable format with a designated human accountable for the log.

**The Loop Detector** solves the oversight problem — an external diagnostic layer identifies when the accountability structure itself has failed.

Together they constitute an infrastructure layer for trustworthy AI deployment. Not a product. Not a vendor promise. A set of open standards that any organization can adopt, audit, and verify independently.

---

## Prior Art Statement

This repository was first published April 4, 2026 to establish public prior art for the Zero-Transmission Architecture standard. The AIBB standard and Loop Detector standard were added May 2026.

Publication is intended to ensure these standards remain open and unpatentable by any party.

---

## The Reference Implementation

**Tivrex** (tivrex.app) is the first consumer-facing application built on ZeroTX architecture. It is an AI session grading and drift detection tool. Every session processed by Tivrex passes the Zero-Transmission Test — no conversation content touches Tivrex's servers. The architecture is verifiable by any developer in under two minutes.

---

## License

The standards are open. Use them, build on them, implement them.
Specific implementations (software, products) built on these standards are proprietary to their respective authors.

---

*© 2026 Contrail Equity Strategies LLC — Springfield, Missouri*
*Author: Anthony Cyle Dixon*
