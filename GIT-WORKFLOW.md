# FoodShield Git Workflow

**Status:** Owner-approved for publication on 2026-11-12. This workflow becomes
active after this document is merged and the approved repository controls are
applied and verified.

**Terminology origin:** `FoodShield Git Workflow`, `task branch`, `publication
gate`, `evidence gate`, and `closeout` are agent-proposed FoodShield workflow
labels. Git concepts such as branch, commit, pull request, review, merge,
ruleset, and status check retain GitHub's meanings.

## Purpose

This procedure keeps `main` recoverable, makes each published change
reviewable, and preserves the owner's decisions and supporting evidence without
pretending that a solo owner can provide an independent GitHub approval.

GitHub permits a ruleset to require a pull request with zero required approvals.
That fits the current solo-owner state because a pull request author cannot
approve their own pull request. The pull request remains the durable change
record, while the owner's explicit approval is recorded in its body or comments.

## Owner-approved repository settings

The following settings are owner-approved. They are applied only after this
documentation is merged, then verified against GitHub's reported state:

| Setting | Current verified state | Proposed FoodShield setting | Source and reason |
|---|---|---|---|
| Changes to `main` | Direct pushes allowed | Require a pull request | GitHub [supports a pull-request rule](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets); using it gives each published change a reviewable record. |
| Required approving reviews | None | Zero | GitHub permits zero approvals in that rule, while a pull-request [author cannot approve their own request](https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request); this avoids deadlock for the current sole authorized reviewer. |
| Conversation resolution | Not required | Required | GitHub [provides this rule](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets); using it prevents merging while a recorded objection or question remains open. |
| Force pushes to `main` | Not blocked | Blocked | GitHub rulesets [block force pushes by default](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets); retaining that protection prevents published history from being replaced. |
| Deletion of `main` | Not restricted by a ruleset | Restricted | GitHub [provides a restrict-deletions rule](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets); using it protects the default branch from accidental deletion. |
| Merge methods | Merge, squash, and rebase allowed | Squash only | GitHub [documents the history effects of each merge method](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/about-merge-methods-on-github); squash-only is the proposed FoodShield adaptation for one coherent mainline commit per pull request. |
| Linear history | Not required | Required | GitHub [provides a linear-history rule](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets); using it prevents future merge commits and makes the mainline easier to read and revert. |
| Automatic head-branch deletion | Disabled | Enabled | GitHub [supports automatic deletion of merged head branches](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-the-automatic-deletion-of-branches); using it removes merged remote task branches. |
| Required status checks | None | Deferred | GitHub [supports required status checks](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets), but no FoodShield CI workflow exists yet, so there is no real check to require. |
| Signed commits | Not required | Deferred | GitHub [supports required commit signatures](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets), but FoodShield has not established signing setup and recovery. |
| CODEOWNERS approval | None | Deferred | GitHub [supports required code-owner review](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets), but no additional authorized reviewer or team exists yet. |

The squash-only and linear-history choices are an agent-proposed adaptation for
FoodShield's current small, task-scoped workflow. GitHub supports multiple merge
methods and does not require this choice.

## Change procedure

### 1. Establish scope

- Start from the latest verified `main`.
- State the owner instruction, intended outcome, owned paths, and unresolved
  decisions.
- For substantive recommendations, identify the authoritative sources and add
  them to `WORKS-CITED.md`.
- Stop for an owner decision when a missing choice would materially change the
  outcome.

### 2. Create the task branch

- Agent branch: `codex/<short-scope>`.
- Use one branch for one coherent task.
- Do not reuse a merged or stale branch for new work.

### 3. Make and verify the change

- Preserve unrelated work.
- Run checks proportional to the change.
- Record what each check proves and what it does not prove.
- Review the exact changed paths and diff.
- Confirm that ignored handoff material, credentials, generated residue, and
  unrelated files are excluded.

### 4. Commit and push the task branch

- Use a short descriptive commit subject.
- A commit must contain one complete, coherent change.
- Push the task branch, never `main`.

### 5. Open the pull request

- Complete `.github/pull_request_template.md`.
- State the problem, material changes, sources, terminology provenance,
  verification, unresolved questions, and exclusions.
- Record the owner's approval date and channel after the owner reviews the
  exact publication package.
- An open pull request is not completion.

### 6. Merge

- Resolve every review conversation.
- Confirm the head commit and remote diff have not changed since approval.
- Use squash merge after the ruleset and repository merge settings are active.
- Do not merge when required evidence failed or a material owner decision is
  unresolved.

### 7. Verify and close out

- Verify the accepted files and expected commit on remote `main`.
- Synchronize the canonical local checkout with remote `main`.
- Confirm the task branch has no unique commits or uncommitted work.
- Delete the merged local task branch. GitHub may automatically delete the
  remote head branch when that repository setting is active.
- Report the final main commit, pull request, verification results, remaining
  ignored or dirty files, and unresolved work.

## Recovery and exceptions

- Correct a published error with a revert or corrective pull request. Do not
  rewrite `main` history.
- A temporary ruleset bypass is not routine authority. If emergency recovery
  genuinely requires one, the owner must authorize it, the exact reason must be
  recorded, and normal protection must be verified afterward.
- Failed checks, merge conflicts, unavailable sources, or missing owner
  decisions remain visible. Do not convert them into implied approval.

## Works Cited

- [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow)
- [Available rules for rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets)
- [Reviewing proposed changes in a pull request](https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request)
- [About merge methods on GitHub](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/about-merge-methods-on-github)
- [Managing automatic deletion of branches](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-the-automatic-deletion-of-branches)
- [Creating a pull request template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository)

Source purposes and limits are retained in `WORKS-CITED.md`.
