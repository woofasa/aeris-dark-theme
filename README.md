# omarchy-aeris-theme

Aeris theme for [Omarchy](https://omarchy.org/): pink and cyan accents on a
near-black background.

![Aeris theme preview](preview.png)

## Installation

```sh
omarchy theme install https://github.com/woofasa/omarchy-aeris-theme.git
```

The theme is applied immediately. When installing from a git repository,
Omarchy skips every `*.lua` file, so two of them have to be installed by hand
(see below).

## Manual installation of Lua files

The files stay in the cloned theme directory, `~/.config/omarchy/themes/aeris/`.
Copy them into place:

```sh
T=~/.config/omarchy/themes/aeris

# Neovim (LazyVim): aeris-nvim plugin and colorscheme.
# For a repository install a plain copy is needed, not a symlink.
cp "$T/neovim.lua" ~/.config/nvim/lua/plugins/theme.lua

# Hyprland: gaps, rounding, blur and border colors (cyan).
# Overwrites an existing ~/.config/hypr/looknfeel.lua, so back it up first.
cp "$T/looknfeel.lua" ~/.config/hypr/looknfeel.lua
hyprctl reload
```

Requires LazyVim and network access to GitHub for the `woofasa/aeris-nvim`
plugin.

## Contents

- `colors.toml` - theme palette
- `shell.toml` - Omarchy bar and menu styling
- `icons.theme` - icon theme (`Yaru-sage`)
- `neovim.lua` - Neovim plugin spec (manual install, see above)
- `looknfeel.lua` - Hyprland look and feel (manual install, see above)
- `backgrounds/` - wallpapers, cycle with `omarchy theme bg next`
- `preview.png` - preview shown in the theme picker
