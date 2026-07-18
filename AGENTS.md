# Repository Guidelines

## Project Structure

- `skills/en/ui-ux-interaction-review/SKILL.md`：英文技能。
- `skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md`：中文技能。
- `README.md` 与 `README.en.md`：面向用户的双语说明，中文为默认入口。
- `CHANGELOG.md` 与 `CHANGELOG.en.md`：双语发布记录。

## Contribution Rules

- 中英文技能必须成对更新，并保持功能与输出结构一致。
- 英文 `SKILL.md` 不得包含中文字符。
- 修改用户可见行为时，更新双语 README 和更新日志。
- 提交前执行 `git diff --check`，并检查所有 Markdown 相对链接。

## Commits

使用 Conventional Commits，提交范围保持单一、可审查。
