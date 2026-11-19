# ghostty

Ghostty terminal config for macOS, archminimal look. One file: `config`.

## Commands
- Install: `cp config ~/.config/ghostty/config` (a copy, not a link), reload with `cmd+shift+,`.
- Check: `ghostty +validate-config --config-file=config` (needs Ghostty installed).

## Layout
- `config`: the whole config, grouped by `# ----` headers (font, colors, window, shell,
  cursor & input, quick terminal, keys).
- `docs/adr/`: decision records (`.adr`), index in `docs/adr/README.md`.

## Conventions
- Read the ADR before changing a recorded decision; commit subjects carry its number.
- Colours must stay inline: a `#` in the middle of a value is part of the value, not a comment.
- The palette is shared with the archminimal desktop, tmux and nvim: change it everywhere or nowhere.
- `macos-option-as-alt = left` is what zsh, tmux and nvim Alt keys rely on; don't change it alone.
- Before adding a keybind, check it doesn't shadow tmux (`Alt-…`) or nvim keys.
