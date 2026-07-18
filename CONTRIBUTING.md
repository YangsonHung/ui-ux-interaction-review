# 贡献指南

感谢你帮助改进这个技能。所有贡献都应保持中英文版本的目标、触发范围和输出结构一致。

## 可以贡献的内容

- 修正触发条件、审查流程或状态机分析逻辑
- 补充匿名化的 UI/UX 交互案例
- 改进中英文文案、示例和术语一致性
- 完善安装、使用和维护文档

## 提交流程

1. 创建聚焦单一问题的分支。
2. 同步修改英文和中文 `SKILL.md`，不要只更新其中一种语言。
3. 更新相关 README；面向用户的改动同时更新 [更新日志](CHANGELOG.md)。
4. 运行以下检查：

   ```bash
   git diff --check
   rg -n -P '[\p{Han}]' skills/en
   ```

5. 使用清晰的 Conventional Commit，例如 `docs: improve review output format`。
6. 按 PR 模板说明改动、验证结果和影响范围。

## 技能规范

- 英文技能：`skills/en/ui-ux-interaction-review/SKILL.md`，`name` 为 `ui-ux-interaction-review`。
- 中文技能：`skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md`，`name` 为 `ui-ux-interaction-review-cn`。
- 两个文件都保留 `author` 与 `source` 元数据。
- `description` 聚焦触发场景；具体流程写在正文中。
- 英文技能文件不包含中文字符。

## 行为准则

请保持讨论尊重、具体且可执行。针对方案和事实提出意见，不针对个人。
