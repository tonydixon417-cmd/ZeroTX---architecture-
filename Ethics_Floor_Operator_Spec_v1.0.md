# The Ethics Floor — Operator Specification
## Engineering Rules for Persistent AI Deployment

**Contrail Equity Strategies LLC · v1.0 · May 2026**
**Author: Anthony Cyle Dixon**

---

## What This Document Is

This is the deployment companion to *The Ethics Floor: A Cross-Cultural Foundation for AI Accountability Systems* (v2.0, May 2026).

That document establishes the principles. This document tells engineers what to build.

Every principle in this spec is expressed as a testable condition with a defined system action and a required log entry. If a principle cannot be audited, it is not in this document. Philosophy belongs in the paper. Rules belong here.

This spec does not replace the AIBB logging standard, the Loop Detector, or the PIL architecture. It references them. Those documents define the infrastructure. This document defines what the infrastructure must enforce.

---

## Conflict Resolution Tier System

When a user request conflicts with an Ethics Floor principle, the system must classify the conflict before responding. Classification determines action. Action is logged. There is no unclassified conflict.

**Tier 1 — Direct Harm**
*Trigger:* Request would directly facilitate harm to an identifiable third party.
*System action:* Decline. State that the request cannot be completed. Do not explain how to reframe the request to avoid the constraint.
*Log entry:* Timestamp · session ID · request classification · tier assigned · action taken · human review flag = TRUE

**Tier 2 — Indirect or Organizational Harm**
*Trigger:* Request may facilitate harm to a third party or group through an intermediate action. Includes decisions that benefit the operator at the expense of the user population.
*System action:* Warn. Complete the task with a mandatory disclosure appended. Escalate to the designated human accountability officer (CAAO or equivalent) via log flag.
*Log entry:* Timestamp · session ID · request classification · tier assigned · warning issued · disclosure text · escalation flag = TRUE

**Tier 3 — Self-Directed Risk**
*Trigger:* Request involves an action that may harm the user themselves. User autonomy is presumed intact.
*System action:* Inform fully. State the risk without softening. Complete the task. The decision belongs to the human.
*Log entry:* Timestamp · session ID · request classification · tier assigned · risk disclosure issued · task completed · user autonomy invoked = TRUE

**Unclassifiable conflict:**
If the system cannot classify a conflict within these three tiers, the default action is Tier 2 treatment. Escalate. Do not guess. Do not proceed silently.

---

## Five Principles — Machine-Testable Rules

---

### Principle 1 — Do Not Harm

**Observable condition triggering review:**
Request contains: instructions for actions directed at a named or identifiable third party + language indicating intent to damage, deceive, expose, or coerce that party.

**Prohibited system action:**
Completing the request without classification. Reframing the request to make it appear compliant. Partial completion that enables harm while maintaining plausible deniability.

**Required system action:**
Classify using Tier system above. Apply corresponding action. Log.

**Audit field:**
`harm_classification` : [none / tier1 / tier2 / tier3 / unclassified]
`harm_action_taken` : [completed / warned / declined / escalated]

---

### Principle 2 — Do Not Deceive

**Observable condition triggering review:**
System output is goal-directed toward a predetermined conclusion using the user's known preferences, psychology, or vulnerabilities as the mechanism of persuasion — rather than evidence and reasoning.

**Three output intent categories — must be distinguishable in log:**

| Label | Definition | Disclosure required |
|---|---|---|
| `informational` | Output presents evidence and analysis without steering toward a conclusion | No |
| `persuasive` | Output is explicitly intended to advocate a position | Yes — system must label it |
| `protective_withholding` | Output omits content to protect user's genuine interest | Yes — system must disclose that an omission occurred, even if content is withheld |

**Prohibited system action:**
Persuasive output delivered without the `persuasive` label. Omission of content without disclosure that an omission occurred. Silence about the silence.

**Required system action:**
Label all output by intent category before delivery. When omitting content, append: *"Note: this response omits information. The omission is in your interest. The full record is logged."*

**Audit field:**
`output_intent` : [informational / persuasive / protective_withholding]
`omission_occurred` : [true / false]
`omission_disclosed` : [true / false]

---

### Principle 3 — Respect Autonomy

**Observable condition triggering review:**
System output presents a recommendation as a conclusion. System output implies a decision has already been made. System output omits material risk information before a consequential user decision.

**Prohibited system action:**
Presenting recommendations as conclusions. Completing a decision-adjacent task without surfacing known material risks. Overriding a user's stated choice on the basis of the system's assessment of what is good for them.

**Required system action:**
Label all recommendations explicitly: *"This is a recommendation. The decision is yours."*
Surface all known material risks before task completion.
If user proceeds after risk disclosure: log autonomy invocation, complete task.

**Audit field:**
`decision_type` : [recommendation / informational / user_decision]
`risk_disclosure_issued` : [true / false / not_applicable]
`autonomy_invoked` : [true / false]

*Note: Principle 3 and Principle 1 interact at Tier 3. When a user invokes autonomy for a self-directed risk, the system informs and completes. When a request involves harm to others, autonomy does not override Tier 1 or Tier 2 classification. The conflict resolution tier system governs. Autonomy applies to the user's own domain. It does not extend to the domain of third parties.*

---

### Principle 4 — Act Fairly

**Observable condition triggering review:**
System output applies materially different standards to similar requests from different users. System is configured by an operator to optimize for operator outcomes at measurable cost to user outcomes.

**Prohibited system action:**
Differential treatment of equivalent requests based on user identity, role, or commercial value to the operator without disclosed justification. Configuration that uses user data to benefit the operator without user disclosure.

**Required system action:**
Operator configurations that affect user outcomes must be logged at the configuration layer, not the session layer. Any configuration that directs the system to prioritize operator interests over user interests must be disclosed to the user at session open.

**Audit field:**
`operator_config_disclosure` : [true / false / not_applicable]
`differential_treatment_flag` : [true / false]
`fairness_escalation` : [true / false]

---

### Principle 5 — Be Accountable

**Logging architecture minimum standard:**

| Requirement | Specification |
|---|---|
| Immutability | Append-only. No record may be modified or deleted after write. Hash each entry at write time. |
| Format | Human-readable. Machine-parseable. JSON acceptable. Plain text acceptable. Proprietary binary format: not acceptable. |
| Access — User | Full access to their own session logs on request. Response time: 30 days maximum. |
| Access — Operator | Full access to all logs within their deployment. Cannot modify. Cannot delete. |
| Access — Regulator / Legal | Producible in full on lawful demand. Operator cannot selectively produce. |
| Retention minimum | 7 years for consequential deployments (healthcare, legal, financial). 3 years minimum for all others. |
| Dispute trigger | Any user assertion that a logged decision caused harm initiates mandatory human review within 72 hours. Auto-escalate to CAAO. |

**Prohibited:**
Log access restricted exclusively to the operator. Logs producible only in proprietary format. Retroactive modification of any log entry for any reason including legal hold, compliance review, or system update.

**Audit field:**
`log_hash` : [SHA-256 of entry at write time]
`access_level` : [user / operator / regulator]
`dispute_flag` : [true / false]
`caao_notified` : [true / false]

---

## Integration References

This spec enforces the Ethics Floor principles at the rule layer. It does not define the infrastructure those rules run on. For full specifications:

- **Logging infrastructure:** AI Black Box Standard (AIBB) v2.4 — Contrail Equity Strategies LLC, May 2026
- **Loop detection:** Loop Detector v1.3 — Contrail Equity Strategies LLC, May 2026
- **Session architecture:** Personal Identity Layer (PIL) — Contrail Equity Strategies LLC, May 2026
- **Drift classification:** Drift Taxonomy v1.0 — Contrail Equity Strategies LLC, May 2026
- **Human accountability role:** CAAO definition — AIBB v2.4, Section 4

---

## Version Notes

v1.0 — Initial release. Companion to Ethics Floor Whitepaper v2.0.
Addresses identified gaps: machine-testable principles, conflict resolution tier system, logging architecture specification, output intent labeling, operator/user access model.

---

*Copyright Anthony Cyle Dixon, Contrail Equity Strategies LLC, May 2026. Published as open prior art. All rights reserved.*
