# TenderAI Assistant — EU AI Act Role Map

## Phase 3 — Provider / Deployer / Third-Party Roles

This is a first-pass role assessment based on the current TenderAI MVP architecture and the intended production deployment described in the project documentation. Final contractual and legal role allocation should be confirmed for an actual deployment.

## Role Map

| Role | Entity | First-pass role | Key responsibilities / considerations |
|---|---|---|---|
| Provider | TenderAI developer / consulting business | **Provider of the TenderAI application, if the system is placed on the market or put into service under its name** | Responsible for the design and delivery of the TenderAI application and for assessing applicable AI Act requirements based on its intended purpose. |
| Deployer | Client company using TenderAI | **Deployer** | Uses TenderAI in its professional activities, provides tender and company information, establishes appropriate internal use procedures, and remains responsible for validating outputs and making final bid decisions. |
| Third-party AI service | OpenAI | **Third-party AI/model service provider** | Provides the external AI model/API used by TenderAI. The exact AI Act role and obligations should be confirmed against the specific service, model, contractual arrangement, and deployment architecture used in production. |
| Technical infrastructure | Pinecone | **Third-party technical service provider** | Provides vector database infrastructure used to store and retrieve document embeddings. Its exact regulatory role should be assessed based on the service actually provided and the production architecture. |

## Provider

For this first-pass assessment, the developer of TenderAI would be treated as the provider if the application were placed on the market or put into service under the developer's name or trademark.

The provider-side responsibilities would include:

- defining and documenting the intended purpose;
- maintaining an accurate description of the system;
- identifying applicable AI Act requirements;
- ensuring that claims about the system match its actual capabilities;
- documenting important technical and operational characteristics;
- identifying third-party AI and infrastructure dependencies;
- establishing appropriate user information and transparency measures;
- reassessing the classification if the intended purpose changes.

Because the current system is classified as minimal risk on the facts reviewed, the full set of high-risk provider obligations is not triggered solely by the current TenderAI use case.

## Deployer

The client company using TenderAI in production would be the first-pass deployer.

The deployer would use the system to support its own tender and bid activities.

The client should:

- use the system consistently with its documented intended purpose;
- ensure appropriate human review of AI-generated assessments;
- verify evidence before relying on it in a final tender;
- ensure that legal, commercial and technical commitments are reviewed by appropriate staff;
- manage access to company information;
- assess applicable GDPR and data-protection requirements;
- monitor whether the system is being used for purposes outside its original scope.

The client remains responsible for the final decision to submit a bid.

## Third-Party AI / Model Provider

TenderAI relies on an external AI service for language-model capabilities.

The external AI provider is a significant dependency because the model contributes to the generation and interpretation of system outputs.

For production deployment, the provider relationship should be documented, including:

- model/service identity;
- API and processing architecture;
- applicable contractual terms;
- data-processing arrangements;
- data retention and training settings where relevant;
- security controls;
- applicable geographic/data-transfer arrangements;
- model limitations and documentation;
- allocation of responsibilities between TenderAI and the external AI provider.

The exact AI Act role of the external model provider should not be inferred solely from the fact that an API is used. It should be verified against the actual service and contractual arrangement.

## Pinecone / Technical Infrastructure

Pinecone is used as the vector database for the RAG architecture.

It stores and retrieves searchable representations of the knowledge-base documents.

For the current MVP, Pinecone is treated as a technical infrastructure dependency rather than automatically classified as a provider of the TenderAI system.

A production assessment should verify:

- what information is stored;
- where it is stored;
- retention and deletion arrangements;
- security controls;
- access controls;
- contractual data-processing terms;
- applicable international data-transfer arrangements.

## Role Boundary

The role allocation above is a first-pass consulting assessment.

The exact legal role of each party can depend on:

- who places the system on the market;
- who puts it into service;
- whose name or trademark is used;
- whether the system is substantially modified;
- contractual arrangements;
- whether third-party components are integrated or merely consumed as services;
- the final production architecture.

A lawyer or specialist AI regulatory counsel should confirm the final role allocation before a commercial deployment.

## Key Finding

The most important role distinction for the current audit is:

**TenderAI developer / consulting business → first-pass provider**

**Client using TenderAI → first-pass deployer**

**OpenAI → third-party AI/model service dependency**

**Pinecone → third-party technical infrastructure dependency**

The current minimal-risk classification means that the high-risk provider obligations do not automatically apply to TenderAI solely because it uses AI technology.