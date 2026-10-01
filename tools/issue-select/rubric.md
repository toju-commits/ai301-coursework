# Rubric: is this a good first issue?

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer-active | Repo facts: last 5 default-branch commits, maintainer first-response sample, and issue comment thread | Pass if there is evidence of recent human maintainer/collaborator activity within the last 90 days, either through commits/merged human PRs or maintainer participation in issues. Bot-only activity does not count by itself. | required |
| repo-in-use | Repo facts: archived flag, latest release, last push to any branch | Pass if the repo is not archived and has had either a release or a nontrivial push within the last 180 days. | required |
| scope-fit | Issue body and comment thread, including whether the issue is a single requested outcome, any umbrella/tracking language, unresolved design discussion, and the history of prior implementation attempts | Pass if the issue asks for one bounded contribution with a clear user-visible outcome. Multiple suspected causes or implementation suggestions may still pass if they address that one outcome. Fail if it is an umbrella/tracking issue, pure support question, has unresolved product/design debate with no settled direction, explicitly requires deep core-internals work, or has multiple abandoned implementation attempts over a long period suggesting hidden complexity. | required |
| unclaimed | Repo facts: assignees and linked PRs; issue comment thread | Pass if there is no current assignee, no open linked PR, and no recent comment clearly stating that someone is actively working on the issue. Closed or abandoned PR attempts do not automatically fail this check. | required |
| ai-policy-compatible | Repo facts: contribution policy; CONTRIBUTING.md / AI policy files when live | Pass if the repo either permits AI-assisted contributions, permits them with conditions, or has no stated restriction. Fail only for an explicit ban on AI-generated or AI-assisted contributions that conflicts with this course workflow. | required |

## Verdict rule

Accept only if every required check passes. Any required check graded fail rejects the issue. Any required check graded unclear also rejects the issue. Preferred checks, if added later, may rank accepted issues but never change the verdict.