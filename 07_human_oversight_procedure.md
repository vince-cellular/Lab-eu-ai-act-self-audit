# TenderAI Assistant — Human Oversight Procedure

## Purpose

This procedure defines how human reviewers should review, validate, and approve AI-generated TenderAI outputs before they are relied upon for a final tender submission.

TenderAI is a decision-support and document-preparation system. It does not replace the professional judgement or final decision-making responsibility of the client organisation.

---

## 1. When Human Review Is Required

Human review is required before:

- a bid-readiness recommendation is treated as final;
- a tender requirement is considered satisfied;
- supporting company evidence is relied upon in a final response;
- an AI-generated Tender Response Blueprint is used as the basis for the final bid;
- technical, legal, commercial, contractual, or pricing statements are included in the final submission.

TenderAI outputs should be treated as draft or decision-support material until reviewed.

---

## 2. Who Performs the Review

The client organisation should assign an appropriate reviewer depending on the type of information.

| Output / Information | Suggested Reviewer |
|---|---|
| Overall bid readiness | Bid Manager / Business Development Manager |
| Technical evidence | Technical / Engineering specialist |
| Project references | Project Manager / Bid Manager |
| Certifications | Quality / Compliance specialist |
| Legal or contractual statements | Legal / Contract specialist |
| Commercial or pricing information | Commercial / Finance specialist |
| Final submission | Authorised Bid Manager / Management |

The same person may perform multiple review roles in a small organisation, provided they have the appropriate knowledge and authority.

---

## 3. What the Reviewer Must Check

For each material AI-generated assessment, the reviewer should check:

### Evidence

- Does the cited company evidence actually exist?
- Does the evidence support the requirement?
- Is the evidence current?
- Is the source appropriate for the claim?

### AI Interpretation

- Has TenderAI interpreted the evidence correctly?
- Has the AI added information that is not present in the source?
- Has uncertainty been represented correctly?

### Requirement Assessment

- Is the requirement correctly understood?
- Is the classification of supported, partially supported, or insufficient reasonable?
- Are mandatory requirements correctly identified?

### Missing Information

- Are the identified gaps accurate?
- Is additional evidence actually required?

### Generated Response

- Does the draft response accurately represent the company?
- Are technical claims correct?
- Are legal or contractual commitments appropriately reviewed?
- Has any unsupported claim been introduced?

---

## 4. Review Decision

The reviewer should record one of three outcomes:

### APPROVED

The reviewer has verified the relevant evidence and accepts the AI-generated assessment for use in the next stage.

### APPROVED WITH MODIFICATIONS

The reviewer accepts the general assessment but has corrected or modified part of the AI output.

### REJECTED

The reviewer considers the AI output unreliable, unsupported, incomplete, or otherwise unsuitable for use.

A rejected output must not be used as verified evidence for the final tender response.

---

## 5. Override Procedure

If a reviewer disagrees with a TenderAI recommendation, the reviewer should record:

- the original AI recommendation;
- the reviewer's decision;
- the reason for the override;
- the evidence supporting the override;
- the reviewer's role;
- the review date.

Example:

**AI recommendation:** INSUFFICIENT

**Human decision:** PARTIALLY SUPPORTED

**Reason:** The AI did not retrieve the most recent project reference document.

**Evidence:** Renewable Energy Project Reference — 2026 project record.

**Reviewer:** Bid Manager

**Date:** [DATE]

---

## 6. Final Bid Responsibility

TenderAI must not be treated as the final decision-maker.

The client organisation remains responsible for:

- deciding whether to submit a bid;
- verifying technical claims;
- verifying certifications;
- approving commercial information;
- approving legal and contractual statements;
- approving the final tender response;
- submitting the final tender.

An AI-generated recommendation must not by itself constitute approval to submit a tender.

---

## 7. Evidence Traceability

Where technically possible, each material TenderAI assessment should retain or display:

- tender requirement ID;
- source document;
- source page or location;
- extracted evidence;
- AI assessment;
- human review status;
- reviewer;
- review date;
- override reason where applicable.

This creates a traceable path from:

**Tender requirement → Company evidence → AI assessment → Human verification → Final response**

---

## 8. Handling Uncertainty

If the reviewer cannot verify an AI-generated statement, it must not be treated as confirmed company evidence.

The reviewer should classify the information as:

**UNVERIFIED**

and request additional evidence from the relevant internal owner.

TenderAI should not be used to fill evidence gaps with assumptions.

---

## 9. Escalation

The reviewer should escalate the issue to the appropriate specialist when:

- a legal interpretation is required;
- a contractual commitment is involved;
- technical compliance is uncertain;
- certification status is unclear;
- personal data concerns arise;
- the AI output materially conflicts with authoritative company records.

Possible escalation contacts include:

- Legal / Contract team;
- Data Protection Officer;
- Technical specialist;
- Quality / Compliance team;
- Bid Director;
- Information Security team.

---

## 10. Minimum Review Record

A production implementation should capture at least:

| Field | Example |
|---|---|
| Tender | Offshore Wind Tender |
| Requirement ID | REQ-012 |
| AI assessment | PARTIALLY SUPPORTED |
| Evidence reviewed | Technical Capabilities.pdf, p. 4 |
| Human decision | APPROVED WITH MODIFICATIONS |
| Reviewer role | Bid Manager |
| Reviewer | [NAME / ROLE] |
| Review date | [DATE] |
| Override reason | [IF APPLICABLE] |
| Final status | [STATUS] |

---

## 11. Principle

The operating principle for TenderAI is:

> **AI assists. Evidence supports. Humans decide.**

TenderAI may accelerate analysis and preparation, but the client organisation remains responsible for validating information and making the final bid decision.