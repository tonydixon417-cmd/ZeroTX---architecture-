# AI Type Rating Framework (ATRF): A Proposed Certification Standard for AI Operators

**Author:** Anthony C. Dixon  
**Version:** 1.0  
**Date:** May 15, 2026  
**Status:** Defensive Publication — Prior Art Established  
**Repository:** https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

---

## Abstract

A pilot certified to fly a **Cessna 172** — a single-engine, four-seat training aircraft — is not authorized to fly a **Boeing 747**. The aircraft are both airplanes. The consequences of error are not comparable. The **Federal Aviation Administration (FAA)** resolves this through the type rating system: a certification specific to aircraft category, class, and type, with demonstrated proficiency requirements that scale with the consequence envelope of the aircraft (14 CFR Part 61).

No equivalent system exists for AI operators. A person with no training in AI behavior, failure modes, or accountability obligations is authorized to deploy enterprise AI systems affecting thousands of users, make consequential decisions based on AI output, and hold the title of AI oversight authority — with no demonstrated proficiency, no recurrency requirement, and no certification specific to the class of system they are operating.

This paper proposes the **AI Type Rating Framework (ATRF)** — a three-tier certification standard for AI operators that scales certification requirements with the consequence envelope of the AI system being operated. The framework establishes what operators must know, how proficiency is demonstrated, and why certification must be recurrent in a field where the aircraft keeps changing.

---

## 1. The Consequence Gap

A **Cessna 150** — a two-seat trainer produced from 1959 through 1977 — cruises at approximately 90 knots and carries 38 gallons of fuel. If a student pilot makes a serious error, the potential harm is severe but limited in scale.

A **Boeing 747-400** carries up to 524 passengers, 57,285 gallons of fuel, and operates at speeds exceeding 500 knots at 35,000 feet. The same error that produces a survivable outcome in a **Cessna 150** produces a catastrophic outcome in a **747**.

The **Federal Aviation Administration** does not pretend this difference does not exist. It encodes the difference into law. The **Cessna 150** requires a student pilot certificate to fly dual, a private pilot certificate to fly solo. The **747** requires an **Airline Transport Pilot (ATP)** certificate, a specific type rating for the aircraft, and demonstrated proficiency in a full-motion simulator.

The difference is not punitive. It is calibrated to consequence.

AI systems exist on an analogous spectrum. A consumer chatbot that helps a user draft a birthday message operates in a low-consequence envelope. An AI system deployed to assist in clinical diagnosis, legal judgment, financial portfolio management, or infrastructure operations is the **747** equivalent. The potential harm from operator error is not comparable. The certification requirements should not be either.

---

## 2. The Three-Tier Framework

### Tier 1 — Casual User Certification (Student Pilot Equivalent)

**Who this applies to:** Any individual using an AI system for personal, non-consequential purposes.

**What is required:** Informed acknowledgment of operating context. The **AI Preflight Briefing Standard (APBS)** (Dixon, 2026) at session initiation constitutes Tier 1 certification for casual users. The user understands:

- What the system can and cannot reliably do
- That the output is AI-generated and requires verification in consequential domains
- What the system will and will not do

**How it is delivered:** Baked into the onboarding experience. The user does not complete a course. They receive a briefing. The briefing is the certification for this tier.

**Consequence envelope:** Low. The user is operating a **Cessna 150** equivalent. The scale of potential harm is limited.

**Recurrency:** Session-level. Each **APBS**-compliant session initiation resets the Tier 1 acknowledgment for that interaction.

---

### Tier 2 — Intermediate Operator Certification (Private Pilot Equivalent)

**Who this applies to:** Professionals using AI systems in domain-specific work — legal research, medical information synthesis, financial analysis, content production at scale, enterprise operations support.

**What is required:** Completion of a structured competency curriculum covering:

1. **AI Failure Mode Awareness** — What drift types exist. How **Confidence Inflation (Type 6)** and **Unwarranted Certainty (Type 9)** manifest per the **AI Drift Taxonomy** (Dixon, 2026). How to recognize when output is outside reliable boundaries.

2. **Loop Recognition** — The four loop types from the **Loop Detector** framework (Dixon, 2026): **Confirmation Loop**, **Dependency Loop**, **Scope Creep Loop**, and **Mode Confusion Loop**. How each develops. How to interrupt.

3. **Output Verification Protocol** — Domain-specific standards for verifying AI output before reliance. What independent verification looks like in the operator's professional context.

4. **Incident Recognition and Reporting** — When something has gone wrong. How to document it. Who to notify.

**How it is delivered:** Scenario-based. Not engineering. Not code. Operational awareness — how the system behaves, not how it is built. Equivalent to a private pilot written exam followed by a practical check ride.

**Consequence envelope:** Moderate. The operator is using AI output to inform professional decisions. Errors affect their clients, patients, or organization.

**Recurrency:** Annual. The curriculum is reviewed and updated as new failure modes are identified and documented.

---

### Tier 3 — CAAO Certification (Airline Transport Pilot / Type Rating Equivalent)

**Who this applies to:** The **Chief AI Accountability Officer (CAAO)** — the designated accountable individual responsible for AI deployment, operation, and incident response within an organization (Dixon, 2026).

**What is required:** Full type rating for the class of AI system being deployed. This includes:

1. **Complete Drift Taxonomy Proficiency** — All nine drift types (Dixon, 2026). Recognition, documentation, and escalation protocol for each.

2. **AIBB Implementation Competency** — Full working knowledge of the **AI Black Box Standard (AIBB)** four-component logging architecture (Dixon, 2026). Ability to review and interpret logs. Ability to conduct post-incident analysis from log data.

3. **Loop Detector Operational Proficiency** — All four loop types. Diagnostic signatures for each. Intervention protocol for each.

4. **Covenant Warning System Administration** — Ethical envelope definition, tier configuration, escalation procedures, refusal documentation, and recurrency scheduling (Dixon, 2026).

5. **AI Preflight Briefing Standard Administration** — Briefing template development, user tier assignment, session-start logging review.

6. **Incident Command** — When a **Tier 3 Warning** event occurs: how to contain, document, investigate, and report. Who is notified. What the record must show.

7. **Regulatory Awareness** — Current status of the **European Union AI Act** (Regulation (EU) 2024/1689), **NIST AI Risk Management Framework (NIST AI 100-1)**, and applicable domestic regulation. How organizational deployment maps to compliance obligations.

**How it is delivered:** Structured examination followed by scenario-based assessment. Equivalent to an **Airline Transport Pilot** written exam, an oral examination, and a full-motion simulator check ride in the specific aircraft type. The check ride tests under pressure — not whether the candidate knows the procedures, but whether they can execute them when something is going wrong.

**Consequence envelope:** Maximum. The **CAAO** holds accountability for AI systems affecting the entire organization and its stakeholders.

**Recurrency:** Annual at minimum. Major system version changes require an updated type rating review.

---

## 3. Updatable Accountability: The Recurrency Principle

The most important structural feature of the **AI Type Rating Framework** is recurrency — and the reason recurrency is required is not administrative. It is architectural.

Aircraft evolve. The **Boeing 737 MAX** crisis demonstrated that a new variant of a familiar aircraft could introduce failure modes invisible to crews trained on earlier versions. The **FAA's** response was mandatory updated type rating training for all **737 MAX** operators. The credential was not permanent. The aircraft had changed. The certification had to change with it.

AI systems are evolving faster than any aircraft program in history. New capabilities emerge. New failure modes are discovered. New regulatory frameworks take effect. A **CAAO** certified in January may be operating a materially different system by December.

**Updatable Accountability** is the principle that:

1. Certification standards must be versioned and datestamped
2. The curriculum must be reviewed and updated at defined intervals
3. Certified operators must complete recurrency training at those intervals
4. The recurrency record is part of the operator's accountability trail
5. A credential that has lapsed is not a current credential — regardless of what the operator remembers from original certification

This is not bureaucracy. This is the recognition that accountability for a changing system requires accountability standards that change with it.

---

## 4. The Type Rating Does Not Replace Domain Expertise

A **Boeing 747** type rating does not make a pilot a better aerodynamicist. It does not require them to understand jet engine thermodynamics at an engineering level. It requires them to understand how to operate this aircraft, in this envelope, when things go as planned — and when they do not.

The **AI Type Rating Framework** makes the same distinction. **CAAO** certification does not require a computer science degree. It does not require knowledge of transformer architecture, training data curation, or model evaluation methodology.

It requires operational competency: knowing how the system behaves, where its limits are, what the failure signatures look like, how to respond when something goes wrong, and how to document what happened.

The goal is not to produce AI engineers. The goal is to produce accountable operators — people who understand the machine they are responsible for well enough to catch what it gets wrong, respond when it fails, and answer for the decisions made in its name.

---

## 5. Relationship to Existing Standards

The **AI Type Rating Framework** is designed to operate within the broader accountability ecosystem:

- **AI Black Box Standard (AIBB) v2.4** (Dixon, 2026) — The logging infrastructure that makes operator accountability auditable
- **Loop Detector v1.3** (Dixon, 2026) — The failure mode taxonomy forming the core curriculum for Tier 2 and Tier 3 certification
- **Covenant Warning System v1.0** (Dixon, 2026) — The alerting architecture that **CAAO**-certified operators are responsible for configuring and monitoring
- **AI Preflight Briefing Standard v1.0** (Dixon, 2026) — The session-initiation standard that constitutes Tier 1 certification for casual users
- **NIST AI RMF 1.0** (NIST, 2023) — The voluntary risk management framework to which Tier 3 certification maps governance functions
- **EU AI Act** (European Parliament, 2024) — The regulatory framework to which Tier 3 regulatory literacy maps compliance obligations

---

## 6. Conclusion

Nobody puts a pilot in the left seat of a **Boeing 747** because they once flew a **Cessna**. The consequence gap is too large. The failure modes are too different. The accountability obligation is too significant.

We are putting the equivalent of untrained operators in the left seat of consequential AI systems every day — and calling it democratization. It is not democratization. It is the absence of a standard.

The **AI Type Rating Framework** does not restrict access to AI. It calibrates accountability to consequence. The **Cessna 150** equivalent remains accessible to anyone willing to receive a briefing. The **747** equivalent requires demonstrated proficiency — because the people affected by that system's output deserve an accountable operator.

The type rating does not prevent flight. It makes flight accountable.

---

## References

1. Federal Aviation Administration. (2023). *14 CFR Part 61: Certification of pilots, flight instructors, and ground instructors.* Electronic Code of Federal Regulations. https://www.ecfr.gov/current/title-14/chapter-I/subchapter-D/part-61

2. Federal Aviation Administration. (2022). *Advisory Circular AC 61-138: Airline Transport Pilot Certification Training Program.* U.S. Department of Transportation. https://www.faa.gov/regulations_policies/advisory_circulars/index.cfm/go/document.information/documentID/1034085

3. National Institute of Standards and Technology. (2023). *Artificial Intelligence Risk Management Framework (AI RMF 1.0).* NIST AI 100-1. U.S. Department of Commerce. https://doi.org/10.6028/NIST.AI.100-1

4. European Parliament. (2024). *Regulation (EU) 2024/1689 of the European Parliament and of the Council laying down harmonised rules on artificial intelligence (Artificial Intelligence Act).* Official Journal of the European Union. (High-risk AI system requirements, Chapter 3, Articles 9–16.)

5. Dixon, A. C. (2026). *AI Black Box Standard (AIBB) v2.4.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

6. Dixon, A. C. (2026). *The Loop Detector v1.3.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

7. Dixon, A. C. (2026). *Covenant Warning System (CWS) v1.0.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

8. Dixon, A. C. (2026). *AI Preflight Briefing Standard (APBS) v1.0.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

9. Dixon, A. C. (2026). *Chief AI Accountability Officer (CAAO) Job Description Template v1.0.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

---

*This document is a defensive publication establishing prior art for the AI Type Rating Framework (ATRF). All concepts, terminology, and proposed standards contained herein are the original intellectual work of Anthony C. Dixon / Contrail Equity Strategies LLC, May 2026. All rights reserved.*
