# Product Requirements Document — Phase 1
Status: Proposed for review | Product: ScaleBob Brand Intelligence Kit | Version: 0.1

## 1. Purpose
An open-source, AI-assisted workflow that helps organizations investigate, discover, validate, operationalize and maintain an evidence-grounded brand. Three independently usable skills share a versioned project contract: Brand Audit (BA), Brand Identity Intelligence (BII), and Brand Expression & Guidelines (BEG). This is not a SaaS application or a guarantee of commercial brand performance.

## 2. Audiences and entry paths
- **New organization:** BII → BEG. Founders may have only a thesis, team and proposed customer. Evidence scarcity must be explicit.
- **Established organization:** BA → BII → BEG → actual implementation → BA reaudit. The initial audit cannot be counted as remediation.
- **Existing strategy, no audit:** BEG standalone with intake validation; if foundations are contradictory, pause for decisions or refer to BII.
- **Audit only:** BA standalone without requiring adoption of identity or guidelines.
- **Established brand requiring clarification:** BII standalone, using existing approved evidence and leadership input.
- **Guidelines maintenance:** BEG can update a previous approved guide without redesigning every element.

## 3. Core design principles
1. Evidence before narrative; distinguish observed fact, participant assertion, inference, aspiration, and unknown.
2. Consequential brand decisions require owner approval; silence is not approval.
3. Adaptive depth: ask questions only when their answers materially affect outputs.
4. No forced reinvention: valid existing identity and assets may remain unchanged.
5. Stable handoffs; no redundant questioning and no dependence on a particular chat session.
6. No fabricated proof, brand assets, social posts, customer quotes, metrics, or client outcomes.
7. A standalone mode must not require other skills or proprietary infrastructure.
8. Respect confidentiality, ownership, accessibility, and intellectual-property constraints.

## 4. Functional requirements
| ID | Requirement | Acceptance evidence |
|---|---|---|
| FR-01 | Determine entry mode, scope, channels, objectives, and accessible tools from concise intake | Each test scenario obtains a valid path |
| FR-02 | Record an evidence inventory with dated, retrievable references and coverage limitations | Source-to-claim traceability |
| FR-03 | BA discovers relevant web touchpoints, conflicting claims, visuals and missing rules | Each finding linked to evidence and rubric criterion |
| FR-04 | BA yields coverage, compliance score, strategic observations, and remediation tickets distinctly | No unsupported 100/100 claim |
| FR-05 | BII produces first-pass understanding from supplied evidence | Hypotheses marked unverified |
| FR-06 | BII generates situational, adversarial questions and captures independent stakeholder input | Questions target gaps/tradeoffs rather than generic agreement |
| FR-07 | BII distinguishes actual, chosen, aspirational brand; validates audience relevance and market distinctiveness | Explicit evidence/confidence and counterarguments |
| FR-08 | BII generates approved concept, representation, manifestation and canonical foundation | All normative decisions have approval records |
| FR-09 | BEG produces verbal identity, visual identity, applications and governance as applicable | Required categories populated or legitimately N/A/pending |
| FR-10 | BEG tracks asset status and never invents approved artwork or claims | Reviewable asset manifest |
| FR-11 | Generate human-readable and machine-readable Brand Operating Pack | File manifests and schema validation |
| FR-12 | Preserve provenance, approvals and session state for resumption and skill handoff | Interruption/restart tests |
| FR-13 | Reaudit against comparable criteria, documenting actual published changes | Before/after evidence, non-comparable cases identified |
| FR-14 | Run in tested skill-capable environments with graceful degradation | Tested compatibility matrix, documented fallback |

## 5. Out of scope for v1
- Autonomous publishing or modifying third-party accounts without explicit, scoped authorization.
- Guaranteed logo generation, editable design-source production, full website implementation, or automated global asset changes.
- A proprietary hosted web app, user database, scheduled monitoring, legal trademark clearance, or an objective prediction of brand-market success.
- Treating private uploads as permission for public distribution.

## 6. Canonical journey
Intake → evidence collection → draft findings/hypotheses → targeted decisions → explicit validation → approved structured handoff → guidelines/assets → implementation (outside skill unless tools available) → independent reaudit. For new businesses omit initial audit. Each stage offers: completed work, evidence, uncertainties, current decision, next action.

## 7. Experience requirements
Default founder interaction is conversational and short. Ask at most one tightly related decision batch (typically 3–5 questions) per checkpoint. Use multiple choice where trade-offs matter; permit 'none', multi-select/ranking, free text, and deferral. Do not turn a rank-order problem into a single-select question. Reuse known answers and record disagreements, not manufactured consensus. Allow 'good enough to proceed provisionally' but never mark provisional decisions approved. Provide a concise recap after each checkpoint.

## 8. Output success
A completed journey results in a portable Brand Operating Pack with START-HERE, canonical JSON, audit (if applicable), approved identity, guidelines, assets inventory, and machine-readable agent rules. The pack should allow an unfamiliar person to determine what is approved, what requires production, why decisions were made, and what to do next.

## 9. Outcomes and telemetry without a SaaS backend
User-side evaluation: completion without outside assistance, percent of claims with traceable evidence, major decision reversals, unanswered critical questions, deliverable validity, consistency of derived copy, fresh-install success, and audit reproducibility. No automatic data collection or analytics is required.

## 10. Launch gate
All release-blocking acceptance cases in `07-quality-acceptance.md` pass in declared environments. Real brands may be used later by their owners; ScaleBob and Centripe are excluded from public fixtures and real-world validation.
