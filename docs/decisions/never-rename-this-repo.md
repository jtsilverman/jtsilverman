# Never rename this repo

**Picked:** the repository stays named exactly `jtsilverman`, at
`github.com/jtsilverman/jtsilverman`, checked out at `~/Documents/projects/jtsilverman-profile`.

**Rejected:** renaming it to anything clearer, such as `profile` or `profile-readme`.

**Reason:** GitHub renders a profile README only from a repository whose name matches its owner's
username. The name is not a label; it is the mechanism. Rename the repo and the profile page goes
blank.

**What this constrains:**

- The repo name and the directory name differ on purpose. The local checkout is
  `jtsilverman-profile` for legibility; the remote must stay `jtsilverman`. Do not "fix" the
  mismatch by renaming the remote.
- `git remote -v` must keep reading `https://github.com/jtsilverman/jtsilverman.git`.
- This rule sits in tension with the naming rule that governs every other repo here. Catchy
  product-style names beat AI-coded ones, and five repos were renamed on that rule. This one is the
  exception, because its name is load-bearing.

**A related trap, opposite direction:** renaming any repo this README links to is safe on GitHub,
because GitHub redirects the old URL. That safety is why the link edit gets forgotten. A rename and
the matching link edit here are one change. Today `~/Documents/projects/agentdiff` still points its
`origin` at `github.com/jtsilverman/agentdiff` while this README links to `tracediff`; one of the two
is riding a redirect.

**What would reopen it:** GitHub changing how profile READMEs resolve. Nothing else.
