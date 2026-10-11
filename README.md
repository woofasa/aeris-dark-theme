# omarchy-aeris-theme

Тема Aeris для [Omarchy](https://omarchy.org/): розовые и бирюзовые акценты на почти чёрном фоне.

## Установка

```sh
omarchy theme install https://github.com/woofasa/omarchy-aeris-theme.git
```

Тема применится сразу. Omarchy при установке из git-репозитория пропускает
все `*.lua` файлы, поэтому два из них нужно поставить вручную (ниже).

## Ручная установка Lua-файлов

Файлы остаются в склонированной папке `~/.config/omarchy/themes/aeris/`.
Скопируйте их на место:

```sh
T=~/.config/omarchy/themes/aeris

# Neovim (LazyVim): плагин aeris-nvim и colorscheme.
cp "$T/neovim.lua" ~/.config/nvim/lua/plugins/theme.lua

# Hyprland: отступы, скругления, blur и цвет рамок (cyan).
# Перезапишет существующий ~/.config/hypr/looknfeel.lua, сделайте резервную копию.
cp "$T/looknfeel.lua" ~/.config/hypr/looknfeel.lua
hyprctl reload
```

Требуется LazyVim и доступ к GitHub для плагина `woofasa/aeris-nvim`.

## Состав

- `colors.toml` - палитра темы
- `shell.toml` - оформление панели и меню Omarchy
- `icons.theme` - иконки (`Yaru-sage`)
- `neovim.lua` - плагин Neovim (ручная установка, см. выше)
- `looknfeel.lua` - оформление Hyprland (ручная установка, см. выше)
- `backgrounds/` - обои, переключение: `omarchy theme bg next`
- `preview.png` - превью в выборе тем
