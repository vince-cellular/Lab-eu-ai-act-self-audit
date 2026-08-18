# TenderAI Assistant — System Brief

## Purpose

TenderAI is an AI assistant that helps companies analyse tender documents and prepare for bid responses. A user uploads a tender PDF, and the system identifies the requirements in the tender and compares them with information stored in the company's knowledge base.

The purpose is to help bid and business-development teams understand a tender faster, identify requirements that the company can or cannot currently support, find relevant company evidence, identify missing information, and prepare a structured first draft for the bid team.

TenderAI is a decision-support and document-preparation tool. It is not designed to submit a tender automatically or make the final decision on whether a company should bid.

## Inputs

The main input is a tender document in PDF format.

The system also uses documents from a company knowledge base, including:

- company profile information
- certifications and compliance information
- technical capabilities
- previous project references
- tender response guidelines

For the MVP, these knowledge-base documents are synthetic and do not contain real confidential company information.

The system processes the text of these documents and stores searchable representations in a vector database. Based on the synthetic MVP data reviewed, the system does not intentionally process special categories of personal data. A production deployment could involve personal data contained in tender documents or company documents, so this would require separate GDPR/data-protection assessment.

## Outputs

TenderAI produces several types of outputs.

For each tender requirement, it can identify whether the available company evidence is:

- supported
- partially supported
- insufficient

It can also identify missing information and required actions.

The system produces a compliance matrix, an overall bid-readiness assessment, and a recommendation such as whether the tender is ready for final review or requires additional evidence.

It can also generate a Tender Response Blueprint containing tender requirements, available evidence, identified gaps, and suggested response directions.

Users can ask questions through the TenderAI chat interface and receive answers based on the tender analysis and company knowledge base.

## People Affected

The primary users are business-development managers, bid managers, proposal managers, sales engineers, project managers, and consulting teams.

The system may influence internal business decisions, particularly whether a company appears sufficiently prepared to respond to a tender and which requirements require further work.

It is not designed to make decisions about employees, job applicants, customers, or members of the public.

## Human Review

Human review remains part of the workflow.

TenderAI does not automatically submit a bid or make the final commercial, legal, technical, or management decision.

The bid team is expected to review the AI-generated assessments, verify supporting evidence, validate missing information, review the generated response blueprint, and approve the final tender response before submission.

The current MVP does not contain a formal mandatory approval workflow or a dedicated mechanism for recording every human override.

## Who Built It

The system was developed as a Project 3 MVP using Python and a RAG architecture. The main technologies include Streamlit, OpenAI, Pinecone, PDF processing tools, and Python document-generation components.

The AI model and vector database are provided through third-party services that are integrated into the application.

## Intended Production User

In a production deployment, TenderAI would be used by a company's bid, proposal, business-development, engineering, or consulting teams.

The company using the system would provide its own tender documents and company knowledge. The system would support those employees in analysing and preparing responses, while the organisation would remain responsible for validating the information and making the final bid decision.