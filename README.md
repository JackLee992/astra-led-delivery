# Astra 主导交付

`astra-led-delivery` 是通用任务协作技能，适用于调研、分析、写作、策划、资料整理、运营协作和工程等工作。

- Astra 负责核心思路、关键调研、方案或架构设计和难题。
- 执行模型完成具体工作、结果核验与交付，可按任务指定模型和思考深度。
- 复用有效方案，精简交接和后续上下文，减少重复调研与无实际问题的复审。

完整规则见 [SKILL.md](SKILL.md)。

## 使用

```text
使用 $astra-led-delivery，执行模型 5.5，思考深度 extra high，整理一份竞品分析报告。
```

| 执行模型别名 | 模型 ID |
| --- | --- |
| 6.1 sol | `gpt-6.1-sol` |
| 5.6 sol | `gpt-5.6-sol` |
| 5.5 | `gpt-5.5` |

`extra high` / `extra-high` 映射为 `xhigh`，`max` 保持为 `max`。也支持工具提供的其他模型与深度；具体组合以实际工具能力为准。

沿用用户当前任务的配置；未指定执行模型时默认 `gpt-6.1-sol`，未指定深度时沿用当前任务设置或工具默认值。支持用户选择低额度执行模型，实际消耗以可靠额度信息为准。

## 安装

首次安装时，将仓库克隆到技能目录下；目标目录应尚不存在：

```bash
git clone https://github.com/JackLee992/astra-led-delivery.git "${CODEX_HOME:-$HOME/.codex}/skills/astra-led-delivery"
```

需要对应 GitHub 仓库的访问权限，以及支持真实模型路由的协作工具。本技能安排任务分工，模型切换由工具实际执行。
