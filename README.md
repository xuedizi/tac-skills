# tac-skills

TAC 流程相关 skill / agent / command 的 monorepo。**整个 repo 共享一个版本号**,
每次 release 用同一个 tag 同时发布所有原语。

## 引用方式

```yaml
# apm.yml
dependencies:
  apm:
    - xuedizi/tac-skills/skills/tac-spec-flow#v0.1.0
    - xuedizi/tac-skills/agents/spec-writer.agent.md#v0.1.0
    - xuedizi/tac-skills/commands/tac.gate#v0.1.0
```

## 目录结构

| 路径 | 原语类型 | APM 寻址 |
|---|---|---|
| `skills/<name>/SKILL.md` | skill | `xuedizi/tac-skills/skills/<name>#vX.Y.Z` |
| `agents/<name>.agent.md` | agent | `xuedizi/tac-skills/agents/<name>.agent.md#vX.Y.Z` |
| `commands/<name>/COMMAND.md` | command | `xuedizi/tac-skills/commands/<name>#vX.Y.Z` |

## 版本节奏

| 变更 | bump |
|---|---|
| typo / 措辞 | patch |
| 新增原语 / 兼容增强 | minor |
| 删除/重命名/不兼容 frontmatter | major |

所有 SKILL.md / .agent.md / COMMAND.md 的 frontmatter `version:` 必须等于
仓库 `VERSION`(CI 校验);release 时 git tag 必须等于 `VERSION`。

## 与其他 repo 的关系

| repo | 关系 |
|---|---|
| `xuedizi/apm-policy` | 子项目的 `apm-policy.yml extends:` 必须放行 `skill/agent/command` 三类原语 |
| `xuedizi/starter-android-kotlin` | starter 的 `recommended_apm` 字段会 pin 本 repo 的某个版本 |
