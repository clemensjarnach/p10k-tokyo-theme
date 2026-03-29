# p10k-tokyo — Powerlevel10k Tokyo Night Theme

A [Powerlevel10k](https://github.com/romkatv/powerlevel10k) prompt theme styled after the [Tokyo Night](https://github.com/folke/tokyonight.nvim) colour palette. Built on the rainbow prompt style with angled separators and Nerd Font icons.

![Preview of p10k-tokyo theme](https://github.com/clemensjarnach/p10k-tokyo-theme/blob/main/p10k-tokyo-screenshot.png?raw=true)

## Palette

| Role | Hex | 256-code |
|------|-----|----------|
| Purple — segment backgrounds | `#9274C9` | 98 |
| Muted lavender — subtle segments | `#A8B1D7` | 146 |
| White — active/bold text | `#ffffff` | 15 |
| Blue — error backgrounds | `#7094E1` | 105 |
| Orange — warnings, errors, slow commands | `#F29761` | 209 |
| Light green — success, clean git | `#73DACA` | 79 |

Terminal background: `#20212F` (256: 235).

## Segment colours

| Segment | Background | Foreground |
|---------|-----------|-----------|
| Directory | 98 purple | 15 cyan |
| Git clean | 79 green | *(default)* |
| Git untracked | 146 lavender | *(default)* |
| Status OK | 0 black | 79 green |
| Status error | 105 blue | 209 orange |
| Command execution time | 209 orange | 0 black |
| Time | 146 lavender | 235 dark navy |

## Installation

> **Prerequisites:** [Powerlevel10k](https://github.com/romkatv/powerlevel10k) must already be installed and active in your shell.

1. Copy `~/.p10k-tokyo.zsh` to your home directory.
2. Point your `.zshrc` at it:

```zsh
[[ -f ~/.p10k-tokyo.zsh ]] && source ~/.p10k-tokyo.zsh
```

3. Reload your shell or run `source ~/.zshrc`.

## Customisation

Every colour assignment is marked with `# customize color here`. To tweak a colour, open the file and search for that comment:

```zsh
grep -n "customize color here" ~/.p10k-tokyo.zsh
```

To preview all 256 terminal colours:

```zsh
for i in {0..255}; do print -Pn "%K{$i}  %k%F{$i}${(l:3::0:)i}%f " ${${(M)$((i%6)):#3}:+$'\n'}; done
```

## Requirements

- [Powerlevel10k](https://github.com/romkatv/powerlevel10k)
- A [Nerd Font v3](https://www.nerdfonts.com/) terminal font
- Zsh

## Credits

- **Powerlevel10k** by [Roman Perepelitsa (romkatv)](https://github.com/romkatv) — the prompt framework this theme is built on. Source: [github.com/romkatv/powerlevel10k](https://github.com/romkatv/powerlevel10k)
- **Tokyo Night** by [Folke Lemaitre (folke)](https://github.com/folke) — the colour palette that inspired this theme. Source: [github.com/folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim)

