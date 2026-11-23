# Phase 1 — Architecture and Specification Review

This folder contains seven proposed, cross-referenced specifications for the **ScaleBob Brand Intelligence Kit**.

1. [Product requirements](01-product-requirements.md)
2. [Skill architecture](02-skill-architecture.md)
3. [Shared data contract](03-shared-data-contract.md)
4. [Audit methodology](04-audit-methodology.md)
5. [Founder experience](05-founder-experience.md)
6. [Output specifications](06-output-specifications.md)
7. [Quality and acceptance](07-quality-acceptance.md)

## Decisions already established
- Public open-source GitHub repository `prowlingcipher/scalebob-brand-intelligence-kit`.
- Public name: ScaleBob Brand Intelligence Kit.
- MIT for original project code; third-party reference and asset rights require separate review.
- Three standalone, interconnected skills: Audit, Identity Intelligence, Expression & Guidelines.
- New organizations start at Identity; existing organizations may start with Audit.
- Real-world validation brands to be selected later; ScaleBob and Centripe excluded.
- Publish only after explicit approval; this branch is for design review.

## Decisions recommended for Phase 1 signoff
- Canonical JSON + Markdown with preferred interactive HTML outputs.
- Schema versioning and immutable approval snapshots.
- Scoring is only for observable compliance with separate coverage and strategic-effectiveness fields.
- Proposed seven audit categories and weights are provisional and must be tested before final adoption.
- Runtimes disclose what browsing/file/artifact capabilities are actually available.

## Open implementation work (not completed by this PR)
Machine-enforceable JSON Schemas, installable SKILL.md instructions, validators, tests, interactive HTML generator, fixtures and public skill pages belong to Phases 2–6. This is a specification package, not a working release.
