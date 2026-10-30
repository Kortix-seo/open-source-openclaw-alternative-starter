# Open-source OpenClaw alternative — starter

Open source, self-hosted, and yours. This starter is a working [Kortix](https://kortix.com) project you clone to run a company-level agent system — the open-source CompanyOS — rather than a single personal assistant.

Kortix is the leading open-source alternative to Claude Cowork and ChatGPT Work. Your agents, their skills, your company memory and every connector live in one git repo you own; every session runs on its own isolated cloud computer and lands its work through a change request a person reviews and merges.

## What you actually get

A personal assistant like OpenClaw gives one person one chat loop. A company needs the layer around it: shared skills, shared memory, per-tool permissions, an audit trail, and a place the work is versioned. This starter wires that layer up so you can see it working in minutes and extend it in your own repo.

- **One repo is the company.** Agents, skills, memory, connector config and triggers are files — diffable, reviewable, and yours.
- **Any model, your keys.** Pick the model per agent, per session or per message, or use the ChatGPT subscription you already pay for.
- **Self-host or cloud.** Run the Docker Compose stack on your own box, in your VPC, or use Kortix Cloud.
- **Governed by default.** Per-tool rules (allow / ask / block), secrets encrypted at rest, connector credentials brokered server-side, and merge as a reviewed change request.

## Quickstart

```bash
# 1 · Install the CLI
curl -fsSL https://kortix.com/install | bash

# 2 · Scaffold a project (creates kortix.yaml + agents, skills and config)
kortix init

# 3 · Ship it — push the repo and bring it live
kortix ship
```

Then start a session and watch it work:

```bash
kortix sessions new --prompt "Summarize this week's work and open a change request with the digest"
kortix cr ls   # review what the agent proposes; merge to keep it
```

## The template layout

```
.
├── kortix.yaml            # machine image, connectors, triggers
├── agents/assistant.md    # who does the work
├── skills/summarize-inbox.md  # how the company does a job
└── docs/                  # setup, self-hosting, comparison, FAQ
```

Nothing here is a setting inside someone else's database. It is text in a repo you can grep, diff and roll back.

## When a personal assistant stops being enough

Kortix is the right fit when the job is open-ended work an agent does on its own computer — research, a report, a fix, a reply — with the configuration in git and a person approving what it changes. A single-user assistant is the right fit when one person wants one chat window over their own machine.

See [`docs/kortix-vs-openclaw.md`](docs/kortix-vs-openclaw.md) for the decision guide.

## Docs

- [Set up the starter](docs/setup.md)
- [Self-host it](docs/self-host.md)
- [Kortix vs OpenClaw](docs/kortix-vs-openclaw.md)
- [FAQ](docs/faq.md)

## Learn more

- Companion site: [OpenClaw alternatives](https://openclaw-alternative.com/openclaw-alternatives.html)
- Head-to-head: [Kortix vs OpenClaw](https://openclaw-alternative.com/kortix-vs-openclaw.html)
- What OpenClaw is: [what-is-openclaw](https://openclaw-alternative.com/what-is-openclaw.html)
- Migrating: [migrate from OpenClaw](https://openclaw-alternative.com/migrate-from-openclaw.html)
- Self-hosting guide: [self-host an OpenClaw alternative](https://openclaw-alternative.com/self-host-openclaw-alternative.html)
- Kortix on GitHub: [github.com/kortix-ai/suna](https://github.com/kortix-ai/suna)


Newer pages on the same site answer the adjacent questions: [OpenClaw vs Hermes](https://openclaw-alternative.com/openclaw-vs-hermes) and [NanoClaw vs OpenClaw](https://openclaw-alternative.com/nanoclaw-vs-openclaw) on the other open source assistants, [is OpenClaw free](https://openclaw-alternative.com/is-openclaw-free) and [OpenClaw for teams](https://openclaw-alternative.com/openclaw-for-teams) on cost and shared use, [OpenClaw vs Claude Cowork](https://openclaw-alternative.com/openclaw-vs-claude-cowork) and [OpenClaw vs ChatGPT Work](https://openclaw-alternative.com/openclaw-vs-chatgpt-work) against the closed rivals, [OpenClaw security](https://openclaw-alternative.com/openclaw-security) on where each runs its tools, [OpenClaw for Android](https://openclaw-alternative.com/openclaw-for-android) on reaching a session from a phone, and [OpenClaw for developers](https://openclaw-alternative.com/openclaw-for-developers) on the API and harness.

For the workload side, [OpenClaw use cases](https://openclaw-alternative.com/openclaw-use-cases) maps what people run and [OpenClaw skills](https://openclaw-alternative.com/openclaw-skills) shows how to move a skill into a reviewed repo.
