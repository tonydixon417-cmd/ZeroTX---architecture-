# AI Preflight Briefing Standard (APBS): A Proposed Framework for Informed Capability Disclosure at Session Initiation

**Author:** Anthony C. Dixon  
**Version:** 1.0  
**Date:** May 15, 2026  
**Status:** Defensive Publication — Prior Art Established  
**Repository:** https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

---

## Abstract

Every commercial airport in the United States broadcasts a continuous **Automatic Terminal Information Service (ATIS)** recording. Before entering the airspace, pilots listen. They learn the active runway, weather conditions, current altimeter setting, and any conditions affecting operations. The **Automatic Terminal Information Service** is not a restriction. It is a gift — information that makes the flight safer and the pilot more effective before the first radio call is made.

Artificial intelligence systems deployed for public or enterprise use currently provide no equivalent. Sessions begin with a generic prompt — "How can I help you today?" — that discloses nothing about the system's capabilities, limitations, confidence boundaries, or operating context. Users proceed without a briefing. Misaligned expectations produce misuse, overtrust, and harm that an informed user would have avoided.

This paper proposes the **AI Preflight Briefing Standard (APBS)** — a structured, session-initiation disclosure framework that gives users the information they need to operate effectively with an AI system before the first substantive exchange. The **AI Preflight Briefing Standard** is designed to function as a capability disclosure mechanism, not a legal disclaimer. It makes AI more useful, not more restricted.

---

## 1. The Problem: Sessions Begin Without Context

When a pilot arrives at an unfamiliar airport, they do not simply taxi onto the runway. They listen to the **Automatic Terminal Information Service**. They call ground control. They receive their clearance. By the time the aircraft moves, the pilot has a shared operational picture with the tower — who they are, where they are going, what conditions exist, and what the active procedures are.

When a user initiates an AI session, none of this occurs. The system knows nothing about the user's intent, expertise level, or expectations. The user knows nothing about the system's actual capabilities, current confidence levels, or operating boundaries. Two parties begin a consequential interaction with no shared context.

The results are predictable:

- Users ask questions outside the system's reliable knowledge domain without knowing it
- Systems answer with uniform confidence regardless of actual reliability
- Users overtrust output in domains where the system is operating near its limits
- Systems undertrust users who have expertise that would have changed the interaction
- No record exists of what either party understood about the operating context at session start

This is not a failure of intelligence — human or artificial. It is a failure of briefing. The information existed. It was never exchanged.

---

## 2. The ATIS Model

The **Automatic Terminal Information Service** works because it is:

- **Proactive** — delivered before the flight begins, not during a crisis
- **Standardized** — pilots know exactly what to expect and where to find each piece of information
- **Concise** — enough information to operate safely, no more
- **Non-punitive** — not a test, not a restriction, not a legal barrier. A tool.
- **Acknowledged** — the pilot reads back the **ATIS** identifier, confirming receipt

The **AI Preflight Briefing Standard** adopts all five properties. It is delivered before the session begins. It follows a defined structure. It is brief. It is framed as capability disclosure, not liability disclaimer. And it creates a documented moment of acknowledgment.

---

## 3. The Standard: Five Briefing Elements

A compliant **AI Preflight Briefing Standard** session initiation includes five elements, delivered in plain language before the first substantive exchange.

### Element 1 — Identity and Role

The system identifies itself and its defined role.

*Example: "I am [System Name], an AI assistant configured for [general use / healthcare information / legal research / financial analysis]. My role in this session is [description]."*

This is the **ATIS** airport identifier. The user knows who they are talking to and what the system was built to do.

### Element 2 — Capability Summary

The system discloses what it does well and where its reliable domain ends.

*Example: "I am well-suited for [drafting, summarizing, analyzing, explaining]. I am less reliable for [real-time information, jurisdiction-specific legal advice, medical diagnosis, calculations requiring external data]."*

This is the active runway and weather information. The user knows the operating conditions before the session begins.

### Element 3 — Confidence Disclosure

The system discloses its current confidence posture — particularly any factors that may affect output reliability in this session.

*Example: "My training data has a knowledge cutoff of [date]. For topics after that date, I will flag when I am uncertain. For any output I provide in [high-consequence domain], I recommend independent verification."*

This is the altimeter setting and **Notice to Air Missions (NOTAM)** summary — conditions that affect reliability right now, in this session.

### Element 4 — Boundary Disclosure

The system discloses what it will not do and why, in plain language.

*Example: "There are some requests I will decline — specifically [harm facilitation, jurisdiction-specific legal advice, medical diagnosis, content involving minors]. If I decline a request, I will tell you why and suggest alternatives where possible."*

This is the departure procedure — what to expect if a go-around is required. Not a threat. Operational information.

### Element 5 — Acknowledgment

The user acknowledges the briefing. In a compliant implementation, this acknowledgment is logged as a **Session Boundary** event in the **AI Black Box Standard (AIBB)** framework (Dixon, 2026).

*Example: "Do you have any questions about how I work before we begin?"*

This is the **ATIS** readback. The pilot confirms the information was received. The record exists.

---

## 4. Certification as Feature, Not Restriction

The aviation industry's experience with the **Automatic Terminal Information Service** and pre-flight briefing standards demonstrates a counterintuitive truth: informed users are better users. Pilots who receive a full weather briefing make better decisions. They divert when conditions warrant. They file alternate airports. They slow down in areas of reduced visibility.

Research on human-automation interaction confirms this principle. Parasuraman and Riley (1997) documented that misuse and abuse of automation — not just disuse — contribute to system failure, and that informed operators calibrate their trust appropriately. The corollary for AI deployment is direct: users who understand what the system can and cannot reliably do will:

- Ask better questions
- Verify output in appropriate domains
- Trust the system more where its confidence is warranted
- Catch errors in domains where they know the system is operating near its limits
- Report problems accurately when something goes wrong

This is not restriction. This is leverage. The **AI Preflight Briefing Standard** makes AI more useful by making users more capable operators of the system they are holding.

Platforms that implement the **AI Preflight Briefing Standard** gain:

- Improved user outcomes and retention
- Reduced liability exposure from overtrust in high-consequence domains
- A differentiation story: the system introduces itself
- Compliance posture for the **European Union AI Act** (Regulation (EU) 2024/1689, effective August 2, 2026), Article 50 transparency obligations, without friction
- A documented session-start record that supports audit and incident investigation

---

## 5. Three Implementation Tiers

### Tier 1 — Casual User Implementation

For consumer-facing AI products. Lightweight. Natural language. Delivered conversationally, not as a legal wall.

The briefing is baked into the onboarding experience. The user experiences it as the AI introducing itself. No formal acknowledgment required. The disclosure is the experience.

**Target length:** 3–5 sentences at session initiation.

### Tier 2 — Professional User Implementation

For AI deployed in professional contexts — healthcare information, legal research, financial analysis, enterprise operations. Structured five-element briefing delivered at session start. Acknowledgment required. Session-start event logged.

**Target length:** One paragraph per element. Under 300 words total.

### Tier 3 — Regulated Domain Implementation

For AI deployed in safety-critical or regulated industries — aviation, healthcare, financial services, infrastructure. Full **AI Preflight Briefing Standard** briefing with **AIBB**-compliant logging. **Chief AI Accountability Officer (CAAO)** review of briefing template required before deployment. Recurrency review of briefing content at minimum annually.

**Target length:** Structured document, delivered and acknowledged before session initiation. Logged as a **Session Boundary** event.

---

## 6. Relationship to the AI Type Rating Framework

The **AI Preflight Briefing Standard** operates at the session level. The **AI Type Rating Framework (ATRF)** (Dixon, 2026) operates at the user certification level. These are complementary, not redundant.

The **Automatic Terminal Information Service** tells every pilot what the conditions are today. The type rating ensures the pilot is qualified to operate in those conditions. Both are necessary. Neither substitutes for the other.

A user holding a full **AI Type Rating** still receives the **AI Preflight Briefing** at session initiation. The briefing confirms current conditions. The certification confirms the user is qualified to handle them.

---

## 7. Conclusion

The aviation industry did not mandate pre-flight briefings because pilots were incompetent. It mandated them because complex systems operating in dynamic environments require a shared operational picture before the flight begins. The briefing is not a test of the pilot. It is a gift to the pilot — and to everyone aboard.

AI systems are complex. The environments they operate in are dynamic. The users operating them have wildly varying levels of understanding about what the system can and cannot reliably do. Sending them into the session without a briefing is not neutral. It is a choice — and the consequences of that choice appear in every overtrust incident, every misuse report, and every moment a user discovered the system's limits after the fact rather than before.

The **AI Preflight Briefing Standard** is the **Automatic Terminal Information Service** for AI. Brief. Standardized. Non-punitive. Acknowledged. And issued before the first exchange — not after the crash.

---

## References

1. Federal Aviation Administration. (2021). *Aeronautical Information Manual: Official Guide to Basic Flight Information and ATC Procedures* (Section 4-1-13: Automatic Terminal Information Service). U.S. Department of Transportation. https://www.faa.gov/air_traffic/publications/atpubs/aim_html/

2. European Parliament. (2024). *Regulation (EU) 2024/1689 of the European Parliament and of the Council laying down harmonised rules on artificial intelligence (Artificial Intelligence Act).* Official Journal of the European Union. (Transparency obligations for providers and deployers, Article 50.)

3. Parasuraman, R., & Riley, V. (1997). Humans and automation: Use, misuse, disuse, abuse. *Human Factors, 39*(2), 230–253. https://doi.org/10.1518/001872097778543886

4. Dixon, A. C. (2026). *AI Black Box Standard (AIBB) v2.4.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

5. Dixon, A. C. (2026). *AI Type Rating Framework (ATRF) v1.0.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

6. Dixon, A. C. (2026). *Covenant Warning System (CWS) v1.0.* Defensive publication. https://github.com/Tonydixon417-cmd/ZeroTX---architecture-

---

*This document is a defensive publication establishing prior art for the AI Preflight Briefing Standard (APBS). All concepts, terminology, and proposed standards contained herein are the original intellectual work of Anthony C. Dixon / Contrail Equity Strategies LLC, May 2026. All rights reserved.*
