# ghostty

[Ghostty](https://ghostty.org) terminal config for macOS in the **archminimal** look: the same
palette as the Hyprland bar, launcher, login screen and nvim panels, one cyan accent
(`#00e5ff`), a translucent blurred background.

## Install

```sh
mkdir -p ~/.config/ghostty
cp config ~/.config/ghostty/config      # then reload: cmd+shift+,
```

A config in `~/Library/Application Support/com.mitchellh.ghostty/config` is loaded too and
can override this one; keep it empty or remove it.

## What's in it

- **Font**: JetBrains Mono 14 (Nerd Font symbols are built into Ghostty), ligatures off,
  slightly thicker strokes, 10% taller cells.
- **Colours**: background `#18191d` at 50% opacity with blur 30, foreground `#d0d2d0`,
  cyan cursor and selection, the archminimal 16-colour palette.
- **Window**: tabs in the title bar, balanced padding, state saved between launches, new
  tabs and splits open in the current folder.
- **Shell**: zsh integration with `ssh-env` / `ssh-terminfo` (remote hosts without
  `xterm-ghostty` work), block cursor, 100M lines of scrollback.
- **Input**: copy on select, left Option is Alt (for zsh, tmux and nvim Alt keys; the right
  Option still types symbols), a notification when a command over 10 s finishes in a
  background window.

## Keys

| Keys | Action |
|---|---|
| `ctrl+\`` (global) | drop-down quick terminal from anywhere |
| `cmd+t` / `cmd+d` / `cmd+shift+d` | new tab / split right / split down (built in) |
| `cmd+shift+enter` | zoom the split |
| `cmd+alt+h/j/k/l` | move between splits |
| `cmd+ctrl+h/j/k/l` | resize splits; `cmd+ctrl+=` equalize |
| `shift+enter` | sends `ESC CR` (newline in Claude Code and similar TUIs) |

Decisions: [docs/adr](docs/adr/README.md).
