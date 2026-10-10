# ADHD mode

An output style for Claude Code. The agent writes every chat message so that a reader
who loses focus fast gets it at a glance.

## Install

In a Claude Code session:

```
/plugin install adhd-mode --marketplace alkbt-id/skills
```

## Turn it on

After installing, pick the style:

```
/output-style
```

and choose `adhd-mode:adhd-mode`. Or make it your default in `~/.claude/settings.json`:

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

## What changes

- The first line is the result or the decision needed from you.
- One idea per message; the next one comes when you're ready.
- Context comes before any question, and the question stands alone at the end.
- Every message makes sense on its own — no "as we discussed".
- No preambles, recaps, or "let me know if anything comes up".

Full rules: [output-styles/adhd-mode.md](output-styles/adhd-mode.md).
