# TenderAI Assistant — EU AI Act Gap Analysis & Remediation

## Phase 5 — Gap Analysis and Remediation Plan

This gap analysis follows the Phase 4 first-pass assessment of the TenderAI MVP.

TenderAI is currently assessed as a minimal-risk AI system with applicable transparency requirements under Article 50. It is not currently classified as a high-risk system under Annex III.

The analysis focuses on identified transparency gaps, operational controls, and parallel legal issues that would need to be addressed before a production deployment using real client data.

This is a first-pass compliance exercise and not a legal opinion, conformity assessment, or certification.

---

# Gap 1 — AI Interaction Transparency

## Obligation

Article 50(1) — transparency for AI systems intended to interact directly with natural persons.

## Current state

TenderAI contains an interactive chat interface through which users can communicate directly with an AI assistant.

The current MVP documentation does not establish that the interface displays a clear notice informing users that they are interacting with an AI system.

## Required state

Users should be clearly informed that they are interacting with an AI system, unless this is already obvious from the circumstances and context.

The disclosure should be clear and accessible at or before the first interaction.

## Remediation

Add a visible AI disclosure to the TenderAI interface.

Suggested wording:

> **AI Assistant Notice**
>
> You are interacting with TenderAI, an AI-powered assistant. Its responses are generated using artificial intelligence and should be reviewed and verified by an appropriate member of the bid team before being relied upon for a tender submission.

The notice should appear before or at the beginning of the first interaction with TenderAI.

The same principle should be applied to any future interface through which users directly interact with the AI assistant.

## Escalation needed?

**No for the basic implementation.**

Legal or compliance review is recommended before production deployment to confirm the final wording and implementation against the applicable Article 50 requirements.

---

# Gap 2 — Human Review Is Expected but Not Formally Enforced

## Obligation

Operational control supporting responsible use of AI outputs.

TenderAI is not currently classified as high-risk, so Article 14's high-risk human-oversight requirements do not directly apply.

However, human review is an important control because TenderAI can generate bid-readiness assessments, compliance assessments, recommendations, and response content.

## Current state

The current system documentation states that human users must:

- review AI assessments;
- verify supporting evidence;
- validate missing information;
- review response recommendations;
- review the Tender Response Blueprint;
- validate legal, technical and commercial content;
- approve the final tender response.

However, the MVP does not contain a formal approval gate.

It does not currently record:

- who reviewed the assessment;
- whether the assessment was approved;
- whether an AI recommendation was overridden;
- why an override occurred.

## Required state

Before production use, the organisation should have a clearly defined human-review process for AI-generated tender assessments and response material.

The final tender submission should remain under human responsibility.

## Remediation

Introduce a formal review step before an AI-generated assessment or response blueprint can be treated as ready for final bid preparation.

The process should allow the reviewer to record:

- reviewer name or role;
- review date;
- assessment reviewed;
- evidence verified;
- decision: accepted / modified / rejected;
- reason for overriding an AI recommendation where applicable.

The MVP does not necessarily need a complex workflow engine. A simple approval record could initially be sufficient.

## Escalation needed?

**No for the basic workflow design.**

The client should determine internally who has authority to approve technical, commercial and legal content.

---

# Gap 3 — Evidence Verification and Traceability

## Obligation

Operational control supporting reliable use of AI-generated outputs.

## Current state

TenderAI already contains several positive controls:

- RAG retrieval from the company knowledge base;
- evidence retrieval;
- supported / partially supported / insufficient classifications;
- missing-information identification;
- evidence validation logic;
- warnings against unsupported company claims.

The system is therefore designed to reduce hallucination and unsupported claims.

However, the current MVP does not formally distinguish every generated statement between:

1. information directly retrieved from company evidence;
2. AI interpretation of that evidence;
3. information that is missing;
4. information that has been verified by a human reviewer.

## Required state

A production workflow should make the evidence basis of important tender assessments visible to the bid team.

Users should be able to distinguish company evidence from AI-generated interpretation.

## Remediation

Strengthen the response and compliance-matrix output so that important conclusions contain:

- source document;
- relevant page or evidence reference where available;
- extracted evidence;
- AI interpretation;
- identified uncertainty or missing evidence;
- human verification status.

Before final submission, the bid team should verify material claims against the original company documents.

## Escalation needed?

**No for the technical implementation.**

A domain expert should determine what evidence is considered sufficient for technical and contractual claims.

---

# Gap 4 — Production Data Protection Assessment

## Obligation

Parallel EU legal requirement — GDPR and applicable data-protection law.

This is not an AI Act risk-tier obligation.

## Current state

The current MVP uses synthetic company documents and therefore does not intentionally process real client personal data.

A production version could, however, process personal data contained in:

- employee CVs;
- project references;
- contact details;
- tender documents;
- previous tender responses;
- emails;
- internal company documentation;
- connected enterprise repositories.

The architecture also uses third-party services including an external AI provider and a vector database.

## Required state

Before real client information is processed, the organisation should understand:

- what personal data enters the system;
- why it is processed;
- which third parties receive it;
- where processing occurs;
- how long information is retained;
- how information is deleted;
- who can access it;
- what contractual data-processing arrangements apply;
- whether international data transfers occur.

## Remediation

Conduct a dedicated GDPR/data-protection assessment before connecting real enterprise data sources.

The production architecture should document:

- data flows;
- categories of data processed;
- third-party processors;
- retention periods;
- deletion procedures;
- access controls;
- security measures;
- applicable data-processing agreements.

The client should involve its Data Protection Officer or appropriate privacy specialist where required.

## Escalation needed?

**YES — Data Protection Officer / privacy specialist.**

Legal review should be completed before processing real client personal data at production scale.

---

# Gap 5 — AI Literacy and User Guidance

## Obligation

AI literacy requirements applicable to providers and deployers should be considered for the people operating and using the system.

## Current state

TenderAI documentation explains that users should review AI-generated outputs.

However, the MVP does not contain a formal AI-use policy or structured user training.

## Required state

Users should understand the capabilities and limitations of TenderAI sufficiently to use it responsibly.

This is particularly important because the system can generate apparently authoritative assessments and recommendations.

## Remediation

Create a short TenderAI user guidance document covering:

- what TenderAI does;
- what it does not do;
- how RAG evidence works;
- what "supported", "partially supported" and "insufficient" mean;
- why AI outputs must be verified;
- examples of possible AI errors;
- which decisions must remain with humans;
- how to report incorrect outputs.

Include this guidance in onboarding for production users.

## Escalation needed?

**No for initial implementation.**

The client should determine the appropriate internal training requirements.

---

# Remediation Priority

| Priority | Gap | Action | Responsible party |
|---|---|---|---|
| 1 | AI interaction transparency | Add Article 50 AI disclosure to chat interface | TenderAI provider |
| 2 | Human review | Introduce formal review and approval process | TenderAI provider + client |
| 3 | Evidence traceability | Strengthen source/evidence visibility and verification | TenderAI provider |
| 4 | GDPR / data protection | Conduct production data-protection assessment | Client + DPO/privacy specialist |
| 5 | AI literacy | Create user guidance and onboarding material | TenderAI provider + client |

---

# Overall Remediation Conclusion

TenderAI does not currently require the high-risk compliance framework applicable to Annex III systems based on its documented intended purpose.

The most immediate AI Act remediation is therefore transparency for direct AI interaction.

The most important operational remediation is formalising human review and evidence verification before AI-generated tender assessments are relied upon in a final submission.

Before production deployment with real company information, the client should also complete a separate GDPR and data-protection assessment covering the data flows to the AI and infrastructure providers.

The product's intended purpose should be monitored continuously. If TenderAI is later extended into employment, education, access to essential services, law enforcement, biometric systems, or another regulated Annex III context, the AI Act classification must be reassessed.