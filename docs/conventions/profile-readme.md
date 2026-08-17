# Profile README conventions

One answer per question. A reviewer can reject an edit from this file alone.

The source of these rules is
`~/Documents/projects/Employment/.claude/rules/employment.md`, section "GitHub profile-README
posture". This file points at that one and adds what the README's own history shows.

## Posture

Portfolio, not a personal blog. Lead with the name, what Jake builds, and the role. Then projects.
Then contact.

Three things are banned by the rule:

| Banned | History |
|---|---|
| A greeting like "Hi I'm Jake" | Was in the README, removed in `263fd01` |
| "Day: / Off-hours:" framing | Was in the README, removed in `263fd01` |
| A persona opener like "treats engineering like a sport" | Never appeared in this README. The rule names it to keep it out |

## Bullets, not paragraphs

Each project is a `###` heading and 3 to 6 bullets. Never a paragraph. `d886ffb` compressed the file
to one-line bullets and `ccfba4f` converted the last per-project paragraphs.

Two projects break the ceiling today: Agnes has 7 bullets and `kalshi-btc15m` has 7. Cut them to 6
when either section is next edited.

The last bullet of every project is always:
```
- **Stack:** <comma-separated technologies>
```

A bullet names what the thing does, a key technical detail, or its scope and scale. It does not sell.

## Categories

Projects group under one of five `##` headings, separated by `---`:

`Production deployments`, `Open-source agents`, `Agent development tooling`,
`Multi-model evaluation`, `Editor / context`.

`Contact` is a sixth `##` heading and is not a category.

A new project joins an existing category or earns a new one. It never sits uncategorized.

## Repo naming

Catchy product-style names beat AI-coded ones. Avoid `agent`, `AI`, and `Claude` in a repo name; let
the description carry the AI angle. Five repos were renamed on that rule:

| Was | Is |
|---|---|
| `agentdiff` | `tracediff` |
| `arc-playground` | `gridplay` |
| `copilot-guard` | `ctxpeek` |
| `mcpprof` | `proxyprof` |
| `skillscore` | `policygrade` |

A rename on GitHub needs the matching link edit here in the same pass. GitHub redirects the old URL,
so a stale link keeps working and the drift stays invisible until the redirect lapses.

## A private repo gets no link

```
**Name** *(private)*: description
```

Bold name, the `*(private)*` tag, no markdown link. A link to a private repo 404s for a cold viewer,
which is the whole audience.

Rock and Agnes follow this. `kalshi-btc15m` is tagged `*(private)*` and still carries a markdown
link, which is a departure recorded in `docs/architecture/what-this-repo-is.md`.

## Never rename this repo

The profile-README auto-render only works while the repo is named exactly `jtsilverman`. See
`docs/decisions/never-rename-this-repo.md`.

## Voice

Literal, not fluffy. Real numbers and concrete technology names only. Never invent a metric; reword
the sentence to drop the quantity rather than keep it because it sounds impressive.

No em dashes anywhere in the body. Use `--`.

## Git

Commit subjects are plain imperative sentences describing the edit: `Convert per-project paragraphs
to bullets`, `Drop greeting and Day/Off-hours framing`. No conventional-commit prefix.

Branch per task, Jake merges the PR. Never commit to main. Stage with `git add <file>`.
