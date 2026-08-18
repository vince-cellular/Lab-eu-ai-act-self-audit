# TenderAI Assistant — EU AI Act Risk Classification

## Phase 2 — Risk Tier Classification

This is a first-pass assessment based on the current TenderAI MVP design and intended purpose. It is not a legal opinion or final regulatory determination.

| Question | Assessment |
|---|---|
| Does this system fall under any prohibited category (Article 5)? | **No, based on the current intended purpose and design.** TenderAI analyses commercial tender documents, retrieves company evidence, assesses tender requirements, identifies gaps, and supports bid preparation. It does not perform the prohibited practices identified in Article 5 such as social scoring, prohibited manipulation, emotion recognition in the relevant prohibited contexts, or other prohibited uses. |
| Does this system operate in any of the eight Annex III areas? | **No, based on the current intended purpose.** TenderAI is designed for commercial tender analysis and bid preparation. Its intended purpose is not employment, education, law enforcement, migration, biometric identification, access to essential services, justice, or another Annex III high-risk area. |
| If Annex III: does it "significantly influence" decisions in that area, or is it narrow/preparatory? | **Not applicable on the current facts.** TenderAI does influence an internal commercial decision by providing bid-readiness assessments and recommendations, but this decision does not concern an Annex III high-risk area. The final bid decision remains with the company's human bid and management teams. |
| Does this system interact with end users or generate content requiring disclosure (Article 50)? | **Potentially yes.** TenderAI includes a direct AI chat interface through which users interact with an AI assistant. The production interface should therefore be assessed for the applicable Article 50 transparency requirement and should clearly inform users that they are interacting with an AI system where required. |
| First-pass risk tier | **Minimal risk. A separate assessment is required for applicable Article 50 transparency obligations relating to the direct AI interaction.** |
| One-sentence justification citing the specific article or Annex entry | **TenderAI does not appear to fall within an Article 5 prohibited practice or an Annex III high-risk area based on its current commercial tender-analysis purpose; its direct AI interaction should nevertheless be assessed separately against the applicable Article 50 transparency requirements.** |

## Classification Rationale

TenderAI is primarily a business decision-support and document-preparation system. Its intended purpose is to analyse tender requirements against a company's knowledge base, identify evidence and gaps, assess bid readiness, and generate a structured response blueprint.

The system does produce recommendations that can influence whether a company proceeds with a tender. However, the decision concerns a commercial bidding activity rather than a decision in one of the Annex III high-risk areas. The current system therefore does not become high-risk merely because its output can influence a business decision.

The current design also does not indicate an Article 5 prohibited practice. It does not use biometric identification, emotion recognition, social scoring, manipulation, or other prohibited functionality described in the current intended use.

The main AI Act issue identified at this stage is transparency. TenderAI includes an interactive AI assistant, so the production implementation should determine and implement any applicable Article 50 disclosure requirements. At minimum, the user interface should make the AI nature of the interaction clear where required.

## Important Boundary

This classification is based on the current intended purpose of TenderAI.

The classification could change if the product is later redesigned to support decisions concerning:

- recruitment or employment;
- education admissions or assessment;
- access to essential services;
- credit or insurance decisions;
- law enforcement;
- migration or border control;
- biometric identification;
- justice or democratic processes.

Any such change in intended purpose would require a new AI Act assessment.
