# emaki

**A complete desktop for [niri](https://github.com/niri-wm/niri).**

emaki is a Wayland desktop shell built for the niri scrollable-tiling compositor. It covers everything a desktop needs beyond window management — bar, dock, launcher, notifications, settings — plus a set of first-party apps, all drawn with the same GPU-rendered design library. The shell is written in Rust on top of [amane](https://github.com/emaki-desktop/amane) and [vello](https://github.com/emaki-desktop/vello), and ships with a niri fork that adds the compositor features the shell relies on.

- **Shell:** a status bar on every monitor, a dock that rises with the overview, a launcher, notifications, Quick Settings, desktop widgets and an on-screen display
- **Apps:** Emaki Settings, Messages, Phone Screen, Shader Lab, Drop and an on-device assistant
- **emaki-kit:** the shell's look as a library, so any app can match it

## Repositories

| Repo | What it is | Branch |
|---|---|---|
| [emaki](https://github.com/emaki-desktop/emaki) | The shell, its apps and emaki-kit | `main` |
| [amane](https://github.com/emaki-desktop/amane) | Fork of [MystiaFin/amane](https://github.com/MystiaFin/amane), the Rust shell library emaki is built on | `emaki` |
| [niri](https://github.com/emaki-desktop/niri) | Fork of [niri-wm/niri](https://github.com/niri-wm/niri) adding materials, blur shapes, vibrancy, a desktop layer and gesture IPC | `emaki` |
| [vello](https://github.com/emaki-desktop/vello) | Fork of [linebender/vello](https://github.com/linebender/vello) with GPU memory budgets sized for a shell | `emaki` |

## Install

emaki and the niri fork are Nix flakes. Start with the [install guide](https://github.com/emaki-desktop/emaki/blob/main/docs/user/install.md). [STACK.md](https://github.com/emaki-desktop/emaki/blob/main/STACK.md) explains how the repos pin each other.

## Contributing

Open issues and pull requests where the change belongs:

- Shell behaviour, apps and the look → **emaki**
- Library work → **amane**
- Compositor work → **niri**

The forks are kept deliberately small so they rebase cleanly onto upstream. Their changes exist to serve emaki and aren't being proposed upstream, so please report problems with emaki here rather than to the upstream projects.

[Contributing guide](https://github.com/emaki-desktop/.github/blob/main/CONTRIBUTING.md) · [Code of conduct](https://github.com/emaki-desktop/.github/blob/main/CODE_OF_CONDUCT.md) · [Security policy](https://github.com/emaki-desktop/.github/blob/main/SECURITY.md)

## License

emaki and amane: MIT · niri: GPL-3.0 · vello: Apache-2.0 or MIT
