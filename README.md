# argvus-desktop

An Arch Linux metapackage for the ARGVUS desktop and everyday applications.
It installs no application payload or system configuration; pacman installs the
declared dependencies.

[![CI](https://github.com/argvus/argvus-desktop/actions/workflows/ci.yml/badge.svg)](https://github.com/argvus/argvus-desktop/actions/workflows/ci.yml)
[![Release](https://github.com/argvus/argvus-desktop/actions/workflows/release.yml/badge.svg)](https://github.com/argvus/argvus-desktop/actions/workflows/release.yml)
[![License](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](LICENSE)

## Dependencies

Required: `firefox`, `mpv`, `audacious`, `nautilus`, `xarchiver`, `inkscape`,
`gimp`, `mousepad`, `hyprland`, `hyprland-guiutils`, `hyprland-qt-support`,
`hyprpolkitagent`, `wayland`, `greetd`, `polkit`, `qt5-quickcontrols2`, `qt5ct`,
`qt6-tools`, `gtk4`, `gtk-layer-shell`, `gtk4-layer-shell`, `glib2`, `libdrm`,
`mesa`, `mesa-utils`, `hyprshot`, `grim`, `slurp`, `satty`, `cliphist`,
`wl-clipboard`, `wtype`, `swaybg`, `gsimplecal`, `udiskie`, `udisks2`,
`adwaita-icon-theme`, `noto-fonts`, `noto-fonts-emoji`,
`ttf-jetbrains-mono-nerd`, `ttf-nerd-fonts-symbols-mono`, `vivid`, `kitty`,
`xdg-utils`, `gst-plugins-base`, `gst-plugins-good`, `wireplumber`, and
`wireguard-tools`.

Optional: `okular`, `zathura`, `feh`, `imv`, `gpu-screen-recorder`,
`wf-recorder`, and `virtualbox-guest-utils`.

The infrastructure packages `systemd-libs`, `gcc-libs`, `pam`, `shadow`, and
`util-linux` are intentionally not direct dependencies.

## Build and validate

On Arch Linux or a compatible distribution with the skeleton's build tools:

```sh
make validate
make build
```

`make build` writes the local source archive and build artifacts under
`build/artifacts/`, and the package under `build/dist/`. The default build skips
dependency checks, so runtime dependencies do not need to be installed to create
the package; tools needed to build it must still be available. `make install`
uses pacman to install the package and resolve its required dependencies from
configured repositories, and therefore requires administrator privileges.

See [DEVELOPMENT.md](DEVELOPMENT.md) and
[packaging/archlinux/README.md](packaging/archlinux/README.md) for packaging
details.

## License

SPDX: `GPL-3.0-only`. See [LICENSE](LICENSE).
