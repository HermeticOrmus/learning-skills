# Using this repo with Cursor

This project includes a Cursor project rule so the five learning workflows are available when you work here.

## In this repository

1. Open the folder in Cursor.
2. The rule [`.cursor/rules/learning.mdc`](.cursor/rules/learning.mdc) is committed with `alwaysApply: false`, so it loads on demand rather than on every request. Reference it when you want a roadmap, explanation, practice set, cheatsheet, or comparison.
3. In Cursor, confirm under Settings, then Rules, where `learning` should appear.

## One combined rule for five workflows

Unlike a single-skill repo, this bundle packages five workflows. To keep Cursor's rule surface small, all five are summarized in one combined rule at [`.cursor/rules/learning.mdc`](.cursor/rules/learning.mdc) rather than five separate files. The full content of each workflow lives in its `SKILL.md` under [`skills/`](skills/).

## Use the same workflows in another project

**Cursor**: copy `.cursor/rules/learning.mdc` into that project's `.cursor/rules/` directory, creating the folder if needed. Merge with existing rules as you like.

**Other AI coding tools**: if a tool only supports a root instruction file, copy [`CLAUDE.md`](CLAUDE.md) into that project, or merge its contents into your existing instructions. Most modern AI coding tools read a root-level instruction file.

## Optional: personal skills

If you want each workflow as a reusable skill, copy the directories under [`skills/`](skills/) into your personal skills directory. See the README for the per-skill install commands.
