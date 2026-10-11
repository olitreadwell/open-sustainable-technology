# protontypes/open-sustainable-technology context
> refreshed 2026-10-11 | upstream default: main @ 52a5966 (Add Energy Icons (#1669))

## Identity & policies
- upstream: protontypes/open-sustainable-technology. Default branch `main`. Content is one big
  awesome list (`README.md`, 2776 entries) plus `education.md`, `papers.md`, `organizations.csv`,
  `docs/` (mkdocs site). Licence: CC-BY-4.0. English-first: yes (README, CONTRIBUTING, issues all English).
- CLA/DCO: none. No CLA bot, no sign-off requirement in CONTRIBUTING.
- AI-assisted PR policy: allowed, disclosure is optional. The only AI text is one checklist line in
  `.github/pull_request_template.md`: "This pull request contains a significant amount of AI-generated
  content. The human author of the PR has reviewed this content." It is a conditional opt-in box, not a
  mandatory disclosure section (contrast codecarbon, whose AI Usage Disclosure is marked mandatory).
  `docs/how_to_identify_projects.md` recommends LLM prompts for finding missing projects. No ban on AI PRs.
  -> `ai_disclosure_required: false`; repos with a mandatory AI disclosure section stay off-limits.
- signed commits required: no.
- PR template: `.github/pull_request_template.md` (repo level). `protontypes/.github` has only
  CODE_OF_CONDUCT.md, FUNDING.yml, README.md, profile/ - no org default PR template.
- external tracker: GitHub issues only. CONTRIBUTING "Fast Lane": a tip can be filed as an issue.

## Conventions (verified from merged PRs)
- branch naming: `Add-<Project>` dominates merged head refs (Add-Energy-Icons, Add-marola, Add-EarthPV,
  Add-Battery-Data-Format); kebab `type/desc` also seen (fix-dead-links, add-claude-carbon).
- commit style: listing commits are `Add <Project>`; the maintainer squash-merges as `Add <Project> (#N)`.
- entry format: `- [Name](url) - One sentence description.` added at the END of the matching section.
- gate that runs on every PR: `npx awesome-lint@2.1.2` (`.github/workflows/main.yml`).
- outside PRs: merged steadily and fast. 2026-10: PR #1669 opened 2026-10-06, merged 2026-10-07.

## Maintainer picture
- Maintainer: Tobias Augspurger (Ly0n, protontypes). Answers listing suggestions within ~a day and
  merges external "Add X" PRs steadily (10+ in the last 60 days).
- Actively working on: listing additions, and new subsections for open hardware/firmware (see #1613).
- Avoid: rewriting the listing scripts (maintenance_script.py / pr_review.py) - maintainer-owned tooling.

## Issue-area health
- #1613 Add Eco-Libre - MAINTAINER-ENGAGED. Ly0n: "We try to always list git repositories here ...
  It would be very pleased to list projects like: https://github.com/Eco-Libre/life-line". Thread then
  drifted to whether hardware needs a new subsection; the reporter could not help and it stalled. Open.
- #1668 Missing project: Energy Icons - solved by PR #1669 (merged 2026-10-07); issue still open, stale.
- #1629 Suggestion: awesome-ai-tokenomics - no maintainer reply. Not engaged.
- #896 "Review projects with ChatGPT" (help wanted, good first issue) - a bulk research task, not a PR.
- #140/#151/#154/#169 - long-running `research/quant` issues, not small PRs.

## Gap ledger (dedupe - READ FIRST, never re-pick)
- 2026-08-04 self-found dead link LiAISON -> fork PR #1 - pr-opened, closed by maintenance sweep.
- 2026-08-05 self-found 3-link batch -> fork PR #3 - pr-opened, closed / "low-value trivial fix".
- 2026-08-12 self-found LiAISON link -> fork PRs #4 + #5 - closed, "low-value trivial fix".
- 2026-08-19 self-found 3 dead links (LiAISON, UN/CEFACT CRM, GED) -> fork PR #7 - closed, "low-value trivial fix".
- 2026-09-25 / 09-26 / 09-27 scheduled loop -> engine-failure, no trace left (3 runs).
- 2026-10-11 issue #1613 (maintainer-engaged) -> add Eco-Libre Life-Line to "Water Supply and Quality"
  -> fork PR https://github.com/olitreadwell/open-sustainable-technology/pull/13 (branch `Add-Life-Line`,
  base fork `main`, non-draft, 1 commit e39df64, +1 line). Fork CI green (`CI`/Awesome_Lint + fetch). Open.

## Mined gaps (discovered, not yet attempted)
- 2026-10-11 docs `mkdocs.yml` nav points at `blog/the_open_source_sustainability_ecosystem.md` and
  `blog/you_can_preserve_the_earth_s_livability_with_open_source.md`; neither file exists in `docs/blog/`,
  so mkdocs silently drops both nav entries. status: proposed (low value, cosmetic).
- 2026-10-11 CI `.github/workflows/main.yml` + `publish.yml` still use `actions/checkout@v2`
  (Node 20 deprecation warning in fork runs). status: proposed (maintainer-owned CI, small value).
- 2026-10-11 fork artifact only: fork CI fails awesome-lint `awesome-github` because the FORK has no
  topics. Upstream has `awesome` + `awesome-list`. Not an upstream gap. status: dropped.
