# Contributing to emaki

**Thanks for helping.** This guide covers all four repositories. Each repository's own
`CONTRIBUTING.md`, where it has one, goes into its build and checks.

## Where a change belongs

| The change is about | Open it in |
|---|---|
| The shell, its apps, emaki-kit, the look, the docs for users | [emaki](https://github.com/emaki-desktop/emaki) |
| The Rust shell library: windows, popups, services, rendering | [amane](https://github.com/emaki-desktop/amane) |
| The compositor: materials, blur shapes, the desktop layer, IPC | [niri](https://github.com/emaki-desktop/niri) |
| GPU memory in the renderer | [vello](https://github.com/emaki-desktop/vello) |

Not sure? Open it in **emaki** and it will be moved.

## Issues

- Search first; add to an existing issue rather than opening a second.
- For a bug, say what you did, what you expected and what happened, and include the revisions
  you run (the `flake.lock` revs of `emaki` and `niri-fork`, or `niri --version`) and the
  shell's log (`journalctl --user -u emaki -b`).
- Report security problems privately, never in an issue: see the
  [security policy](SECURITY.md).

## Pull requests

- Keep a pull request to one change. Mechanical changes (renames, moves, formatting) go in
  their own commit, apart from the change that needs review.
- Run the repository's checks before you push; CI runs the same ones.
- Update the docs your change affects, and add a line to `CHANGELOG.md` in emaki.
- Diagrams in docs are [Mermaid](https://mermaid.js.org) blocks, not ASCII art.

## The forks

amane, niri and vello are forks kept **thin and rebasable**: a short series of commits on a
tagged upstream base, on the branch `emaki`. That shapes what they take:

- New work goes in new files where it can, so a rebase rarely conflicts.
- Upstream's own files stay as upstream has them, apart from the few each fork's `FORK.md`
  lists.
- Each fork's changes are documented in its `docs/fork/`.
- The forks' changes serve emaki and are **not proposed upstream**. Please don't report
  problems with emaki to the upstream projects; open them here.

## Conduct

Everyone taking part follows the [code of conduct](CODE_OF_CONDUCT.md).
