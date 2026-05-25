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
