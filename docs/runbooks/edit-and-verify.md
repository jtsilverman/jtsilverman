# Edit and verify

## Edit the profile

1. Read `docs/conventions/profile-readme.md` before writing. The posture rules are not in the file
   you are editing.
2. Edit `README.md` on a branch. Never commit to main.
3. Stage the one file:
   ```
   git add README.md
   ```
4. Commit with a plain imperative subject naming the edit.
5. Push the branch and open a PR. Jake merges.

There is nothing to build, install, or test. The repo has one file and no toolchain.

## Verify the render

The profile renders at `https://github.com/jtsilverman` after the merge lands on the default branch.
Check three things there, not in the markdown:

1. Every link resolves. A markdown link to a private repo shows a 404 to a signed-out viewer, which
   is the audience.
2. No section is a wall of text. Every project ends in a `**Stack:**` line, and the rule is 3 to 6
   bullets. Agnes and `kalshi-btc15m` each carry 7 today.
3. The page opens with the name and what Jake builds, with no greeting and no persona line.

Check a link's public visibility while signed out, or in a private window. Signed in as the owner, a
private repo renders as a working link.

## Add a project

1. Pick the category it belongs to: `Production deployments`, `Open-source agents`,
   `Agent development tooling`, `Multi-model evaluation`, or `Editor / context`.
2. Add a `###` heading with the repo name. Link it when the repo is public. When it is private, write
   `**Name** *(private)*` with no link.
3. Write 3 to 6 bullets: what it does, a key technical detail, its scope or scale.
4. End with `- **Stack:** <technologies>`.

## Rename a linked repo

Renaming on GitHub and editing this README are one change, not two.

1. Rename the repository on GitHub.
2. Update the markdown link here in the same pass.
3. Update the local checkout's remote so it stops relying on the redirect:
   ```
   git -C ~/Documents/projects/<dir> remote set-url origin https://github.com/jtsilverman/<new-name>.git
   ```

GitHub redirects the old URL indefinitely in practice, so skipping step 2 leaves a link that works
and a README that lies. Today `~/Documents/projects/agentdiff` still has
`https://github.com/jtsilverman/agentdiff.git` as `origin` while this README links to `tracediff`.

## Do not rename this repo

`git remote -v` must keep reading `https://github.com/jtsilverman/jtsilverman.git`. The profile
render depends on the name. See `docs/decisions/never-rename-this-repo.md`.
