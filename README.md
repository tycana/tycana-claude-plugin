<p align="center">
  <img src="tycana-logo.svg" alt="Tycana" width="300">
</p>

<p align="center">
  <strong>AI productivity partner — capture, plan, review, and think through your work with Claude.</strong>
</p>

<p align="center">
  <a href="https://www.tycana.com/getting-started/">Get Started</a> &middot;
  <a href="https://www.tycana.com">Website</a> &middot;
  <a href="https://www.tycana.com/mcp/">MCP Docs</a>
</p>

---

Tycana turns Claude into your productivity partner. Capture tasks with full context, plan energy-aware days, get honest progress reviews, and brain-dump everything on your mind — all through conversation.

Unlike a task list Claude reads back to you, Tycana is a productivity backend Claude *thinks through*. It remembers your work across conversations, tracks patterns over time, and gives increasingly personalized recommendations the more you use it.

## What You Get

**Smart capture** — mention a task in conversation and Tycana captures it with inferred effort, energy level, project, and context. No forms, no fields to fill.

**`/tycana:morning`** — personalized daily briefing with your real priorities, carryovers, and a sequenced plan.

**`/tycana:dump`** — empty your head in 30 seconds. Tycana parses your stream of consciousness into organized, enriched items.

**`/tycana:review`** — honest weekly assessment with real velocity trends, slip patterns, and forward-looking observations.

**`/tycana:next`** — energy-aware recommendation for what to work on right now, with reasoning.

**`/tycana:upgrade`** — check for plugin updates and install them.

**Persistent memory** — Tycana remembers your tasks, preferences, and work patterns across every conversation.

## Install

In Claude Code:

```
/plugin marketplace add tycana/tycana-claude-plugin
/plugin install tycana@tycana
```

## Pricing

This plugin requires a Tycana subscription. One plan, everything included.

- **$15/month** or **$150/year** (2 months free)
- 14-day free trial, no credit card required
- No feature tiers, no per-seat pricing, no upsells

[Start your free trial](https://www.tycana.com/getting-started/)

## Connection

- **Claude.ai** — connects automatically via OAuth on first use
- **Claude Code** — this plugin configures the MCP connection for you
- **Manual setup** — see [tycana.com/getting-started](https://www.tycana.com/getting-started) for bearer token and direct MCP configuration

## How It Works

Tycana is an [MCP server](https://modelcontextprotocol.io) — a productivity backend designed for AI consumption. This plugin teaches Claude how to use Tycana idiomatically:

- **Background intelligence** — Claude automatically captures tasks from conversation with rich metadata, tracks relationships between items, and presents Tycana's intelligence signals as natural conversation instead of raw data.
- **Daily workflows** — slash commands chain Tycana's 14 tools into high-value rituals (morning briefing, brain dump, weekly review).

The plugin is markdown instructions. All data lives in your Tycana account, accessible from any MCP-compatible client.

## Plugin Contents

```
skills/
  tycana-productivity/    Background skill — capture, context, relationships, completion
  getting-started/        Onboarding for new users
commands/
  morning.md              /tycana:morning — daily briefing
  dump.md                 /tycana:dump — brain dump
  review.md               /tycana:review — progress review
  next.md                 /tycana:next — what to do next
  upgrade.md              /tycana:upgrade — plugin updates
```

## Learn More

- [Tycana website](https://www.tycana.com)
- [Getting started guide](https://www.tycana.com/getting-started)
- [MCP documentation](https://www.tycana.com/mcp/)
- [Privacy Policy](https://app.tycana.com/privacy)
- [Terms of Service](https://app.tycana.com/terms)

## License

MIT
