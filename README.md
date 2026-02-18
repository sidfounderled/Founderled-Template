# founderled-gtm

Agency knowledge base and Claude Code skill system for founderled.io client GTM work.

## Quick Start

1. Clone this repo
2. Open the folder in your terminal
3. Run `claude` to start Claude Code
4. Use slash commands to run skills

## Slash Commands

| Command | What It Does |
|---------|-------------|
| `/campaign-ideas` | Mine situations and generate testable campaign ideas from client data |
| `/campaign-brief` | Turn an approved campaign idea into a full execution brief |
| `/email-copy` | Generate cold email sequences from a campaign brief |
| `/list-strategy` | Translate a campaign brief into Clay build instructions |
| `/full-build` | Run the entire GTM build process for a new client |

## Adding a New Client

1. Copy `clients/_template/` to `clients/{client-name}/`
2. Fill in `master.md` with everything you know
3. Add call transcripts to `call-transcripts/`
4. Run `/campaign-ideas` to start generating campaigns

## Folder Structure

```
founderled-gtm/
├── .claude/
│   ├── commands/        ← Slash command skill files
│   └── profile.md       ← founderled.io context (read by all skills)
├── clients/
│   ├── _template/       ← Blank starter for new clients
│   └── {client-name}/   ← One folder per client
├── resources/
│   ├── copy-frameworks.md
│   ├── situation-patterns.md
│   └── objection-handling.md
└── README.md
```

## Updating Skills

Edit the files in `.claude/commands/` to refine how skills work. Changes take effect immediately on next use.

## Resources

The `resources/` folder contains shared knowledge used across all clients:
- **situation-patterns.md** — Library of common B2B buying situations with signals
- **copy-frameworks.md** — Cold email frameworks, subject line rules, CTA patterns
- **objection-handling.md** — Common objections and how to handle them
