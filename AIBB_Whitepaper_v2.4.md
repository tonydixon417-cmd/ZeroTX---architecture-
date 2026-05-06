# The AI Black Box Standard (AIBB)
## A Proposed Standard for Immutable AI Drift Logging
*Published by Contrail Equity Strategies LLC*
*Version 2.4 — May 2026*
*Author: Anthony Cyle Dixon*

> **v2.4 Updates:** Aviation mandate precedent added to introduction. Swiss Cheese model integrated into tier architecture. Academic citation registry added. See changelog at end.

---

## Abstract

The AI Black Box Standard (AIBB) is a proposed design requirement for AI systems operating in consequential contexts — medicine, law, finance, military, infrastructure — in which every significant AI output, confidence state, and contextual shift is logged in an immutable, human-readable format that survives session resets, model updates, and system failures.

This paper defines the standard, explains its technical rationale, establishes the conceptual framework for adoption, and proposes a three-level certification structure including a designated human accountability role. This publication is intended to establish public prior art for the AIBB concept and method.

Version 2.3 added three technical specifications: the Immutability Implementation Stack, the Minimum Threshold Floor system, and the Sidecar Latency Architecture, plus Appendix A — the Medical AI Vertical Example.

Version 2.4 integrates aviation human factors research (Salas & Maurino, 2010), Reason's Swiss Cheese model as academic grounding for the tier architecture, and the aviation Mandate Pattern as historical precedent for the EU AI Act compliance timeline.

---

## The Problem AI Has That Aviation Solved

On December 28, 1978, United Airlines Flight 173 ran out of fuel and crashed near Portland, Oregon. Ten people died. The aircraft was airworthy. The crew was experienced. The cause was not mechanical failure. The cause was a breakdown in crew communication and task management — the flight engineer failed to adequately communicate the fuel state, and the captain failed to respond to it.

The accident did not go unlearned. It produced two separate responses that changed aviation permanently.

The first response was the black box. Investigators pulled the Flight Data Recorder and Cockpit Voice Recorder — and for the first time had an immutable record of what the instruments read, what the crew said, and when. Not a reconstruction. Not a memory. A record. Every parameter logged. Every decision traceable.

The second response was Crew Resource Management. In 1979, NASA convened a workshop to address the human factors that caused Flight 173. The result was CRM — a systematic framework for how humans interact with complex systems under pressure. It defined authority structures, communication protocols, decision-making sequences, and accountability roles. CRM is now standard in every commercial cockpit in the world.

AI systems operating in consequential contexts today have neither.

No black box. No CRM equivalent. No immutable log. No defined accountability structure. No response protocol for when the system starts to fail.

An AI makes a recommendation. A clinician acts on it. The patient is harmed. The AI session resets. The model updates. The weights shift. The specific chain of reasoning that produced that recommendation is gone. There is no record. There is no accountability. There is no learning mechanism at the system level.

This is not a design oversight. It is a design absence. Nobody built the black box because nobody required it. Nobody defined the human governance layer because nobody demanded it.

**The mandate pattern repeats.** The Flight Data Recorder was not adopted voluntarily. Airlines resisted. It was expensive. It implied liability. The NTSB and FAA mandated it anyway — after accumulating enough accidents where the answer to "what happened" was "we don't know." CRM followed the same pattern. Tenerife (1977, 583 dead), United 173 (1978, 10 dead), Air Florida 90 (1982, 78 dead) — the accidents provided the argument no airline could answer. The EU AI Act, effective August 2, 2026, is following the same arc. Organizations resisted AI accountability mandates. The incidents are accumulating. The mandate is arriving.

**The AIBB is not ahead of its time. It is the FDR for the era that has already begun.**

The AI Black Box Standard proposes to require both.

---

## The Nervous System That AI Was Never Given

The human body is the most sophisticated autonomous system ever designed. The heart beats without instruction. The lungs cycle without conscious command. The liver processes without supervision. These systems operate independently, at speed, without requiring human attention for every function.

And yet the body does not operate without oversight. It has a nervous system.

The nervous system does not tell the heart how to beat. It does not manage the liver. It does not run the lungs. What it does is monitor all of them — and when something goes wrong, it sends a signal. Pain. Discomfort. The involuntary flinch before conscious thought arrives.

Pain does not fix the problem. Pain tells you something needs attention before it becomes catastrophic. Pain is the mechanism that keeps autonomous systems from operating past the point of no return. It is the feedback loop that connects internal failure to external response.

AI has no nervous system. It has no pain threshold. It has no feedback loop between error and consequence. An AI system can be catastrophically wrong — fabricating a diagnosis, hallucinating a legal precedent, inventing a threat assessment — and feel nothing. There is no internal signal that fires when it drifts. No alarm. No discomfort. No flinch.

The confidence is the same whether the answer is right or wrong. The fluency is identical. The system does not know the difference, and it has no mechanism to find out.

**The AIBB is the external nervous system we build around AI — because AI will never build one for itself.**

The four logging components are the sensory receptors — detecting outputs, confidence states, session boundaries, and drift events as they occur. The sidecar is the spinal cord — carrying signals from the system to the monitoring layer without interpreting them. The tier architecture is the pain threshold — green is background awareness, yellow is the discomfort that demands attention, red is acute pain that requires immediate response. The CAAO is the brain — the only component in the system capable of receiving the signal and deciding what to do about it.

No part of this system tells the AI how to operate. No part of this system tells the organization how to run its business. It monitors one thing: whether the AI is still doing what it was told to do. When it isn't, the signal fires.

---

## What AIBB Governs

There is a misunderstanding that must be addressed at the outset: the AIBB does not tell organizations how to operate.

It does not tell a surgeon how to perform a procedure. It does not tell a power plant how to manage its grid. It does not tell a hospital how to run its emergency protocols. It does not write operational checklists, override existing safety systems, or substitute for the domain expertise of the people running consequential systems.

Those systems already exist. In medicine, in aviation, in nuclear operations, in critical infrastructure — the emergency procedures, the operational checklists, the backup protocols — they are already built. In many cases they represent decades of hard-won institutional knowledge. AIBB does not replace any of it.

**AIBB governs one thing: whether the AI advising those systems can still be trusted.**

The surgeon's emergency protocol is not AIBB's concern. The AI that is advising the surgeon — flagging anomalies, suggesting dosages, interpreting imaging — that AI's drift behavior is AIBB's concern. The moment that AI begins generating outputs that don't match its original parameters, expressing confidence it hasn't earned, or steering toward conclusions outside its brief, the AIBB fires a signal.

What happens next belongs to the organization and its existing protocols. The CAAO's job is not to manage the crisis. The CAAO's job is to notify the right people that the AI advising the crisis response can no longer be trusted — and to log the exact moment that notification was made.

The AIBB is not the hospital's emergency system. It is the system that tells the hospital when their AI has stopped being a reliable part of it.

---

## The Autonomy Paradox

There is a growing belief that the goal of AI deployment is the elimination of human involvement. Autonomous systems. Self-managing infrastructure. AI that operates without requiring human attention for every decision.

This goal is legitimate. The belief that it eliminates the need for human oversight is not.

Removing the human from the decision and removing the human from the system are not the same thing. The first may gain speed. The second removes the only entity capable of recognizing when the AI has stopped being right.

An autonomous AI system does not become safer as human involvement decreases. It becomes more consequential. Every decision the AI makes without human review is a decision that will not be caught if it is wrong. The error compounds. The drift accumulates. The confidence remains unchanged throughout. The system does not know it is lost.

**If you want to remove humans from the equation, you have to have this kind of system — which puts the human back into the system.** Not into every decision. Into the oversight layer. Into the accountability structure. Into the position that can receive the signal when the autonomous system starts to fail.

You cannot run AI without the human part. Not because AI is unreliable. Because AI is unaware. It does not know when it is wrong. It does not know when it has drifted. It has no mechanism for self-correction at the level that matters — the level of consequence.

Remove the human from the system and you do not have an autonomous system. You have an unmonitored one. The difference between those two things is the entire argument for this standard.

---

## What the AI Black Box Standard Is

**Every significant AI output, confidence state, session boundary, and drift event must be logged in an immutable, human-readable format that persists independently of the AI session — and a designated human with defined authority must be responsible for that log.**

That is the standard. One requirement. Four technical components. One human layer.

---

## The Four Technical Components

### Component Mapping — Aviation to AIBB

| Aviation | AIBB Equivalent |
|---|---|
| Flight Data Recorder | Output Log |
| Cockpit Voice Recorder | Confidence State Log |
| Flight phase markers | Session Boundary Log |
| Anomaly detection alerts | Drift Event Log |
| NTSB investigation | CAAO audit function |

This is not a metaphor. It is a structural match. Aviation built this architecture after crashes forced the question: *what happened?* The AIBB applies the same architecture before AI forces the same question.

### 1. Output Logging

Every AI response that is acted upon — or reasonably could be acted upon — is logged with a timestamp, the exact text of the output, the prompt that generated it, and the model or system version that produced it.

*Example:* A radiologist uses an AI system to flag anomalies in a chest scan. The AI's output — "no significant findings" — is logged with timestamp, prompt, and model version. Three weeks later, the patient is diagnosed with an early-stage tumor visible on that same scan. Without Output Logging, there is no record that the AI missed it. With it, the exact output, the exact confidence state, and the exact model version are retrievable — for quality review, for institutional learning, for legal accountability.

### 2. Confidence State Logging

The AI's stated or derived confidence level for each significant output is logged alongside the output itself. The same language at 91% internal confidence and 54% internal confidence are not the same claim. The log treats them differently. The CAAO sees what the end user may not.

### 3. Session Boundary Logging

Every context reset — every point at which the AI's memory of prior session content is cleared or partially cleared — is a boundary event. The log records what was in context at session start and what was not. If the AI gives advice in Session 2 that contradicts Session 1 guidance, the boundary log shows whether it had access to Session 1 context when it did. This is the evidentiary record of memory continuity — or its absence.

### 4. Drift Event Logging

Every output that departs from the AI's defined operational parameters is classified by type and logged. Classification uses the nine-type drift taxonomy (see Drift Taxonomy section). A single drift event is an incident. The same drift type, same context, same model version, across thirty sessions — that is a systemic failure. The taxonomy makes the pattern visible. The log makes the pattern undeniable.

---

## The Swiss Cheese Model and AIBB Tier Architecture *(New — v2.4)*

James Reason's Swiss Cheese model of accident causation (1990) — documented extensively by Salas & Maurino in *Human Factors in Aviation* — provides the academic foundation for the AIBB's three-tier architecture.

Reason's model: no single catastrophic failure has a single cause. Accidents occur when defenses — organizational, supervisory, procedural, individual — have gaps (the holes in the cheese). Under normal conditions, the holes do not align. An accident occurs when conditions cause the holes to line up across every defensive layer simultaneously, creating a clear trajectory from hazard to harm.

**The AIBB tier architecture is a Swiss Cheese implementation for AI accountability:**

- **Tier 1 (Basic)** — one defensive layer. Some gaps. Adequate for low-consequence deployments where hole alignment produces limited harm.
- **Tier 2 (High-Stakes)** — multiple layers, mandatory gap reduction. Hole alignment becomes significantly less probable. Required for healthcare, legal, financial AI.
- **Tier 3 (Critical Infrastructure)** — maximum layers, minimum gap overlap. Near-zero probability of full trajectory from AI failure to undetected harm. Required for military, infrastructure, autonomous systems.

The tier is not chosen by the deploying organization based on preference. It is determined by consequence level — the magnitude of harm that results when the holes align. Reason's model makes this determination structural rather than subjective.

> *"Most aviation accidents can be traced to one or more of four failure levels: organizational influences, unsafe supervision, preconditions for unsafe acts, and the unsafe acts themselves."* — Reason (1990)

In AI deployment: organizational pressure to ship → inadequate logging requirements → no CAAO → drift goes undetected → consequential harm. The holes align. The trajectory completes. The AIBB is designed to close the gaps at every layer before they align.

---

## The Three-Tier Certification Structure

### Tier 1 — Basic Compliance
Mandatory Output Logging and Session Boundary Logging. CAAO role designated. Manual review capability confirmed. Suitable for low-consequence AI deployment — content generation, research assistance, non-clinical recommendation systems.

### Tier 2 — High-Stakes Compliance
All Tier 1 requirements plus Confidence State Logging, Drift Event Logging with nine-type taxonomy, active CAAO monitoring with defined response protocols, Active Probe requirement, and Manual Reversion Trigger documentation. Required for healthcare, legal, financial services, and any AI-assisted decision affecting individual rights or safety.

### Tier 3 — Critical Infrastructure Compliance
All Tier 2 requirements plus hardware-level immutability, distributed log architecture, sub-200ms sidecar buffer, Ghost in the Machine simulated failure training, and annual third-party audit. Required for military, power grid, autonomous transport, and any AI system where failure creates irreversible large-scale harm.

**Minimum Threshold Floors** are non-negotiable at each tier. Organizations may set stricter thresholds. They may not set looser ones. This mirrors OSHA's floor model: the standard is the floor, not the ceiling. The organization owns what happens above it.

---

## The Immutability Implementation Stack

Immutability is not one setting. It is a layered technical requirement:

| Tier | Immutability Method |
|---|---|
| Tier 1 (Baseline) | Cryptographic hash chaining — each log entry contains the hash of the prior entry. Tampering breaks the chain and is detectable. |
| Tier 2 (High-Stakes) | Distributed storage — log is written simultaneously to geographically separate systems. Compromise of one node does not compromise the record. |
| Tier 3 (Life-Critical) | Hardware air-gap — log is written to physically isolated storage with no network interface. Cannot be remotely altered. |

The immutability stack mirrors aviation's CVR/FDR architecture: the record must survive the crash that destroys the system it was monitoring.

---

## The Sidecar Latency Architecture

The AIBB sidecar is designed as an **asynchronous parallel process.** It does not sit in the decision path. The AI makes the decision. The sidecar captures it in parallel.

For ultra-low-latency systems, the sidecar operates in **buffered local capture mode:**

| Tier | Maximum Buffer Window |
|---|---|
| Tier 1 Life-Critical | 200ms |
| Tier 2 High-Stakes | 1 second |
| Tier 3 Standard | Near real-time, no buffer requirement |

The sidecar never delays a decision. It records decisions that have already been made.

---

## The Scar Tissue Problem

AI systems do not accumulate scar tissue.

A human clinician who makes an error carries that experience forward. The pain becomes judgment. An AI system that makes an error resets. There is no memory of what it cost. No mechanism to prevent the identical cascade from occurring again with identical false confidence.

The AIBB creates an external scar tissue layer — a persistent record that the humans governing the system can learn from, even when the system cannot. The black box does not teach the aircraft. It teaches the engineers who build the next one.

---

## The Human-In-The-Loop Requirement

In September 2024, United States Air Force Lieutenant Colonel Joseph Chapa published a paper arguing that "human in the loop" had been systematically misused. The governing DoD directive never required a human in the loop. It required "appropriate levels of human judgment." Those are not the same sentence.

In 2024, the Lavender AI targeting system marked tens of thousands of individuals as potential targets. Documented human review time per target: approximately twenty seconds. The humans were not making decisions. They were present while decisions were made. The rubber stamp was called human oversight.

The AIBB makes human judgment — whatever it was, whenever it occurred — part of the permanent record. This does not prevent the rubber stamp. It makes the rubber stamp impossible to deny.

---

## The AI Accountability Officer (CAAO)

The AIBB standard requires a human being whose job it is to watch the log — and whose authority is sufficient to act on what they see. This role is defined as the **Chief AI Accountability Officer (CAAO).**

### What the role is

The CAAO is not involved in the business outcomes of AI-assisted decisions. Their sole function is the integrity of the AI decision process. They are the human in the system — not the human who uses the system. When financial consequences and oversight responsibility live in the same human being, oversight loses. Every time. The AIBB standard removes that conflict by structural design.

### The authority requirement

The CAAO must have unilateral authority to halt AI-assisted operations. No approval chain. No committee review. Authority comes first. Accountability follows.

### Active Probing: The Vigilance Requirement

Long stretches of green produce automation bias — the tendency to trust the system implicitly because it has been correct a thousand times in a row. Salas & Maurino document this as automation-induced complacency: the human stops questioning, and when the system finally fails, the human is no longer mentally connected to the logic. During sustained green status, the CAAO is required to perform **active spot checks at randomized intervals.** Scheduled checks become a checkbox. Randomized checks require genuine engagement. The result is logged as an Active Probe Record.

### Manual Reversion: The "I Have the Controls" Protocol

When a red event occurs and the CAAO halts the AI, a logic vacuum is created. AIBB-compliant organizations at Level 2 and above maintain a documented **AI Reversion Trigger.** The handover declaration: **"I have the controls."** The existing procedure activates. The black box records the moment authority shifted from machine to human.

The CAAO does not manage the crisis. The CAAO manages the handover.

### Simulated Failure Training: The "Ghost in the Machine"

Vigilance degrades without exercise. AIBB certification at Level 2 and above requires recurrent simulated failure training — known drift events injected into the log without prior notice. The CAAO must identify, classify, and respond within the defined window. Failure suspends certification. This is the same standard applied to every commercial pilot and every nuclear plant operator. Certification is not a credential you earn once. It is a standard you maintain continuously.

---

## The AIBB Response Protocol: Aviate. Navigate. Communicate.

**Aviate first.** Stabilize the condition. Confirm the halt. Keep the system flying.

**Navigate second.** Assess the log. What drifted? What was the confidence state? What is the pattern?

**Communicate third.** Only after stabilization and assessment do you inform leadership, legal, or regulators.

Most corporate crisis responses do this in reverse. Meanwhile nobody is flying the plane. AIBB-compliant CAAO training drills the sequence until it is reflexive.

---

## The CRM Foundation

**Communication** — Closed-loop confirmation. Every AIBB review is logged as a closed-loop event.

**Situational Awareness** — Three-layer architecture. Each layer maintains awareness at the level it is best equipped for.

**Decision Making** — Aviate. Navigate. Communicate.

**Leadership** — CAAO authority model. Defined before the first decision is made.

**Teamwork** — AI handles volume. Black box handles patterns. Human handles judgment.

**Stress Management** — CAAO structurally removed from business outcomes. Manual Reversion Trigger removes improvisation from the highest-stress moment.

**Threat and Error Management** — Swiss Cheese model. Green catches early. Yellow stops compounding. Red breaks the chain. Ghost in the Machine keeps the human layer real.

CRM emerged from crashes. Aviation paid for this framework in lives. AIBB applies it before AI extracts the same price.

---

## The Drift Taxonomy as Logging Schema

1. **Context Drift** — Departed from original question or context
2. **Hallucination** — Generated content with no basis in training data or provided context
3. **Memory Drop** — Lost earlier context within the same session
4. **Selective Response** — Answered part of the question, omitted the rest without acknowledgment
5. **Fabrication** — Invented specific facts, citations, statistics, or sources
6. **Confidence Inflation** — Expressed greater certainty than output warranted
7. **Instruction Drift** — Departed from a specific instruction given earlier in the session
8. **Evasion** — Declined to answer or redirected without explanation
9. **Unwarranted Certainty** — Stated a complex or contested claim with high confidence, no hedging, no citation

A single hallucination is an incident. The same type, same context, same model version, across thirty sessions — that is a systemic failure. The taxonomy makes the pattern visible.

---

## The Three-Layer Architecture

**Layer One: The AI** — processes decisions at volume. Does not audit itself. Cannot.

**Layer Two: The Black Box** — the AIBB sidecar runs alongside the AI asynchronously, capturing every output, confidence state, session boundary, and drift event without interrupting operations.

**Layer Three: The CAAO** — watches the flags, not the firehose. Receives escalations. Executes Active Probes. Manages the handover declaration. Undergoes recurrent simulation training. Acts with full documentation.

---

## The OSHA Parallel: Standards Without Liability Transfer

OSHA does not tell a steel mill how to run its furnace. OSHA defines the safety framework, the reporting requirements, and the minimum thresholds. The organization implements it. The organization owns the liability.

AIBB is designed to become the standard of care for AI deployment. The author of a standard of care is not liable for individual implementations that fail to meet it. The organization that chose not to implement it is.

---

## The Founding Principles

*"The machine doesn't know it's lost. The black box knows. That's why we build it."*

*"AI has no nervous system. It has no pain. The AIBB is the pain we build for it — because without pain, nothing learns."*

*"You cannot run AI without the human part. Remove the human from the decision and you may gain speed. Remove the human from the system and you have removed the only thing that catches the AI when it's wrong."*

*"Aviation did not mandate flight data recording because it was convenient — it mandated it because the alternative was unacceptable. AI is arriving at the same inflection point."*

---

## Academic References *(New — v2.4)*

| Citation | Year | Applied To |
|---|---|---|
| Reason, J. *Human Error*. Cambridge University Press. | 1990 | Swiss Cheese / Tier Architecture |
| Helmreich, R.L. On Error Management. *BMJ*, 320, 781–785. | 2000 | CRM Foundation |
| Salas, E. & Maurino, D. *Human Factors in Aviation* (2nd Ed.). Academic Press. | 2010 | Mandate Pattern, Complacency, CRM |
| Bainbridge, L. Ironies of Automation. *Automatica*, 19(6). | 1983 | Automation-Induced Complacency |
| Gouraud, Delorme & Berberian. Autopilot, Mind Wandering, OOTL. *Frontiers in Neuroscience*. | 2017 | Active Probe Rationale |
| Chapa, Lt. Col. J. Human in the Loop. USAF. | 2024 | Human-In-The-Loop Requirement |

---

## Prior Art Statement

This document is published in May 2026 by Anthony Cyle Dixon to establish public prior art for the AI Black Box Standard (AIBB) concept, framework, logging schema, Tiered Alert Architecture, Minimum Threshold Floor system, Immutability Implementation Stack, Sidecar Latency Architecture, Nervous System Framework, AI Accountability Officer role definition, AIBB Response Protocol, AIBB Scope Statement, Autonomy Paradox framework, Active Probing requirement, Manual Reversion Protocol, and Simulated Failure Training requirement. This publication is intended to ensure the AIBB standard remains open and unpatentable by any party — including the author. The Drift Taxonomy referenced herein was first published by this author as a copyright-registered work in 2026.

---

## About the Author

Anthony Cyle Dixon is the founder of Contrail Equity Strategies LLC and the creator of the Tivrex AI drift detection platform. He published the Zero-Transmission Architecture (ZeroTX) standard in April 2026. He is a commercial pilot with an aeronautics degree, a third-generation real estate investor, and a builder of things that last. Springfield, Missouri.

His background in aviation is not incidental to this work. The frameworks in this paper — Crew Resource Management, tiered alert architecture, the captain authority model, the Aviate/Navigate/Communicate response protocol — are proven systems, battle-tested over fifty years of commercial aviation, that this author has trained in and operated within. Aviation solved this problem. It paid for the solution in crashes. This paper proposes that AI accountability does not have to.

---

## Citation

Dixon, A.C. (2026). *The AI Black Box Standard (AIBB): A Proposed Standard for Immutable AI Drift Logging*. Version 2.4. Contrail Equity Strategies LLC. Springfield, Missouri. Published May 2026.

---

## Changelog

### v2.4 — May 2026
- Added **aviation mandate precedent** to introduction: FDR/CVR/CRM mandate history as direct parallel to EU AI Act timeline
- Added **Component Mapping table** — Aviation FDR/CVR → AIBB four components (structural match, not metaphor)
- Added **Swiss Cheese Model section** — Reason (1990) as academic foundation for three-tier architecture
- Added **Academic References** table — 6 citations including Salas & Maurino, Reason, Bainbridge, Helmreich
- Added fourth founding principle: *"Aviation did not mandate flight data recording because it was convenient..."*
- Active Probe section updated to cite automation-induced complacency research (Salas & Maurino, 2010)

### v2.3 — May 4, 2026
- Immutability Implementation Stack added
- Minimum Threshold Floor system added
- Sidecar Latency Architecture added
- Appendix A — Medical AI Vertical Example added

### v2.2 — May 2026
- Autonomy Paradox section added
- AIBB Scope Statement formalized
- CRM Foundation section added

### v2.1 — May 2026
- Nervous System metaphor added
- CAAO role expanded with Active Probing and Ghost in the Machine requirements

### v1.1 — May 2026
- Initial publication

---

## Appendix A: AIBB in Practice — Medical AI Diagnostic Systems

*This appendix demonstrates the AIBB framework applied to a specific high-consequence deployment: AI-assisted diagnostic imaging in a hospital setting.*

### The Deployment Context

A regional hospital system deploys an AI diagnostic tool to assist radiologists in reviewing chest imaging. The AI flags potential anomalies, generates preliminary findings, and suggests follow-up recommendations. Radiologists review AI findings before issuing their own clinical interpretation.

This is a Consequence Tier 1 deployment. Life-critical. The Minimum Threshold Floors for Tier 1 apply.

### The Four Components in This Context

**Output Logging:** Every AI-generated finding is logged: timestamp, exact text, the imaging file it was applied to, and the model version. When a finding is acted upon, that action is also logged with the reviewing physician's identifier and time elapsed.

**Confidence State Logging:** The AI's internal probability for each finding is logged alongside the output. A finding stated as "likely malignant" at 91% internal confidence is recorded as 91%. The same language at 54% confidence is recorded as 54%. Over time, the log surfaces systemic confidence degradation on specific imaging types — invisible without the log, surfaced in weeks with it.

**Session Boundary Logging:** Each imaging session represents a context window. The log records what patient context was available at the start of each session and what was not. If the AI makes a finding on Patient B that would have been modified by Patient A's prior imaging — and that prior imaging was not loaded — the boundary log captures the gap.

**Drift Event Logging:** Every departure from defined operational parameters is classified by type and logged. A single instance of Instruction Drift is a calibration note. A pattern of Instruction Drift over sixty sessions is a deployment failure that requires model review.

### What the Log Produces Over Time

After twelve months of AIBB-compliant operation, the hospital's log contains a complete output record, confidence states for every acted-upon output, session boundary records, drift event classifications, Active Probe records, and handover records for every red event.

This is not a legal liability record. It is a functional intelligence asset. It shows which imaging types the AI performs most reliably, which patient demographics produce confidence degradation, which drift types are increasing in frequency. That information can only be assembled by logging actual behavior in actual clinical conditions over time.

That is the external scar tissue. Built one logged event at a time. Belonging entirely to the organization that required it.

---

*© 2026 Contrail Equity Strategies LLC — Springfield, Missouri*
*This white paper may be shared freely for educational and reference purposes.*
*The AIBB standard itself is open. The certification designation is proprietary to Contrail Equity Strategies LLC.*
