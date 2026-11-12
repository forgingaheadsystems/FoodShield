# FoodShield Project Context

**Status:** Existing individual project entering formal repository setup.

## Current authority

- The owner's newest explicit decision controls.
- Verified current repository state and approved project records control present facts.
- The Grok handoff is historical evidence, not project authority.
- External agencies and standards bodies remain authoritative for their own regulated or standardized terminology.

## Canonical locations

- Local repository: `E:\Projects\FoodShield`
- Remote repository: `https://github.com/forgingaheadsystems/FoodShield`
- Default branch: `main`
- Glossary source of record: `GLOSSARY.md`
- Citation register: `WORKS-CITED.md`

The Grok handoff ZIP and extracted folder are retained locally and excluded from Git.

## Glossary bootstrap task

**Title:** Glossary bootstrap and external terminology audit
**Owner approval:** Approved for first publication on 2026-11-12
**Owned paths:** `.gitignore`, `README.md`, `CONTEXT.md`, `GLOSSARY.md`,
`TERMINOLOGY-MAP.md`, and `WORKS-CITED.md`

The owner reviewed the external terminology collisions and approved these paths
as the first publication package. The pull request and Git history preserve the
publication, review, merge, and closeout state.

## First-publication baseline

Verified immediately before publication on 2026-11-12:

- Local branch: `codex/glossary-bootstrap`
- Local `HEAD`, local `main`, and `origin/main`: `7a5eab4` (`Initial commit`)
- Remote: `https://github.com/forgingaheadsystems/FoodShield.git`
- GitHub visibility: public
- Remote branches reported by GitHub: `main` only
- Repository rulesets reported by GitHub: none
- GitHub reports `main` as unprotected
- The local glossary-bootstrap files were untracked and no glossary commit or
  push had occurred at this baseline.
- The Grok handoff ZIP and extracted folder remain local and ignored.

The absence of a ruleset or branch protection is a verified repository fact,
not an approved Git policy. The exact protection settings remain an owner
decision to be made before routine development begins.

## Owner-approved direction

- FoodShield is intended to answer the requested digital-tool features identified in the Sundermeir et al. survey.
- The eventual suite is limited to three to five modules; fewer is preferred.
- Functions that share data or communication channels should be considered together.
- Avoid unnecessary third-party service dependencies.
- Keep the primary interface simple for older users and place complex functions behind the primary workflow.
- Investigate open-source foundations without treating a candidate codebase as selected.
- Use short-lived branches and pull requests instead of developing directly on `main`.
- Identify the provenance of project terminology, including wording proposed by an
  agent even when it adapts, compounds, or conjugates established terminology.
- Use **FoodShield-to-Industry Terminology Map** as the owner-approved name for
  the mapping between FoodShield language and terms controlled by outside
  organizations. The name originated as an agent proposal and was approved by
  the owner on 2026-11-12.

## Unresolved decisions

- Exact module boundaries and names.
- Technical architecture, language, database, and deployment model.
- The operational boundary of “100% no cost.”
- The intended meaning and workflow of communication with emergency services.
- Whether client communications are included in the staff-and-volunteer communication feature.
- Which regulatory, funding, transportation, warehousing, produce-trade, and traceability roles apply to FoodShield itself versus organizations using it.
- Which external identifiers or exchange standards FoodShield must support.
