# Awesome Claude Skills [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of Agent Skills, plugins, and skill-adjacent tooling for Claude Code and the open Agent Skills ecosystem.

Every entry here was fetched and verified alive before inclusion. Quality over volume: if it isn't documented, maintained, and genuinely useful, it doesn't go on the list.

## Contents

- [What are Agent Skills?](#what-are-agent-skills)
- [Official](#official)
- [Skill collections & marketplaces](#skill-collections--marketplaces)
- [Individual skills worth stealing](#individual-skills-worth-stealing)
  - [Shipping & review](#shipping--review)
  - [Research](#research)
  - [Workflow & ops](#workflow--ops)
  - [Other](#other)
- [Tooling](#tooling)
- [Patterns & guides](#patterns--guides)
- [Related lists](#related-lists)
- [Sibling ecosystems](#sibling-ecosystems)
- [Contributing](#contributing)

## What are Agent Skills?

A skill is a folder containing a `SKILL.md` file — instructions, plus optional scripts and reference material — that an agent discovers by its short description and loads only when a task actually calls for it. This makes skills radically token-efficient: dozens can be installed for a few hundred tokens of overhead, with the full body paid for only on use. Introduced with Claude Code and the Claude apps in October 2025 and released as an [open standard](https://agentskills.io) in December 2025, the format is now supported by many agents beyond Claude — see the [official docs](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for the complete picture.

## Official

- [Agent Skills overview](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) - Anthropic's canonical documentation: what skills are, how discovery and progressive disclosure work.
- [Agent Skills specification](https://agentskills.io) - The open standard for the skill format, with the spec itself at [/specification](https://agentskills.io/specification). Adopted well beyond Claude.
- [Claude Code: Skills](https://docs.claude.com/en/docs/claude-code/skills) - How skills work specifically inside Claude Code: personal, project, and plugin scopes.
- [Claude Code: Plugins](https://docs.claude.com/en/docs/claude-code/plugins) - The packaging layer — plugins bundle skills, subagents, hooks, and MCP servers for distribution via marketplaces.
- [anthropics/skills](https://github.com/anthropics/skills) - The official Agent Skills repository: Anthropic's production document skills (docx, pdf, pptx, xlsx), example skills, the spec, and a template to start from.
- [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official) - Anthropic's managed directory of high-quality Claude Code plugins.
- [anthropics/claude-code](https://github.com/anthropics/claude-code) - Claude Code itself; issues and release notes here are the closest thing to a changelog for skill behavior.

## Skill collections & marketplaces

- [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) - Production-grade engineering skills (code review, debugging, performance, testing) from the Chrome engineering leader.
- [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) - Large multi-domain pack — engineering, product, marketing, compliance — portable across Claude Code and other coding agents.
- [coleam00/second-brain-skills](https://github.com/coleam00/second-brain-skills) - Skills that turn Claude Code into a personal knowledge-management system.
- [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) - Marketing skills done seriously: CRO, copywriting, SEO, analytics, growth engineering.
- [davepoon/buildwithclaude](https://github.com/davepoon/buildwithclaude) - A hub for finding skills, agents, commands, hooks, plugins, and marketplace collections in one place.
- [dylanpulver/claude-skills](https://github.com/dylanpulver/claude-skills) - Twenty daily-driver skills in five installable plugins: session continuity, shipping, thinking tools, launch, and skills governance.
- [hashicorp/agent-skills](https://github.com/hashicorp/agent-skills) - Official skills for Terraform and other HashiCorp products — a good model of a vendor skill pack.
- [Jeffallan/claude-skills](https://github.com/Jeffallan/claude-skills) - 66 focused full-stack developer skills, one concern per skill.
- [jeremylongshore/claude-code-plugins-plus-skills](https://github.com/jeremylongshore/claude-code-plugins-plus-skills) - Open-source marketplace (tonsofskills.com) with hundreds of plugins and thousands of skills, plus the `ccpi` CLI.
- [jezweb/claude-skills](https://github.com/jezweb/claude-skills) - Practical web-stack skills: Cloudflare, React, Tailwind v4, AI integrations.
- [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) - Validated skills for science — biology, chemistry, medicine, drug discovery — plus access patterns for 100+ scientific databases.
- [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills) - Official Obsidian skills: teach your agent the Obsidian CLI and open formats like Markdown, Bases, and JSON Canvas.
- [obra/superpowers](https://github.com/obra/superpowers) - The best-known skills framework: a full software-development methodology (planning, TDD, debugging, code review) expressed as composable skills.
- [obra/superpowers-marketplace](https://github.com/obra/superpowers-marketplace) - The curated plugin marketplace companion to Superpowers.
- [simonw/claude-skills](https://github.com/simonw/claude-skills) - The contents of `/mnt/skills` from Claude's code-interpreter environment, extracted and tracked — see how Anthropic writes its own production skills.
- [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) - Vercel's official skills, including a react-best-practices skill distilled from their internal engineering guidance.

## Individual skills worth stealing

### Shipping & review

- [blader/humanizer](https://github.com/blader/humanizer) - Strips the tells of AI-generated writing from text; useful as a final pass on anything user-facing.
- [hamelsmu/claude-review-loop](https://github.com/hamelsmu/claude-review-loop) - An automated code-review loop that pits Claude Code against a second model until findings converge.
- [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) - Anti-slop aesthetic judgment for generated output — stops the generic-looking defaults.
- [Nutlope/hallmark](https://github.com/Nutlope/hallmark) - Anti-AI-slop design skill for frontend work; pairs well with any UI-building session.

### Research

- [aiwithremy/claude-skills-llm-council](https://github.com/aiwithremy/claude-skills-llm-council) - Runs a decision through five AI advisors with peer review before you commit.
- [dylanpulver/prior-art](https://github.com/dylanpulver/prior-art) - Scans the open-source and research landscape for projects doing what your repo does — novelty verdict, steal list, watch list.
- [Graphify-Labs/graphify](https://github.com/Graphify-Labs/graphify) - Turns a codebase — docs, SQL schemas, configs, PDFs — into a queryable knowledge graph via a `/graphify` skill, with deterministic AST parsing and no vector store.
- [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) - Researches any topic across Reddit, X, YouTube, HN, and the web, then synthesizes a grounded summary of the last 30 days.

### Workflow & ops

- [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) - Cuts a large share of output tokens by making the agent talk like a caveman. Silly premise, real savings.
- [OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files) - Persistent file-based planning: crash-proof markdown plans, recovery after `/clear` and compaction, a deterministic completion gate.

### Other

- [dgreenheck/webgpu-claude-skill](https://github.com/dgreenheck/webgpu-claude-skill) - Deep domain knowledge for building WebGPU applications with Three.js — a good template for any niche-API skill.
- [SawyerHood/dev-browser](https://github.com/SawyerHood/dev-browser) - Gives your agent a real web browser as a skill rather than an MCP server — a clean example of the scripts-in-skills pattern.

## Tooling

- [alirezarezvani/claude-code-skill-factory](https://github.com/alirezarezvani/claude-code-skill-factory) - Toolkit for generating structured skill templates, commands, and prompts at scale.
- [dylanpulver/judge-check](https://github.com/dylanpulver/judge-check) - Calibration kit for LLM-judge setups (common inside skill eval loops): decoy pass-rate, score separation, verdict-flip consistency.
- [dylanpulver/keypop](https://github.com/dylanpulver/keypop) - Native dialog for handing secrets to a skill or agent without the value ever entering model context. 60 lines of shell.
- [dylanpulver/session-deck](https://github.com/dylanpulver/session-deck) - Zero-dependency live dashboard for parallel Claude Code sessions.
- [jarrodwatts/claude-hud](https://github.com/jarrodwatts/claude-hud) - Plugin HUD showing context usage, active tools, running agents, and todo progress in real time.
- [sickn33/agentic-awesome-skills](https://github.com/sickn33/agentic-awesome-skills) - Local control plane for skill discovery, selection, and stack validation over a 2,000+ skill catalog, with CLI and MCP interfaces.
- [skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) - Anthropic's own meta-skill for authoring skills: interviews you, scaffolds the folder, and evaluates the result.
- [vercel-labs/skills](https://github.com/vercel-labs/skills) - `npx skills` — the open cross-agent installer: add, list, and update skills across Claude Code, Codex, Cursor, and dozens of other agents.

## Patterns & guides

- [Equipping agents for the real world with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) - Anthropic's engineering deep-dive: the design rationale, progressive disclosure, and how skills compare to fine-tuning and RAG.
- [Introducing Agent Skills](https://www.anthropic.com/news/skills) - The launch announcement — useful for the product framing across Claude apps, Claude Code, and the API.
- [Agent Skills best practices](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/best-practices) - Official authoring guidance: naming, description triggers, when to reach for scripts vs. prose.
- [Claude Skills are awesome, maybe a bigger deal than MCP](https://simonwillison.net/2025/Oct/16/claude-skills/) - Simon Willison's launch-week analysis; still the best short argument for why the pattern matters.
- [Agent Skills](https://simonwillison.net/2025/Dec/19/agent-skills/) - Willison again on the open standard: why a spec you can read in minutes is the point.
- [dylanpulver/agent-ops](https://github.com/dylanpulver/agent-ops) - Patterns for running Claude Code as a team of agents: session boards, handoffs, state ledgers, and an overnight queue.

## Related lists

- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) - Broad list of skills and resources across Claude workflows.
- [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - The big Claude Code list — skills are one section among agents, status lines, and tooling.
- [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) - Another well-maintained skills list with a Claude Code focus.
- [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) - Cross-agent skill list: official dev-team skills and community skills for Claude Code, Codex, Gemini CLI, Cursor, and more.

## Sibling ecosystems

Skill-like concepts exist beyond Claude; these are the closest cousins.

- [agents.md](https://agents.md) - The open `AGENTS.md` format: a single project-level instructions file supported by most coding agents.
- [github/awesome-copilot](https://github.com/github/awesome-copilot) - Community instructions, agents, and skills for GitHub Copilot — Copilot now also consumes Agent Skills.
- [google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) - Gemini's terminal agent; its extensions system plays the role plugins play in Claude Code.

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first: entries must exist (fetchable, not archived), be documented, and show signs of maintenance.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.

---

Built by [Dylan Pulver](https://dylanpulver.com), software engineer and entrepreneur in Toronto.
