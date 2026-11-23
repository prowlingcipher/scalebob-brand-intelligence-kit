# Shared Data Contract — Data, State and Handoffs
Status: Proposed | Version: 0.1 | Schema family: `1.0.0-draft`

## 1. General invariants
Every artifact: `schema_version`, `project_id`, `artifact_type`, `updated_at` (ISO-8601 where available), `status`, `source_ids` and `version`. Use durable IDs (`EV-...`, `BA-...`, `DEC-...`, `AS-...`). No duplicate IDs; do not reuse IDs after deletion. Links to source IDs must resolve. Unknown values are explicit null/status, never guessed.

## 2. Core files
**company-profile.json**
`project_id`, legal/display name, URLs, geography (if known), industry (if known), audience segments, stage (`new|established|transitioning|unknown`), operating context, owner labels, restricted/public data markings, and audit scope.

**evidence.json**
Records: `id`, `source_type` (public_url, supplied_file, stakeholder_statement, observation, external_research), `locator`, `captured_at`, `accessed_at`, `source_owner`, `summary`, `quote_excerpt` (optional short quote), `claim_ids`, `reliability` (high/medium/low/unknown), `availability`, `sensitivity`, `limitations`. Observations can be stale. Stakeholder statements are not independent market proof.

**decisions.json**
`id`, `question`, `chosen_option_or_text`, `alternatives`, `rationale`, `evidence_ids`, `status` (`proposed|approved|rejected|deferred|superseded`), `approver`, `approved_at`, `supersedes`, `affected_artifacts`. Conflicting stakeholder answers remain distinct until reconciled or documented.

**project-state.json**
`project_id`, `current_skill`, `current_stage`, `stage_status`, `completed_gates`, `blocked_on`, `next_actions`, `input_artifact_versions`, `output_artifact_versions`, `environment_capabilities`, `open_questions`, `last_verified`. It is a resume pointer, not the sole record of truth.

**brand-foundation.json**
Company identity (description, purpose, beliefs); actual/chosen/aspirational distinctions; strategic ambition; audiences and needs; market differentiators and evidence levels; personality; voice principles; representation priorities; manifestation territories; exclusions; uncertainties; approved decision references. Each normative claim has `evidence_ids`, `decision_ids`, `validation_state`.

**audit-findings.json**
Audit ID, rubric version, scope, coverage, baseline score/method, findings. Finding: `id`, `criterion_id`, `description`, `severity`, `touchpoint_ids`, `evidence_ids`, `impact`, `recommendation`, `owner_module`, `remediation_status`, `verification_evidence_ids`, `resolution_decision_ids`. Do not delete resolved findings.

**asset-manifest.json**
Assets: `id`, `category`, `name`, `file_path`, `format`, `status` (`approved|proposed|pending|not_applicable`), `source_asset_ids`, `license_info`, `usage_rules`, `required_variants`, `reviewer`, `last_reviewed`. Absence of a file cannot equal approved.

## 3. Provenance contract
Each significant brand assertion is one of: `observed`, `stakeholder_asserted`, `inferred`, `aspirational`, `unknown`. It also has evidence links and confidence (high/medium/low or unknown). Approvals validate **the organizational choice**, not empirical truth of market differentiation. Do not promote inferred traits to observed facts based solely on a founder clicking 'approve'.

## 4. Handoff rules
BA → BII: transmit scoped findings, evidence, unresolved strategic questions and original scores. BII must preserve BA IDs and mark its resolutions by ID.
BII → BEG: hand off approved foundation and open uncertainties, not a silently flattened narrative. Proposed or unresolved positions cannot be emitted as approved public messaging.
BEG → BA reaudit: transmit approved rules, target touchpoints and actual implementation evidence (when present). Updated guide alone is not a fixed live touchpoint.

## 5. Change propagation
When a decision changes: record new decision version, mark prior decision superseded, recompute dependencies, flag affected generated documents/assets for review, and keep historical audit evidence. Approved versions are immutable snapshots; generated HTML and Markdown must disclose their foundation version.

## 6. Schema validation implementation notes
Phase 2 must supply machine-enforceable JSON Schemas, example passing/failing fixtures, and a validator for: required keys, enum values, unique IDs, valid references, status transitions, empty strings, date formatting, forbidden approvals, and stale dependencies. The specification here defines semantics, not yet executable schema files.

## 7. Example finding (fictional)
```json
{"id":"BA-001","criterion_id":"POS-02","description":"Conflicting category claims",
 "severity":"high","evidence_ids":["EV-001","EV-002"],
 "owner_module":"brand-identity","remediation_status":"open"}
```
The actual schema will require additional fields and will not permit this abbreviated sample as a finished handoff.
