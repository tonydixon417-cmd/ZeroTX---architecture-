# The Missing CVR: Why AI Audit Standards Are Incomplete By Design

**A Companion Paper to the AI Black Box Standard (AIBB)**  
Published by Contrail Equity Strategies LLC  
Version 1.2 — May 2026  
Author: Anthony Cyle Dixon

---

## Abstract

The aviation black box is not a single device. It is two. The Flight Data Recorder (FDR) captures what the aircraft did — altitude, speed, heading, control surface position, engine performance. The Cockpit Voice Recorder (CVR) captures what the crew said — commands, callouts, alarms, the human conversation that preceded every action the aircraft took. Both recorders are mandatory. Neither is optional. The reason is simple: one without the other is an incomplete record.

Current AI audit proposals — including early AIBB implementations — capture the AI output side of the interaction. They log what the AI said, what confidence state it expressed, and where drift occurred in its responses. What they do not capture is the human prompt chain: the questions asked, the framing applied, the leading language that may have steered the AI toward the output being audited. This is the Missing CVR.

An AI audit standard without prompt logging has a structural blind spot built in by design. It can identify AI drift. It cannot determine whether the drift was caused by the AI or invited by the human. It can exonerate the machine while obscuring the operator's role entirely.

This paper defines the problem, establishes the CVR parallel, proposes the minimum requirement for a complete AI session record, and identifies the ZeroTX on-device architecture as the first implementation capable of capturing both sides without transmission risk.

---

## Part One: The Two-Recorder Architecture

On July 19, 1989, United Airlines Flight 232 suffered a catastrophic engine failure that destroyed all three hydraulic systems. Captain Al Haynes and his crew performed one of the most remarkable feats of airmanship in aviation history — executing an emergency landing at Sioux City, Iowa that saved 185 of 296 people on board.

The NTSB investigation had access to both recorders. The FDR showed exactly what the aircraft did — every control input, every speed change, the precise moment hydraulic pressure dropped to zero. The CVR captured what the crew said — the calm decision-making, the resource management, the communication that made the controlled crash possible.

Neither recorder alone told the full story. The FDR without the CVR showed a plane behaving erratically with no explanation. The CVR without the FDR showed a crew talking without knowing what effect their actions had. Together, they produced a complete reconstruction that became the foundation for new training standards that are credited with saving thousands of lives since.

The lesson is not that one recorder matters. The lesson is that the system-side record and the human-side record must exist together for the investigation to mean anything. AI audit standards that log only AI output are FDRs without CVRs.

---

## Part Two: The Prompt Is the Control Input

In aviation, the CVR captures what the crew told the aircraft to do. The FDR captures how the aircraft responded. In an AI session, the prompt is the control input. It shapes what the AI produces with the same directness that a yoke input shapes what the aircraft does.

An AI session that produces a hallucinated citation does not exist in isolation. It was preceded by a question. That question had framing. It may have been leading. It may have used language that activated a particular pattern in the model. It may have asked for certainty when none was available. It may have repeated a false premise that the AI confirmed rather than challenged.

Without the prompt chain, the audit can identify the hallucination but cannot determine its cause. Research on automation trust demonstrates that operators consistently accept automated outputs without independent verification — particularly when the output is delivered with high confidence and fluency. [3] The prompt chain is the only record that shows whether the operator provided a check or simply forwarded the output.

Was the AI drifting on its own trajectory? Or was it following a human down one? This distinction is not academic. It determines liability. It determines whether the failure was a model problem or an operator problem. An audit standard that cannot answer this question is not an accountability system. It is an output monitor with a compliance certificate attached.

---

## Part Three: The Blind Spot Is Structural

The reason current AI audit proposals lack prompt logging is not oversight. It is architecture. Most AI systems operate through APIs. The prompt goes in. The output comes out. The audit layer — if one exists — is typically attached to the output side because that is where the organization has access.

Capturing the prompt requires either client-side logging (a privacy concern), server-side interception (a transmission and storage liability), or user consent and submission (a compliance burden that most users ignore). Each approach creates a new problem in the act of solving the old one.

Sociologist Diane Vaughan documented the same pattern in her analysis of the Challenger disaster: organizations normalize the absence of a safety requirement by consistently operating without it until the gap becomes invisible. The missing CVR layer in current AI audit standards is not a gap organizations are aware of tolerating. It is a gap that has been normalized by deployment at scale before the standard was written. [1]

---

## Part Four: The ZeroTX Answer

The ZeroTX architecture was developed as a privacy-first AI session protocol with a specific design constraint: no data leaves the user's device. The session is conducted locally. The analysis is performed locally. The output — the Readback — is generated locally and stored locally.

This constraint, designed to address HIPAA compliance concerns, solves the Missing CVR problem as a structural byproduct. Because the full session — both the prompts and the AI responses — exists on the device where it was generated, there is no transmission liability in capturing the prompt chain. There is no server-side storage of sensitive user inputs. There is no privacy violation in logging the human side of the conversation because the log never leaves the device it was created on.

The ZeroTX session log, by design, is the complete record. FDR and CVR in one file. ZeroTX is the first AI session architecture that makes the complete record technically possible without creating a new compliance problem in the process. The Missing CVR is not missing in a ZeroTX session. It was captured from the first word.

---

## Part Five: The Minimum Standard

A complete AI session audit record must capture the following:

**The FDR Layer (AI Output Side — currently addressed by AIBB v2.4):**
- AI output log, timestamped
- Confidence state per output (Green / Yellow / Red)
- Drift event log with type classification
- Session boundary markers
- Platform fingerprint

**The CVR Layer (Human Input Side — currently absent from most standards):**
- Full prompt chain, timestamped
- Prompt framing indicators (leading language, false premises, certainty demands)
- Human confirmation or rejection of AI outputs
- Operator identity and role (where applicable)
- Session intent declaration

Neither layer alone constitutes a complete audit record. Both layers together constitute what the NTSB would recognize as an investigatable record — one from which a qualified investigator could reconstruct the full sequence of the session and assign causal weight to both the system and the operator.

---

## Part Six: The Liability Implication

The Missing CVR is not just a completeness problem. It is a liability architecture problem. An audit standard that captures only AI output creates a one-sided record. The AI can be found to have drifted. The operator cannot be found to have prompted the drift.

This imbalance concentrates liability — always on the system side, always away from the operator. Over time, operators who know the audit only captures AI output have no documented accountability for the prompts they submit. The AI becomes the legal backstop for every operator decision that was made through it.

Research on automation bias consistently finds that operators who trust automated systems without accountability mechanisms develop systematic over-reliance — not through negligence, but through the absence of feedback that their judgment is being bypassed. [2]

Accountability without the prompt chain is not accountability. It is a one-sided record with a compliance label.

---

## Part Seven: When the Pilot Leaves the Cockpit — The Synthetic Intelligence Problem

Every argument in this paper rests on a shared assumption: a human authored the prompt. The operator typed a question. The AI responded. The CVR logs what the human said. The FDR logs what the AI did. Both sides are human-initiated at the origin point.

Synthetic intelligence removes that assumption.

Synthetic intelligence — AI that sets its own goals, initiates its own tasks, and operates without a human prompt at each step — does not wait to be asked. It decides what to do next autonomously. The prompt chain, in an SI deployment, is generated internally by the system itself. No human typed it. No human reviewed it before the action was taken. No human signed off.

This is not a future scenario. Agentic AI systems are already operating in production environments — scheduling, executing, communicating, and transacting on behalf of organizations without per-action human review. The aviation equivalent is not a pilot who made a bad decision. It is an aircraft that decided on its own to change course, with the pilot unaware until the destination appeared on the horizon.

The Missing CVR problem escalates dramatically in this context.

In a human-prompted session, the CVR gap means the operator's influence on the AI's output is undocumented. The liability question is: who led whom? In a synthetic intelligence deployment, there is no human prompt to document. The liability question becomes: who authorized the system to act at all, and under what defined constraints?

The audit requirement does not shrink. It expands. An SI deployment requires documentation of:

- **The original mandate:** what the system was authorized to do, in writing, before deployment.
- **The constraint boundaries:** what the system was explicitly prohibited from doing.
- **Every autonomous decision node:** each point at which the system chose a path without human input.
- **Every action taken:** outputs, communications, transactions, and data accesses.
- **Every deviation from original mandate:** flagged, timestamped, and logged.

Without this record, SI deployments produce outcomes with no traceable chain of authorization. In high-stakes domains — healthcare, finance, legal, infrastructure — this is not an audit gap. It is a liability void.

The aviation parallel is precise. When automated flight systems began executing maneuvers without direct pilot input, the industry did not remove the black box. It expanded the recording requirements to capture automated system inputs alongside crew inputs — because the question "what happened" now required documenting what the automation decided, not just what the human commanded.

The same expansion is required for synthetic intelligence. The AIBB standard, applied to SI deployments, must capture the full autonomous decision chain — not as an optional compliance feature, but as the minimum record required to reconstruct what the system did and why.

A kill switch with no audit log is not a safety mechanism. It is a way to stop the aircraft and erase the recording simultaneously. The AIBB is the black box that must survive the crash — especially when no human was flying the plane.

---

## Conclusion

The aviation black box survived sixty years of crashes, investigations, and regulatory battles because it captures the complete record. Not half of it. Not the convenient half. Both sides — the machine and the human — logged together, immutably, in a format that survives the failure it was built to document.

AI audit standards that capture only AI output are half a black box. The Missing CVR is not a feature to add later. It is a structural requirement for any audit standard that claims to establish accountability. Without it, the investigation can identify what the AI said. It cannot determine why — and in high-stakes domains, why is the only question that matters.

The ZeroTX architecture provides the first technically viable path to capturing both layers without creating transmission liability. The AIBB standard provides the FDR layer. Together, they constitute a complete session record.

As synthetic intelligence removes the human from the prompt chain entirely, the stakes of this gap do not diminish. They compound. The missing piece has been named. The architecture exists. The standard is being written. The aircraft is beginning to fly itself.

---

## References

**Aviation & Accident Investigation**
- NTSB Aircraft Accident Report: United Airlines Flight 232, Sioux City, Iowa, July 19, 1989
- NTSB Aircraft Accident Report: United Airlines Flight 173, Portland, Oregon, December 28, 1978
- FAA Advisory Circular AC 120-51E: Crew Resource Management Training
- ICAO Annex 6: Operation of Aircraft, Part I — International Commercial Air Transport

**Academic Sources**

[1] Vaughan, Diane. (1996). *The Challenger Launch Decision: Risky Technology, Culture, and Deviance at NASA.* University of Chicago Press.

[2] Parasuraman, R. & Manzey, D. (2010). "Complacency and Bias in Human Use of Automation: An Attentional Integration." *Human Factors*, 52(3), 381–424.

[3] Skitka, L.J., Mosier, K., & Burdick, M. (1999). "Does Automation Bias Decision-Making?" *International Journal of Human-Computer Studies*, 51(5), 991–1006.

**Author's Prior Art Publications**
- Dixon, A.C. (2026). *The AI Black Box Standard (AIBB), Version 2.4.* Contrail Equity Strategies LLC.
- Dixon, A.C. (2026). *ZeroTX Architecture: Zero-Transmission AI Session Protocol.* Contrail Equity Strategies LLC.
- Dixon, A.C. (2026). *The Loop Detector: A Human Accountability Standard for AI-Assisted Decision Making, v1.3.* Contrail Equity Strategies LLC.

---

## Changelog

**v1.2 — May 18, 2026**
- Added Part Seven: When the Pilot Leaves the Cockpit — The Synthetic Intelligence Problem
- Addresses autonomous AI (SI) as the next escalation of the Missing CVR accountability gap
- Updated Conclusion to reflect SI escalation

**v1.1 — May 13, 2026**
- Added three academic citations inline (Vaughan, Parasuraman & Manzey, Skitka et al.)
- Expanded References section with structured academic registry

**v1.0 — May 2026**
- Initial publication

---

*This document is published to establish public prior art for the concept of dual-layer AI session logging (prompt chain + AI output) as a required component of AI accountability standards. All rights reserved. © 2026 Anthony Cyle Dixon / Contrail Equity Strategies LLC.*
