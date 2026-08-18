# TenderAI Assistant — EU AI Act Compliance Memo

## To: Head of Product — TenderAI
## Subject: First-Pass EU AI Act Compliance Assessment
## Date: 18 August 2026

---

## 1. System Classification

TenderAI is currently assessed as a **minimal-risk AI system with applicable transparency requirements**, based on its intended purpose as a commercial tender-analysis and bid-preparation assistant.

The system does not currently appear to fall within an Article 5 prohibited practice or one of the Annex III high-risk areas. However, because TenderAI directly interacts with users through an AI chat interface, the applicable Article 50 transparency requirement must be addressed.

This is a first-pass assessment and not a legal opinion.

---

## 2. Role Map

The TenderAI developer / consulting business would be the **provider** if the system were placed on the market or put into service under its name or trademark.

The client organisation using TenderAI for its own tender and bid activities would generally be the **deployer**.

OpenAI is a third-party AI/model service dependency, while Pinecone provides vector-database infrastructure.

The exact legal role and responsibility allocation should be confirmed against the final production architecture and contractual arrangements.

---

## 3. Key Findings

### Finding 1 — AI interaction transparency

TenderAI contains a direct AI chat interface, but the current MVP does not establish that users are clearly informed that they are interacting with an AI system.

A visible AI disclosure should therefore be added to the production interface before or at the beginning of the user's interaction with TenderAI.

### Finding 2 — Human review is not formally enforced

TenderAI is designed as a decision-support tool and the documentation requires human review before final tender use.

However, the MVP does not currently provide a formal approval gate, reviewer record, or structured override mechanism.

A production workflow should record who reviewed the AI assessment, whether it was accepted or modified, and whether an AI recommendation was overridden.

### Finding 3 — Evidence verification should be strengthened

TenderAI already uses RAG retrieval and evidence validation to reduce unsupported claims.

However, the production system should make the distinction between source evidence, AI interpretation, missing evidence, and human-verified information clearer.

This would improve traceability and reduce the risk that an AI-generated conclusion is treated as verified company information.

---

## 4. Recommended Next Steps

### Step 1 — Implement AI transparency

Add a clear AI-interaction notice to the TenderAI chat interface.

**Owner:** TenderAI provider

### Step 2 — Formalise human review

Introduce a review and approval procedure for AI-generated tender assessments and response blueprints.

**Owner:** TenderAI provider + client

### Step 3 — Strengthen evidence traceability

Display source documents and evidence references alongside material tender assessments and generated response content.

**Owner:** TenderAI provider

### Step 4 — Complete production data-protection assessment

Before connecting real client repositories or processing real personal data, conduct a GDPR/data-protection review covering the AI and infrastructure providers.

**Owner:** Client + DPO/privacy specialist

### Step 5 — Provide user guidance

Create short user guidance explaining TenderAI's capabilities, limitations, evidence model, and human-review requirements.

**Owner:** TenderAI provider + client

---

## 5. Caveats

This memo is a first-pass compliance assessment prepared for an educational Project 3 audit.

It is **not**:

- a legal opinion;
- a formal EU AI Act conformity assessment;
- a certification;
- a substitute for legal advice;
- a determination of the final contractual roles of the parties;
- a GDPR data-protection assessment.

The classification should be reassessed if TenderAI's intended purpose, functionality, users, or deployment context changes.

Particular attention would be required if the system were extended into employment, education, access to essential services, law enforcement, biometrics, migration, justice, or another Annex III area.

---

## Executive Conclusion

Based on the current MVP and intended purpose, TenderAI does not appear to be a prohibited or high-risk AI system under the EU AI Act.

The immediate compliance priority is **AI-interaction transparency**.

The most important operational priorities are **formal human review and stronger evidence traceability**.

Before production deployment with real enterprise information, a separate **GDPR/data-protection assessment** should be completed.

The product should also maintain a documented intended purpose and reassess its AI Act classification whenever significant functionality or use cases change.