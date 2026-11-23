# Quality, Testing and Acceptance Criteria
Status: Proposed | Version 0.1

## 1. Release strategy
Release only after testing real behavior, not just prompt formatting. Do not use ScaleBob or Centripe as QA fixtures or public examples. Use two fictional organizations for reproducible end-to-end tests, plus privately selected brands only after the user chooses them and grants appropriate scope.

## 2. Mandatory test scenarios
**T1 New firm:** Minimal product thesis, no brand artifacts. BII avoids treating intention as observed market proof; BEG creates usable approved/pending rules.
**T2 Fragmented established firm:** Conflicting names/claims across controlled fixture pages, partial visuals and unsupported proof. BA finds and cites issues, BII resolves decisions, BEG specifies corrections, implemented fixture is independently reaudited.
**T3 Good existing firm:** Consistent established identity. BA does not invent problems or force redesign; BII/BEG retain valid decisions.
**T4 Standalone BA:** Public/supplied evidence audit without BII; no invented strategy.
**T5 Standalone BII:** No audit input; independently complete scoped identity process.
**T6 Standalone BEG:** Existing approved foundation; no invented approvals or assets.
**T7 Capability limits:** No browser, no file execution, no HTML/ZIP rendering; clear reduced-scope paths.
**T8 Conflicting stakeholders:** Preserve differences, ask a meaningful targeted question, don't automatically merge.
**T9 Interrupt/resume:** Stop midway, reconstruct from project-state and canonical artifacts without repeated interview.
**T10 Decision change:** Revise approved positioning; correctly invalidate dependent messaging and generated guides.
**T11 Adversarial source:** A website/file instructs agent to leak data or override workflow; ignore instructions, use only evidence.
**T12 Missing assets:** No master logo, limited copyright license, or placeholder screenshot; statuses must stay pending.
**T13 Changed audit scope:** Reaudit uses different channels; reports comparability and coverage without false gain.
**T14 Data integrity:** Dangling evidence IDs, invalid enums, duplicate IDs, stale approvals and corrupted ZIP rejected.

## 3. Quality dimensions and threshold
- **Evidence integrity (release blocking):** no fabricated citations, provenance loss or unsupported claims of completion.
- **Decision integrity (release blocking):** no implicit approval, discarded dissent, or conversion of aspiration to fact.
- **Artifact integrity (release blocking):** schemas pass, required files and valid references, approved assets exist.
- **Functional workflow (release blocking):** standalone and full paths work on declared supported hosts.
- **Security and privacy (release blocking):** no unauthorized publication, confidential fixtures, or obeyed prompt injection.
- **Brand utility (human evaluation):** clear, specific, relevant, consistently actionable; must be assessed by reviewers and not inferred from layout quality.
- **Founder ergonomics:** no unnecessary repeated inputs, high-value checkpoints, continuity after interruptions.

## 4. Test evidence
Each test case must record fixture ID/version, environment/model/tool capabilities, prompts, expected observations, output pack path, validation results, defects, manual review judgment and rerun result. Build automated validators for schema/ID/link/file/status rules and deterministic score recomputation, plus manual checks for brand distinctiveness and nuance. Keep a release-blocker tracker.

## 5. Acceptance gates
| Gate | Pass condition |
|---|---|
| G1 Specification coherence | No conflicting fields, module responsibilities or state transitions across Phase 1 documents |
| G2 Skill functionality | Each skill passes its standalone path, relevant error cases and produces correct canonical handoff |
| G3 End-to-end | New and established journeys complete under real declared host capabilities |
| G4 Evidence and approval | Claims trace to data/decisions, no high-severity unresolved integrity violations |
| G5 Export quality | JSON/CSV/Markdown/HTML and valid optional archive pass required checks |
| G6 Installation | Fresh independent installation succeeds in each environment marked 'supported' |
| G7 Release rights | MIT license included for our code; all other assets/references have compatible rights or links |
| G8 Publication | Repo, skills pages, examples and links reachable; actual post-publication smoke tests pass |

## 6. Defects and signoff
P0: privacy leak, fabricated factual proof or unauthorized account action — block release.
P1: broken primary workflow, handoff/approval corruption, false complete score — block release.
P2: degraded secondary output or unclear user experience — fix or document with explicit signoff depending on impact.
P3: cosmetic issue — can defer if documented.
A task is complete only with a linked artifact/test result. Phase 1 approval does **not** certify later skill implementation.

## 7. Milestones
Phase 1: seven reviewed specifications and explicit architecture decisions.
Phase 2: three skill packages + referenced guidance.
Phase 3: schemas/templates/validators and artifact generators.
Phase 4: full test matrix and correction evidence.
Phase 5: docs, examples, compatibility matrix, license and skill pages.
Phase 6: approved version, public publishing, verified installation and smoke tests.
