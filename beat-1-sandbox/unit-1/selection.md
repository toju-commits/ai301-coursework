# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/13

**Verdict output**

Evidence gathering is done; here is the graded read-out for the three candidates, all inside the scoped repo codepath/pathreview-ai301-fa26-s1 and measured against today, 2026-10-01.

Ranked read-out

1. #69 — Output parser crashes on a top-level JSON array fallback — ACCEPT
- Fit: this is real backend logic in an AI system (the LLM output parser), in Python, and it matches your "bounded enough to understand, reproduce, test, and complete" line. It touches two files and has an existing xfail test that defines done.
- Crowding: seven-plus classmates have claimed or reproduced it. Under the house rule that does not block it, and I did not let it affect the rank.
- Scope note: thread reproductions show the crash enters from both json.loads call sites (lines 41 and 48), but the existing test only covers the raw-JSON one.

2. #13 — Add an integration test that runs the full RAG pipeline against a mock LLM — ACCEPT
- Fit: it serves your "larger unfamiliar systems" goal, since it spans retrieval, generation and parsing. It ranks second because it is less bounded for a first contribution.
- Why less bounded: it is tier-2 with no good-first-issue label, estimated at 4–6 hours, and you must first design a way to inject a fixed response into ReviewGenerator.
- Crowding: one classmate has claimed it and no PR exists.

Rejected: #18 — Repo analyzer never receives a file list — sunk by unclaimed
- PR #79 by ColonelToad is open, not a draft, and formally closes #18.
- The house rule waives classmates' claim comments only, and says "Everything else in the rubric applies as written." The rubric's "no open linked PR" condition therefore fails.
- The other four checks pass. If you think a classmate's open PR should not block in Path Review, that is a change to make in rubric.md or scope.md.

Repo-level checks (same for all three)

- maintainer-active — pass: Aburke225, a human account and the author of all three issues, has the last five commits on main; the newest is 2026-09-16, 15 days ago.
- repo-in-use — pass: the repo is not archived and was last pushed 2026-09-16. It has no releases, but the rubric accepts a push.
- ai-policy-compatible — pass: docs/CONTRIBUTING.md, docs/SETUP.md, the README and the PR template state no AI restriction, and there is no AI policy file.

One tension the rubric does not penalise: no maintainer has commented in any of the three threads, and the repo has six open PRs with no merged ones. PR #79 itself has no reviews. Course credit attaches to opening the PR, so this matters less here than it would elsewhere.

```json
[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/69",
    "checks": [
      {
        "name": "maintainer-active",
        "grade": "pass",
        "evidence": "Last 5 main commits are by human user Aburke225 (also the issue author), newest 2026-09-16, 15 days before 2026-10-01."
      },
      {
        "name": "repo-in-use",
        "grade": "pass",
        "evidence": "archived: false; last push 2026-09-16T21:48:27Z (within 180 days); no releases published."
      },
      {
        "name": "scope-fit",
        "grade": "pass",
        "evidence": "One bounded outcome: \"The fallback path should handle array responses\"; two files, est. 2-4 hours, labels good first issue / tier-1; no implementation PRs in this repo."
      },
      {
        "name": "unclaimed",
        "grade": "pass",
        "evidence": "No assignee and no open linked PR (only cross-reference is a PR in another user's own repo); all claim comments are from classmates (association NONE), ignored per the Path Review house rule."
      },
      {
        "name": "ai-policy-compatible",
        "grade": "pass",
        "evidence": "docs/CONTRIBUTING.md, docs/SETUP.md, README and PR template state no AI restriction; no AI_POLICY.md or AGENTS.md exists."
      }
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/13",
    "checks": [
      {
        "name": "maintainer-active",
        "grade": "pass",
        "evidence": "Last 5 main commits are by human user Aburke225 (also the issue author), newest 2026-09-16, 15 days before 2026-10-01."
      },
      {
        "name": "repo-in-use",
        "grade": "pass",
        "evidence": "archived: false; last push 2026-09-16T21:48:27Z (within 180 days); no releases published."
      },
      {
        "name": "scope-fit",
        "grade": "pass",
        "evidence": "One bounded outcome: add one @pytest.mark.integration test running retrieval, generation and parsing against a fixed response; est. 4-6 hours, tier-2; no umbrella language, design debate or abandoned PRs."
      },
      {
        "name": "unclaimed",
        "grade": "pass",
        "evidence": "No assignee and no linked PR (only cross-reference is closed issue #43); the single claim comment is from classmate Elias0305Ha, ignored per the Path Review house rule."
      },
      {
        "name": "ai-policy-compatible",
        "grade": "pass",
        "evidence": "docs/CONTRIBUTING.md, docs/SETUP.md, README and PR template state no AI restriction; no AI_POLICY.md or AGENTS.md exists."
      }
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/18",
    "checks": [
      {
        "name": "maintainer-active",
        "grade": "pass",
        "evidence": "Last 5 main commits are by human user Aburke225 (also the issue author), newest 2026-09-16, 15 days before 2026-10-01."
      },
      {
        "name": "repo-in-use",
        "grade": "pass",
        "evidence": "archived: false; last push 2026-09-16T21:48:27Z (within 180 days); no releases published."
      },
      {
        "name": "scope-fit",
        "grade": "pass",
        "evidence": "One bounded outcome: GitHubTool must supply a file list under file_structure so has_tests and has_ci are correct; two files, est. 2-4 hours, labels good first issue / tier-1."
      },
      {
        "name": "unclaimed",
        "grade": "fail",
        "evidence": "Open, non-draft PR #79 by ColonelToad (created 2026-09-29) formally closes #18; the house rule waives claim comments only, not open linked PRs."
      },
      {
        "name": "ai-policy-compatible",
        "grade": "pass",
        "evidence": "docs/CONTRIBUTING.md, docs/SETUP.md, README and PR template state no AI restriction; no AI_POLICY.md or AGENTS.md exists."
      }
    ],
    "verdict": "reject"
  }
]
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

`agreement: 3/3 scored items`

`agreement: 18/20 scored items  (bar: 18/20: PASS)`

`agreement: 2/2 scored items`

`agreement: 20/20 scored items  (bar: 18/20: PASS)`

**Issue analysis**

`issue-19`

Rubric decision: `reject`

Gold label: `accept`

The first full run reported:

`issue-19  accept  reject   NO     failed: scope-fit`

My original `scope-fit` check rejected this issue because it described two possible causes of the same performance problem and several possible implementation approaches. I treated the number of technical paths as evidence that the task was too broad.

After reviewing the disagreement, I realized that all of those paths were still directed at one bounded user-visible outcome: preventing the UI from freezing when selecting large subgraphs in proof mode. The issue therefore exposed a weakness in my definition of scope rather than a problem with the issue itself.

I revised `scope-fit` so that multiple suspected causes or implementation suggestions can still pass when they all serve one clearly defined outcome.

**Check rationale**

Current `scope-fit` check from `rubric.md`:

> `| scope-fit | Issue body and comment thread, including whether the issue is a single requested outcome, any umbrella/tracking language, unresolved design discussion, and the history of prior implementation attempts | Pass if the issue asks for one bounded contribution with a clear user-visible outcome. Multiple suspected causes or implementation suggestions may still pass if they address that one outcome. Fail if it is an umbrella/tracking issue, pure support question, has unresolved product/design debate with no settled direction, explicitly requires deep core-internals work, or has multiple abandoned implementation attempts over a long period suggesting hidden complexity. | required |`

I wrote the check this way because a first contribution should have a clearly bounded result without requiring every implementation detail to be predetermined. An issue can name several suspected causes and still be appropriately scoped if they all contribute to the same outcome.

I also added the history of abandoned implementation attempts as evidence because `issue-15` showed that an issue can appear newcomer-friendly while years of unsuccessful attempts reveal hidden complexity that is not obvious from the label or issue description alone.

**Trade-offs**

This version of `scope-fit` is more permissive toward issues that list several technical causes or possible implementation strategies. The trade-off is that it can accept an issue whose implementation turns out to be more technically complex than its single stated outcome initially suggests.

I tested this trade-off directly by rerunning `issue-15` and `issue-19` after revising the check. The revised rubric correctly separated the two cases: `issue-19` became `accept` because its multiple technical ideas still served one bounded outcome, while `issue-15` remained `reject` because its long history of design discussion and abandoned implementation attempts suggested hidden complexity.

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

1. **Fit to my interests and the time available**

   I selected issue #13 because it gives me experience across the full RAG pipeline rather than limiting the contribution to one isolated function. The issue involves retrieval, generation, output parsing, integration testing, and mocking an LLM response. That lines up closely with the AI and backend systems work I want to become stronger at.

   It is estimated at 4–6 hours, which is larger than issue #69, but it is still bounded enough to complete within the course. The expected deliverable is also concrete: add an integration test that sends a query through retrieval, generation, and parsing using a fixed mock LLM response.

2. **What the verdict identified correctly and what I weighed outside the rubric**

   The verdict correctly identified that the repository is active, the issue describes one bounded outcome, there is no blocking linked pull request, and the repository has no AI-use restriction.

   The skill ranked #69 above #13 because #69 is a smaller and more immediately bounded first contribution. I decided to choose #13 anyway because my fit profile is not only about minimizing difficulty. I also want experience understanding larger unfamiliar systems and seeing how different parts of an AI application work together.

   The rubric does not directly measure the long-term learning value of one accepted issue compared with another. For me, learning how to test an entire RAG pipeline and make an LLM-dependent component testable is more valuable than taking the smallest accepted bug.

3. **Anticipated difficulty in claiming it**

   One classmate has already posted a claim comment on issue #13, but the Path Review house rule says that classmate claim comments do not block an issue. There is currently no linked implementation pull request, so the issue still passes my `unclaimed` check.

   I expect the larger challenge to be technical rather than procedural. `ReviewGenerator` currently constructs its own OpenAI client, so I will need to understand that code and determine a clean way to inject a fixed response for the integration test. I will need to keep that change scoped so the contribution does not grow into an unnecessary refactor.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.