# Changelog

## v0.1.1 — 2026-05-13

- fix(commands): drop `mode: agent` frontmatter from `tac.{commit,gate,pr}.prompt.md`(Copilot-only 字段,Claude target compile 会丢字段并打 warning)

## v0.1.0 — 2026-05-13

- 首版骨架
- 9 skill: `tac-{spec,clarify,plan,tasks,implement,gate,commit,pr,metrics}-flow`
- 5 agent: `spec-writer / plan-author / tdd-implementer / gate-runner / commit-reviewer`
- 3 command: `commands/tac.{gate,commit,pr}.prompt.md`(APM `.prompt.md` 文件形)
