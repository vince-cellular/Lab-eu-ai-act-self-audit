# TenderAI Assistant — EU AI Act Obligation Assessment

## Phase 4 — Applicable Obligations

This assessment is a first-pass compliance review of the current TenderAI MVP. It is based on the system's documented intended purpose, architecture, and current deployment model.

It is not a legal opinion, conformity assessment, or certification.

---

## 1. High-Risk Obligations

TenderAI is currently classified as **minimal risk / transparency risk**, rather than high-risk.

The current intended purpose is commercial tender analysis and bid-preparation support. The system does not operate in an Annex III high-risk area such as employment, education, access to essential services, law enforcement, migration, biometrics, or justice.

Therefore, the specific high-risk provider obligations under Articles 9–15 and the related conformity, registration and post-market requirements are **not triggered solely by the current intended purpose**.

The high-risk checklist from the lab is therefore not completed.

This conclusion must be reassessed if TenderAI's intended purpose or deployment context changes.

---

## 2. Article 50 — Transparency

Article 50 is the main AI Act obligation identified for the current TenderAI design.

TenderAI contains an interactive AI assistant through which users can directly communicate with an AI system.

Article 50(1) requires providers of AI systems intended to interact directly with natural persons to ensure that those persons are informed that they are interacting with an AI system, unless this is already obvious from the circumstances and context.

The European Commission's current guidance confirms that Article 50 transparency obligations apply from 2 August 2026. 

### Current state

The current MVP contains a TenderAI chat interface.

However, the system documentation does not establish that the production interface contains a clear and explicit notice informing users that they are interacting with an AI system.

Therefore:

**Status: PARTIAL / GAP**

### Required state

The production interface should clearly inform users that the TenderAI assistant is an AI system at or before the first interaction, unless the AI nature of the interaction is already obvious in context.

The notice should be clear, distinguishable and accessible.

### Proposed implementation

Add a visible notice to the TenderAI interface, for example:

> **AI assistant notice:** You are interacting with TenderAI, an AI-powered assistant. Its responses are generated using AI and should be reviewed and verified by a qualified member of the bid team before being relied upon for a tender submission.

The notice should appear before or at the user's first interaction with the assistant.

---

## 3. Article 50 — AI-Generated Text and Reports

TenderAI generates several forms of text, including:

- AI chat responses;
- tender requirement assessments;
- compliance explanations;
- bid-readiness recommendations;
- Tender Response Blueprints;
- structured report content.

Article 50 also contains rules concerning AI-generated or manipulated content.

However, the current TenderAI use case is an internal business workflow. The generated reports are intended to support a company's bid team rather than to publish information to the general public.

The current MVP therefore does not appear to trigger the specific deployer obligation concerning AI-generated text published to inform the public on matters of public interest.

If generated content were later published externally for a public-information purpose, the Article 50 analysis would need to be revisited.

### Current state

**Status: No specific Article 50(4) deployer gap identified on the current facts.**

### Boundary

The product should not assume that all AI-generated text automatically requires the same public disclosure treatment. The intended use and publication context matter.

---

## 4. Article 50 — Deepfakes, Emotion Recognition and Biometrics

TenderAI does not currently:

- generate or manipulate deepfake audio, image or video;
- perform emotion recognition;
- perform biometric categorisation;
- perform biometric identification.

Therefore the corresponding Article 50 transparency obligations are not applicable to the current MVP.

### Status

**Not applicable based on current functionality.**

This should be reassessed if these capabilities are added in a future version.

---

## 5. Human Review

Although TenderAI is not currently classified as high-risk, human review remains an important control in the system design.

The current workflow states that users must review:

- AI-generated assessments;
- supporting evidence;
- identified gaps;
- missing information;
- response recommendations;
- the Tender Response Blueprint;
- final technical, legal and commercial content.

The final bid decision remains with the client organisation.

### Current state

Human review exists as a documented process expectation.

However, the MVP does not currently contain:

- a mandatory approval gate;
- a formal override mechanism;
- a record of who reviewed an AI assessment;
- a structured record explaining why an AI recommendation was accepted or rejected.

### Status

**PARTIAL**

This is not currently a specific Article 14 high-risk obligation because TenderAI is not classified as high-risk.

Nevertheless, strengthening human review would reduce operational and compliance risk.

---

## 6. Accuracy and Grounding

TenderAI is designed to reduce unsupported AI claims through retrieval from the company knowledge base.

The system:

- retrieves relevant evidence;
- distinguishes supported, partially supported and insufficient requirements;
- identifies missing information;
- is designed not to invent company experience or certifications;
- requires human verification before final submission.

This is a positive control.

However, the current MVP does not provide a formal guarantee that every AI-generated statement is factually correct.

### Status

**PARTIAL**

### Recommended improvement

Introduce a formal evidence-validation step before a response blueprint can be approved for final use.

The system should clearly distinguish:

- retrieved evidence;
- AI interpretation;
- missing evidence;
- human-verified information.

---

## 7. Data Protection / GDPR Boundary

The current MVP uses synthetic company documents and therefore does not intentionally process real personal data.

However, a production deployment could contain personal data within:

- tender documents;
- employee CVs;
- project references;
- contact information;
- internal documents;
- previous tender responses;
- emails or other connected enterprise sources.

The AI Act classification does not remove the need to assess GDPR and other applicable data-protection requirements.

A production deployment should therefore undergo a separate data-protection assessment.

### Questions requiring review

- What personal data enters TenderAI?
- What data is sent to third-party AI services?
- Where is the data processed?
- How long is it retained?
- What deletion mechanisms exist?
- What access controls are applied?
- What contractual data-processing arrangements are required?
- Are international transfers involved?

### Status

**Parallel legal / data-protection review required for production.**

This is outside the scope of the AI Act risk-tier classification itself.

---

# Summary Table

| Requirement / Issue | Article | Status | Finding |
|---|---:|---|---|
| High-risk risk-management system | 9 | Not applicable | Current system is not classified as high-risk |
| High-risk data governance | 10 | Not applicable | Current system is not classified as high-risk |
| High-risk technical documentation | 11 | Not applicable | Current system is not classified as high-risk |
| High-risk logging | 12 | Not applicable | Current system is not classified as high-risk |
| High-risk transparency to deployers | 13 | Not applicable | Current system is not classified as high-risk |
| High-risk human oversight | 14 | Not applicable | Current system is not classified as high-risk |
| High-risk accuracy/robustness/cybersecurity | 15 | Not applicable | Current system is not classified as high-risk |
| Conformity assessment | 43 | Not applicable | No high-risk classification identified |
| EU declaration / CE marking | 47–48 | Not applicable | No high-risk classification identified |
| Registration | 49 | Not applicable | No applicable high-risk registration identified |
| Post-market monitoring | 72 | Not applicable | No high-risk classification identified |
| Direct AI interaction transparency | 50(1) | **Partial / Gap** | Production interface should clearly inform users they are interacting with AI |
| AI-generated public-interest text | 50(4) | Not currently applicable | Current use is internal business support, not public-interest publication |
| Deepfake disclosure | 50(4) | Not applicable | No deepfake functionality |
| Emotion / biometric transparency | 50(3) | Not applicable | No such functionality |
| Human review | Operational control | **Partial** | Human review exists but is not formally enforced or recorded |
| Evidence validation | Operational control | **Partial** | Grounding exists but formal human verification could be strengthened |
| GDPR / data protection | Separate EU law | **Review required** | Production data may contain personal data |

---

# Overall Finding

The current TenderAI MVP does not appear to trigger the AI Act's high-risk obligations based on its documented intended purpose and functionality.

The principal AI Act issue identified is **transparency under Article 50**, particularly because the product contains a direct AI chat interaction.

The most important operational weakness is that human review is described in the product documentation but is not currently enforced through a formal approval or override mechanism.

The production version should therefore prioritize:

1. Clear AI-interaction disclosure.
2. Formal human review before final tender use.
3. Evidence verification and traceability.
4. A separate GDPR/data-protection assessment before processing real client data.

---

## Regulatory Caveat

This assessment is a first-pass compliance exercise for the Project 3 audit.

It should not be treated as legal advice.

The classification and applicable obligations should be reassessed if:

- the intended purpose changes;
- the system is used in an Annex III context;
- new decision-making functionality is introduced;
- biometric or emotion-recognition functionality is added;
- the system begins producing public-interest publications;
- new enterprise data sources are connected;
- the production architecture materially changes.