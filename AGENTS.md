# FoodShield Repository Instructions

## Session start

- Load the **company** standards manifest from GitHub `forgingaheadsystems/company-standards` (`Governance/CompanyStandardsManifest.json` on `main`). This product’s `Governance/CompanyStandardsManifest.json` is a **thin pointer** (`companyManifest.uri` + expected version/checksum) — verify it matches; on mismatch, fail closed. Do not treat this product repo as company SoR.
- Load company **OWNER LAW** from company-home `Governance/OwnerLaw.md` (nine-proof done rule; catalog vs company-claims; invent-term / write API/event boundary). Do not copy Owner Law into this product — load from company home.
- Then load this product’s own product SoR (this file’s authority rules, product glossary, and any product write gate such as ActiveWork when the product uses one).
- Prefer the Desktop working copy of company-standards when present and synced; otherwise fetch from the private GitHub company-standards repo with credentials.
- Do not copy company glossary or company doctrine into this product. Company terms live in company-standards; product terms live here.


## Authority and evidence

1. The owner's newest explicit decision is highest authority.
2. This file governs repository work. `CONTEXT.md` records approved project
   direction, `GLOSSARY.md` governs FoodShield terminology, and
   `WORKS-CITED.md` preserves external sources and their limits.
3. Current code, configuration, repository state, and live external state are
   evidence for present facts. The local Grok handoff is historical evidence,
   not project authority.
4. Do not convert a proposal, imported statement, passing check, commit, push,
   or pull request into evidence of owner approval or completion.

## Bounded work

- Before writing, identify one coherent task, its owned paths, the current
  branch, and any unresolved owner decisions.
- Work from current `main` on a short-lived task branch. Agent-created branches
  use `codex/<short-scope>`.
- Do not develop or push directly to `main`.
- Preserve unrelated, ignored, untracked, and user-owned work.
- Do not expand a documentation task into application architecture or a
  standards-applicability decision.

## Terminology and sources

- Follow `GLOSSARY.md` and `TERMINOLOGY-MAP.md`.
- Identify agent-proposed terminology, including adaptations, compounds,
  conjugations, normalized forms, filenames, workflow labels, and ruleset
  names. Do not present those expressions as external requirements.
- Before a substantive recommendation, verify the relevant current official
  source, cite it beside the recommendation, explain why it supports the
  recommendation, and retain it in `WORKS-CITED.md`.
- Keep verified external requirements, owner decisions, proposed FoodShield
  adaptations, inferences, and unresolved questions visibly separate.
- Do not claim regulatory, funding, food-safety, transportation, traceability,
  accessibility, security, or standards compliance without evidence covering
  the exact applicable scope.

## Git publication

- Follow `GIT-WORKFLOW.md`.
- Keep each commit coherent and use a descriptive message.
- Review the exact diff and verification evidence before publication.
- Use a pull request for every change to `main`.
- Record the owner's publication approval in the pull request body or a pull
  request comment before merge. GitHub's required-approval count may be zero
  while FoodShield has only one authorized reviewer.
- Never force-push or delete `main`.
- Prefer a revert through a new pull request over rewriting published history.

## Completion and cleanup

- Completion requires verification on merged remote `main`, not merely a local
  edit, commit, push, or open pull request.
- Report changed paths, checks actually run, unresolved work, branch and pull
  request state, and remaining dirty or ignored files.
- Delete only a merged task branch after verifying that it has no unique work.
- Retain the ignored Grok handoff as local provenance unless the owner gives a
  separate deletion instruction.
