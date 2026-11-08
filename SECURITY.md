# Security policy

**Report vulnerabilities privately.** Never in a public issue or pull request.

## Reporting

Use GitHub's private vulnerability reporting on the repository the bug is in: its
**Security** tab, then **Report a vulnerability**.

| The bug is in | Report it at |
|---|---|
| The shell or its apps | [emaki](https://github.com/emaki-desktop/emaki/security) |
| The library | [amane](https://github.com/emaki-desktop/amane/security) |
| The compositor fork | [niri](https://github.com/emaki-desktop/niri/security) |
| The renderer fork | [vello](https://github.com/emaki-desktop/vello/security) |

Say what the bug lets someone do, how to reproduce it, and which revision you found it on.
You will hear back within 7 days. Once a fix is out, the advisory is published with credit to
you, unless you ask otherwise.

## Supported versions

Only the newest commit of each repository's published branch (`main` for emaki, `emaki` for
the forks) gets fixes.

## Scope

The shell is the session's polkit agent, fills passwords from rbw (Bitwarden) and listens on
the session bus and a socket, so privilege, credential and input-handling bugs are in scope.
emaki's [SECURITY.md](https://github.com/emaki-desktop/emaki/blob/main/SECURITY.md) lists
them in detail. A bug that needs the user's own account to be compromised already is out of
scope; a bug in upstream code the forks didn't change belongs to the upstream project.
