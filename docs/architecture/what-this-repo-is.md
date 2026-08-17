# What this repo is

Say it in one sentence: one markdown file that GitHub renders at the top of
`github.com/jtsilverman`.

## The mechanism

GitHub renders `README.md` from a repository whose name matches its owner's username onto that
owner's profile page. This repo pushes to `github.com/jtsilverman/jtsilverman`, so its `README.md` is
the profile. The rendering is automatic and depends on the repo name matching exactly. See
`docs/decisions/never-rename-this-repo.md`.

## The whole repo

`README.md`. That is the only tracked file; `git ls-files` returns it alone. There is no build, no
test, no CI workflow, no `.gitignore`, and no dependency.

## The shape of the file

A one-line opener naming what Jake builds, then his role and one credential, then the projects
grouped into five categories, then contact. `grep -n '^## ' README.md` returns six headings: the five
categories plus `Contact`.

| Section | Holds |
|---|---|
| Opener | What he builds. Two sentences: the work, then role plus the PwC Transfer Pricing AI competition win |
| Production deployments | Rock, Agnes, kalshi-btc15m |
| Open-source agents | travel-concierge, gridplay |
| Agent development tooling | tracediff, proxyprof, policygrade, probe |
| Multi-model evaluation | council, browser-bench |
| Editor / context | ctxpeek |
| Contact | Email and LinkedIn |

Each project is a `###` heading followed by bullets, the last one always
`**Stack:** <technologies>`. All twelve projects end on a `**Stack:**` bullet. The rule is 3 to 6
bullets; ten projects hold to it and two do not, which the table below records.

## Where the current file departs from its own rules

The governing rules are in `~/Documents/projects/Employment/.claude/rules/employment.md`. Two
departures are visible in the file itself:

| Rule | The README |
|---|---|
| A private repo gets a bold name only, no markdown link, because linking a private repo 404s for a cold viewer | Rock and Agnes follow it. `kalshi-btc15m` is tagged `*(private)*` **and** wrapped in a markdown link to `github.com/jtsilverman/kalshi-btc15m` |
| Each project section is 3 to 6 bullets | Ten projects hold. Agnes has 7 and `kalshi-btc15m` has 7 |
| Job-search-facing surfaces use `jakesilverman.pro@gmail.com`, never the personal address | Contact reads `jtsilverman8@gmail.com` |

Bullet counts by project: Rock 6, Agnes 7, kalshi-btc15m 7, travel-concierge 5, gridplay 5,
tracediff 5, proxyprof 5, policygrade 5, probe 3, council 5, browser-bench 5, ctxpeek 4.

The email one is a genuine conflict, not an oversight to fix on sight. The Employment rule scopes
itself to "CV, cover letters, outreach" and does not name the profile README, and the
profile-README-posture section says nothing about contact details. Whether a public GitHub profile
counts as job-search-facing is Jake's call. Recorded here rather than resolved.

## The rename history

Four repos were renamed away from AI-coded names in `4f4f40d`, and one in `1b472e1`:

| Was | Is |
|---|---|
| `agentdiff` | `tracediff` |
| `arc-playground` | `gridplay` |
| `copilot-guard` | `ctxpeek` |
| `mcpprof` | `proxyprof` |
| `skillscore` | `policygrade` |

The local working directory is still `~/Documents/projects/agentdiff`, and its `origin` still points
at `https://github.com/jtsilverman/agentdiff.git`, while this README links to
`github.com/jtsilverman/tracediff`. GitHub redirects a renamed repository's old URL, so a stale
`origin` keeps working and both facts can be true at once. Confirm which name is live before trusting
either. Renaming a repo on GitHub without updating the README link here leaves a link that works only
while the redirect holds.
