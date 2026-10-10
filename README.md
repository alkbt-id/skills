# alkbt-skills

A Claude Code plugin marketplace.

## Plugins

- [`adhd-mode`](plugins/adhd-mode/output-styles/adhd-mode.md) — an output style for
  readers who lose focus fast: result on the first line, one idea per message, context
  before any question and the question set apart, every message self-contained, no
  preambles or recaps.

`adhd-mode` is inspired by the [`i-have-adhd`](https://github.com/pydantic/pydantic-ai/blob/main/.agents/skills/i-have-adhd/SKILL.md) skill from pydantic-ai.

## Install

In Claude Code:

```
/plugin install adhd-mode --marketplace alkbt-id/skills
```

Then turn the style on: run `/output-style` and pick `adhd-mode:adhd-mode`, or set it
as your default in `~/.claude/settings.json`:

```json
{
  "outputStyle": "adhd-mode:adhd-mode"
}
```

Only one output style is active at a time, so this replaces any other style you use.

## Updates

Auto-update is off by default for this marketplace. Turn it on in `/plugin` →
Marketplaces → `alkbt-skills` → Enable auto-update, or in `~/.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "alkbt-skills": {
      "source": { "source": "github", "repo": "alkbt-id/skills" },
      "autoUpdate": true
    }
  }
}
```

Then new versions arrive when a session starts. Without auto-update, run
`/plugin marketplace update alkbt-skills` to get them.

## License

[MIT](LICENSE)
