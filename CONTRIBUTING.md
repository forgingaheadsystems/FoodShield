# Contributing to FoodShield

**Terminology origin:** The filename, title, section labels, and
FoodShield-specific contribution wording in this file are Codex-proposed
drafting for owner review. Established Git and GitHub terms retain their
external meanings.

FoodShield is in early project-definition work. Application architecture,
module boundaries, and many operational requirements remain unresolved. A
proposal must not present those open decisions as established design.

## Before changing the repository

1. Confirm the intended outcome with the owner.
2. Read `CONTEXT.md`, `GLOSSARY.md`, `TERMINOLOGY-MAP.md`, `AGENTS.md`, and
   `GIT-WORKFLOW.md`.
3. Start from current `main` and create a short-lived branch for one coherent
   task.
4. Do not push directly to `main`.

## Preparing a change

- Keep verified requirements, owner decisions, proposals, inferences, and
  unresolved questions visibly separate.
- Identify terminology introduced by an agent or contributor, even when it is
  adapted from an established term.
- Support substantive recommendations with current authoritative sources and
  preserve those sources in `WORKS-CITED.md`.
- Do not claim compliance or external applicability without evidence for the
  exact organization, activity, program, transaction, and version involved.
- Keep imported handoffs, credentials, local machine details, generated files,
  and unrelated work out of the change.

## Pull requests

Use `.github/pull_request_template.md`. A pull request should state:

- the owner-authorized scope;
- what changed and why;
- terminology provenance;
- authoritative sources and their limits;
- verification actually performed;
- unresolved decisions and excluded work; and
- the owner's publication approval.

FoodShield currently uses a solo-owner review model. The GitHub ruleset is
intended to require a pull request but zero approving GitHub reviews because a
pull request author cannot approve their own change. This does not remove the
requirement for the owner's explicit publication approval.

## After merge

Verify the result on remote `main`, synchronize the canonical local checkout,
and remove only the merged task branch after confirming it has no unique work.
Published errors are corrected through a new pull request or revert, not by
rewriting `main`.

## License

By contributing, you agree that your contribution will be distributed under
the repository's [MIT License](LICENSE).
