<p align="center">
  <img src="https://ormus.solutions/mascot/pixellab_liquid_to_lotus.gif" alt="Learning Skills" width="128" style="image-rendering: pixelated;" />
</p>

<h1 align="center">Learning Skills</h1>

<p align="center">
  <em>A Claude Code skill bundle for learning any technology — roadmaps, explanations, practice drills, cheatsheets, and comparisons.</em>
</p>

<p align="center">
  <a href="https://github.com/HermeticOrmus/learning-skills/stargazers"><img src="https://img.shields.io/github/stars/HermeticOrmus/learning-skills?style=flat-square&color=aa8142" alt="Stars" /></a>
  <a href="https://github.com/HermeticOrmus/learning-skills/blob/main/LICENSE"><img src="https://img.shields.io/github/license/HermeticOrmus/learning-skills?style=flat-square&color=aa8142" alt="License" /></a>
  <a href="https://github.com/HermeticOrmus/learning-skills/commits"><img src="https://img.shields.io/github/last-commit/HermeticOrmus/learning-skills?style=flat-square&color=aa8142" alt="Last Commit" /></a>
  <img src="https://img.shields.io/badge/Claude_Code-aa8142?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code" />
</p>

---

## The problem

Learning a new technology on your own is unstructured and slow. You do not know what to learn first, in what order, or when you have learned enough. You re-explain the same concept to yourself three times, drill the wrong things, lose what you learned because you never wrote it down, and stall on tool choices you have no basis to make.

This bundle packages five learning workflows that each fix one of those failure modes. Together they cover the arc from planning a path to retaining what you learned.

## The five skills

| Skill | What it does |
|---|---|
| `learning-roadmap` | Builds a phased learning path with prerequisites, topics, practice, milestones, and pitfalls |
| `learning-explain` | Explains one concept from first principles with examples, analogies, and gotchas |
| `learning-practice` | Generates progressive exercises from warm-up to real-world, with worked solutions |
| `learning-cheatsheet` | Produces a concise, scannable reference of common operations, syntax, and patterns |
| `learning-compare` | Compares tools or approaches across consistent dimensions with a context-aware recommendation |

Umbrella overview: [`CLAUDE.md`](CLAUDE.md). Worked examples: [`EXAMPLES.md`](EXAMPLES.md).

## Install

### The whole bundle

Copy every skill into your personal skills directory so Claude Code loads all five:

```bash
cp -r skills/* ~/.claude/skills/
```

### Individual skills

Copy only the ones you want:

```bash
cp -r skills/learning-roadmap ~/.claude/skills/
cp -r skills/learning-explain ~/.claude/skills/
cp -r skills/learning-practice ~/.claude/skills/
cp -r skills/learning-cheatsheet ~/.claude/skills/
cp -r skills/learning-compare ~/.claude/skills/
```

### As slash commands

The same five workflows also work as `/learning:*` slash commands. Copy the skill bodies into your commands directory:

```bash
mkdir -p ~/.claude/commands/learning
cp skills/learning-roadmap/SKILL.md   ~/.claude/commands/learning/roadmap.md
cp skills/learning-explain/SKILL.md    ~/.claude/commands/learning/explain.md
cp skills/learning-practice/SKILL.md   ~/.claude/commands/learning/practice.md
cp skills/learning-cheatsheet/SKILL.md ~/.claude/commands/learning/cheatsheet.md
cp skills/learning-compare/SKILL.md    ~/.claude/commands/learning/compare.md
```

Then invoke `/learning:roadmap`, `/learning:explain`, `/learning:practice`, `/learning:cheatsheet`, or `/learning:compare`.

### In Cursor

See [`CURSOR.md`](CURSOR.md) for the Cursor-rule equivalent. The five workflows are summarized in one combined rule at [`.cursor/rules/learning.mdc`](.cursor/rules/learning.mdc).

## See also

- [`vibe-engineer-skills`](https://github.com/HermeticOrmus/vibe-engineer-skills): guidelines for directing AI codegen well, the companion discipline to learning
- [`andrej-karpathy-skills`](https://github.com/HermeticOrmus/andrej-karpathy-skills): how Claude should behave when writing code

## Contributing

PRs welcome, especially for additional worked examples in [`EXAMPLES.md`](EXAMPLES.md) and adaptations of [`CURSOR.md`](CURSOR.md) for other AI coding tools.

## License

MIT. Use it, fork it, merge it into your own setup.

---

## Part of the Libre Open-Source Stack for Claude Code

This repository is part of a growing family of open-source toolkits for Claude Code.

### Libre suite — comprehensive plugin bundles

- [LibreUIUX-Claude-Code](https://github.com/HermeticOrmus/LibreUIUX-Claude-Code) — UI/UX development (152 agents, 70 plugins, 76 commands, 74 skills)
- [LibreArch-Claude-Code](https://github.com/HermeticOrmus/LibreArch-Claude-Code) — Software architecture and system design
- [LibreCopy-Claude-Code](https://github.com/HermeticOrmus/LibreCopy-Claude-Code) — Technical writing and documentation engineering
- [LibreDevOps-Claude-Code](https://github.com/HermeticOrmus/LibreDevOps-Claude-Code) — DevOps engineering and infrastructure automation
- [LibreEmbed-Claude-Code](https://github.com/HermeticOrmus/LibreEmbed-Claude-Code) — Embedded systems, firmware, and IoT development
- [LibreFinTech-Claude-Code](https://github.com/HermeticOrmus/LibreFinTech-Claude-Code) — Financial technology development
- [LibreGEO-Claude-Code](https://github.com/HermeticOrmus/LibreGEO-Claude-Code) — AI-search optimization (ChatGPT, Perplexity, Gemini, Google AI Overviews)
- [LibreGameDev-Claude-Code](https://github.com/HermeticOrmus/LibreGameDev-Claude-Code) — Game development across Godot, Unity, Unreal
- [LibreMLOps-Claude-Code](https://github.com/HermeticOrmus/LibreMLOps-Claude-Code) — ML engineering and AI operations
- [LibreMobileDev-Claude-Code](https://github.com/HermeticOrmus/LibreMobileDev-Claude-Code) — Mobile app development (Flutter, React Native, native iOS, native Android)
- [LibreSecOps-Claude-Code](https://github.com/HermeticOrmus/LibreSecOps-Claude-Code) — Security operations
- [LibreSessionFlow-Claude-Code](https://github.com/HermeticOrmus/LibreSessionFlow-Claude-Code) — Session lifecycle: handoff, pickup, absorb, explore, close

### Skills mini-repos — single CLAUDE.md drop-ins

- [vibe-engineer-skills](https://github.com/HermeticOrmus/vibe-engineer-skills) — Direct AI codegen well: hypothesis before help, scoped prompts, validate before accepting
- [markdown-discipline-skills](https://github.com/HermeticOrmus/markdown-discipline-skills) — Strip AI-slop from markdown (no em dashes, no marketing fluff)
- [shell-safety-skills](https://github.com/HermeticOrmus/shell-safety-skills) — `set -euo pipefail` discipline plus 15 failure-mode examples
- [commit-standard-skills](https://github.com/HermeticOrmus/commit-standard-skills) — Ormus Commit Standard v1.0 plus commit-msg hook and commitlint
- [unwoke-skills](https://github.com/HermeticOrmus/unwoke-skills) — Strip AI theater (ten sins to eliminate, symmetric engagement)
- [python-conventions-skills](https://github.com/HermeticOrmus/python-conventions-skills) — Modern Python 3.11+ (types, pathlib, async, ruff, mypy, uv)
- [typescript-conventions-skills](https://github.com/HermeticOrmus/typescript-conventions-skills) — TypeScript strict mode, discriminated unions, Result types
- [hermetic-laws-skills](https://github.com/HermeticOrmus/hermetic-laws-skills) — Seven Hermetic Principles applied to engineering
- [riper-workflow-skills](https://github.com/HermeticOrmus/riper-workflow-skills) — Research / Innovate / Plan / Execute / Review systematic dev
- [six-day-cycle-skills](https://github.com/HermeticOrmus/six-day-cycle-skills) — Sustainable shipping cadence with mandatory rest
- [token-optimization-skills](https://github.com/HermeticOrmus/token-optimization-skills) — Claude Code token and context optimization
- [osint-skills](https://github.com/HermeticOrmus/osint-skills) — OSINT research methodology (multi-wave investigative spiral)
- [calcinate-skills](https://github.com/HermeticOrmus/calcinate-skills) — Stage 1 of the Magnum Opus (burn project bloat)
- [claude-md-overhaul-skills](https://github.com/HermeticOrmus/claude-md-overhaul-skills) — Audit CLAUDE.md and MEMORY.md against caps
- [session-handoff-skills](https://github.com/HermeticOrmus/session-handoff-skills) — Session handoff and pickup discipline
- [naming-skills](https://github.com/HermeticOrmus/naming-skills) — Product naming methodology (mine the brand's vocabulary)
- [magnum-opus-skills](https://github.com/HermeticOrmus/magnum-opus-skills) — Seven-stage alchemy applied to project transformation
- [mem-search-skills](https://github.com/HermeticOrmus/mem-search-skills) — Search claude-mem cross-session memory: search, filter, fetch
- [hypothesis-debugging-skills](https://github.com/HermeticOrmus/hypothesis-debugging-skills) — Hypothesis-driven debugging: reproduce, isolate, test, fix
- [vibe-proof-skills](https://github.com/HermeticOrmus/vibe-proof-skills) — Security hardening for vibe-coded full-stack apps
- [tdd-skills](https://github.com/HermeticOrmus/tdd-skills) — Test-driven development (Red-Green-Refactor) for JS/TS and Python
- [mars-skills](https://github.com/HermeticOrmus/mars-skills) — Production-readiness audit: the five mortal sins of vibe-coded MVPs
- [git-workflow-skills](https://github.com/HermeticOrmus/git-workflow-skills) — Clean git workflow: branch, atomic commits, reviewable PRs
- [code-review-skills](https://github.com/HermeticOrmus/code-review-skills) — Domain-aware code review: classify the code, then focus
- [code-comprehension-skills](https://github.com/HermeticOrmus/code-comprehension-skills) — Understand an unfamiliar codebase fast
- [dx-audit-skills](https://github.com/HermeticOrmus/dx-audit-skills) — Audit developer experience: docs, onboarding, tooling friction
- [setup-env-skills](https://github.com/HermeticOrmus/setup-env-skills) — Set up a project's development environment
- [automate-skills](https://github.com/HermeticOrmus/automate-skills) — Turn repetitive tasks into reliable automation scripts
- [quick-fix-skills](https://github.com/HermeticOrmus/quick-fix-skills) — Fast troubleshooting for common issues
- [prime-context-skills](https://github.com/HermeticOrmus/prime-context-skills) — Prime project context at the start of a session
- [auto-docs-skills](https://github.com/HermeticOrmus/auto-docs-skills) — Generate and maintain project documentation
- [linux-sysadmin-skills](https://github.com/HermeticOrmus/linux-sysadmin-skills) — Linux system administration: security, performance, diagnostics, monitoring, maintenance

### Template source

- [andrej-karpathy-skills](https://github.com/HermeticOrmus/andrej-karpathy-skills) — the canonical single-file CLAUDE.md pattern (fork of jiayuan_jy's original)

Star the family, not just one — that's how the suite stays coherent.
