# Brand Operating Pack — Output Specifications
Status: Proposed | Version 0.1

## 1. General format policy
Canonical machine data: JSON conforming to shared schemas. Editable narrative: Markdown. Human presentation: self-contained HTML where runtime permits, plus optional PDFs. Machine-context: concise BRAND.md and structured brand-rules.json. A ZIP is an export convenience, not the only canonical location. Each generated document includes company, generation date if available, source/foundation version, and approval/completeness status.

## 2. Directory contract (conditional paths noted)
```
company-brand/
  START-HERE.md
  project-state.json
  company-profile.json
  evidence.json
  decisions.json
  01-audit/                 # existing company / audit-run only
    audit-report.md
    audit-report.html       # if rendering available
    audit-findings.json
    findings.csv
    evidence-register.csv
    remediation-plan.md
  02-identity/
    concept-note.md
    representation-note.md
    manifestation-note.md
    brand-foundation.json
    open-questions.md
  03-guidelines/
    brand-guidelines.md
    brand-guidelines.html    # preferred human-facing guide
    messaging-bank.md
    visual-specification.json
    applications.md
    brand-governance.md
  04-assets/
    asset-manifest.json
    asset-inventory.csv
    logos/
    templates/
    imagery/
  05-agent-context/
    BRAND.md
    brand-rules.json
  VALIDATION-REPORT.md
```

## 3. Audit outputs
Report includes executive diagnosis, scope and coverage, scores with calculation basis, sources and dates, uncertainty, high-severity issues, competitor/market observations clearly marked, prioritized remediation and rerun plan. Findings CSV fields include ID, criterion, evidence, severity, affected touchpoint, owner, action, status, verification method. Evidence-register CSV records reproducible locators and capture dates. For no browsing, report must say supplied-material audit, not online audit.

## 4. Identity outputs
- Concept note: company, origin/purpose (as evidenced), products/customers, economics/operating principles, differentiators, contradictions, founder/organizational character, current vs future, uncertainties and validation.
- Representation: external impression hierarchy, relevance to specific audiences, evidence to earn claims, voice/personality boundaries, what must not be implied.
- Manifestation: authentic possible expressions linked to concept truths; tangible examples, failure modes, priority and proof requirement. Ideas remain proposals until approved or demonstrated.
- Canonical foundation: structured approved facts, chosen priorities, audience specifics, proof links, constraints, and unresolved decisions.
Do not require three mechanical revisions; iterate until important claims are approved or labeled unresolved.

## 5. Guidelines outputs
At minimum where applicable: brand basics/naming; positioning and messaging hierarchy; copy bank (tagline, short/long descriptions, social bio, boilerplate, audience adaptations, approved CTAs); voice rules with positive/negative examples; logo rules; palette/contrast; typography; imagery, illustration and motion; application patterns by selected channels; approval, change control, asset rights and maintenance. Sections can be N/A with rationale. Approved source marks or typefaces must not be recreated from guesses.

Interactive HTML guide should provide navigation, responsive layout, copy buttons, visual specimens, status labels, downloadable links only for existing approved files, reduced-motion respect, keyboard functionality, and printable baseline. This is a target, not a promise all hosts will render it.

## 6. Asset production classification
For each asset: `approved|proposed|pending|not_applicable`; ownership, required variants, filename, format, source reference, license, resolution/canvas specifications, reviewer and actual file availability. Never create fake links or represent a placeholder preview as the approved artifact. Export formats must be actually generated/validated before marking approved. Editable masters may require separate human/design-tool work.

## 7. Machine context
`BRAND.md` summarizes approved identity, priority audiences, messaging/voice rules, do/don't, visual constraints, evidence/claims limits and canonical source references. `brand-rules.json` contains structured equivalent; no secret/customer data by default. Agent output should respect approved versus proposed states and remain synced to foundation version. AI cannot be assumed to follow these files unless installed into the receiving system's context.

## 8. Pack integrity
`START-HERE.md` explains status, file map, key decisions, recommended next actions and limitations. `VALIDATION-REPORT.md` lists checks and failures, unresolved decisions, missing assets, version consistency, broken references, manual reviews, and whether the pack is approved or provisional. A valid ZIP must open, contain an index, and match actual files. Do not include confidential work examples in public fixtures.

## 9. Definition of done per output
Report: grounded, scoped, reproducible.
Foundation: consequential claims linked to owner decisions and evidence.
Guidelines: exact approved usage rules or explicit pending states.
Assets: real valid files; approved means available and reviewed.
Pack: schemas validate, links resolve, statuses consistent, documents render/read, no unsupported achievement claims.
