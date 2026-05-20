# .ai

AI assistant configs for the `bodnar-sh` workspace.

## Layout

| Subdir | Tool |
| --- | --- |
| `claude/` | Anthropic Claude Code config (`~/.claude/`-equivalent inside the workspace) |
| `opencode/` | OpenCode config |

The workspace's `setup.sh` symlinks these under the workspace-local XDG path:

- `dotfiles/../.config/claude` → `.ai/claude`
- `dotfiles/../.config/opencode` → `.ai/opencode`

Plus workspace-root convenience symlinks `.claude` and `.opencode`.

## Filling these in

Drop your Claude / OpenCode config files into the matching subdir. Both tools respect `XDG_CONFIG_HOME`, which the workspace's `mise.toml` pins to `/workspaces/code/github.com/bodnar-sh/.config`. Nothing leaks to the host user's home.
