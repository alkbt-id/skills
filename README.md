# alkbt-skills

A Claude Code plugin marketplace.

## Plugins

- [`adhd-mode`](plugins/adhd-mode/README.md) — an output style for readers who lose
  focus fast: result first, one idea per message, no preambles or recaps.

## Install

In a Claude Code session:

```
/plugin install <plugin> --marketplace alkbt-id/skills
```

Each plugin's README says what to do after installing.

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
