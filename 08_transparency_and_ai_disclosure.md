# TenderAI Assistant — Transparency & AI Disclosure Specification

## Phase 8 — Article 50 Transparency Control

This document defines the transparency control required for the current TenderAI MVP based on the Phase 4 obligation assessment and Phase 5 remediation plan.

This is a first-pass compliance implementation specification. It is not a legal opinion or final legal determination.

---

# 1. Objective

TenderAI provides an interactive AI assistant through which users can communicate with an AI system.

The purpose of this control is to ensure that users are clearly informed that they are interacting with an AI system where the applicable EU AI Act transparency requirement applies.

The control should be implemented directly in the TenderAI user interface.

---

# 2. Relevant Requirement

## EU AI Act — Article 50(1)

TenderAI's chat interface is designed for direct interaction between a natural person and an AI system.

The production interface should therefore provide a clear disclosure that the user is interacting with an AI system, unless the AI nature of the interaction is already obvious from the circumstances and context.

---

# 3. Current System

TenderAI currently provides:

- an interactive TenderAI chat interface;
- AI-generated answers;
- AI-generated tender assessments;
- AI-generated compliance explanations;
- AI-generated bid-readiness recommendations;
- AI-generated Tender Response Blueprint content.

The AI functionality is provided through an external AI/model service integrated into the TenderAI application.

---

# 4. Identified Gap

## Current state

The current MVP documentation does not establish that a clear AI disclosure is displayed to users before or at the beginning of their interaction with the TenderAI assistant.

## Gap status

**OPEN — TRANSPARENCY CONTROL REQUIRED**

---

# 5. Required Control

TenderAI should display a visible notice informing users that they are interacting with an AI-powered assistant.

The notice should be:

- clear;
- easy to understand;
- visible to the user;
- presented before or at the beginning of the interaction;
- associated clearly with the AI assistant.

---

# 6. Proposed User-Facing Disclosure

Recommended wording:

> **AI Assistant Notice**
>
> You are interacting with TenderAI, an AI-powered assistant. Its responses are generated using artificial intelligence and should be reviewed and verified by an appropriate member of the bid team before being relied upon for a tender submission.

The final wording should be reviewed before production deployment.

---

# 7. Recommended Interface Placement

The disclosure should appear in at least one prominent location associated with the TenderAI assistant.

Recommended implementation:

```text
+--------------------------------------------------+
| TenderAI Assistant                               |
|                                                  |
| AI Assistant Notice                              |
| You are interacting with TenderAI, an            |
| AI-powered assistant. Responses should be        |
| reviewed and verified by the bid team.           |
|                                                  |
| ------------------------------------------------ |
|                                                  |
| Ask TenderAI a question...                       |
|                                                  |
+--------------------------------------------------+