# Repository Guidelines

## Project Structure

- `skills/en/ui-ux-interaction-review/SKILL.md`: English skill definition.
- `skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md`: Chinese skill definition.
- `README.md` and `README.zh-CN.md`: Bilingual user documentation, with English as the default.
- `CONTRIBUTING.md` and `CHANGELOG.md`: English contribution and release documentation.

## Contribution Rules

- Update the English and Chinese skills together, keeping their behavior and output structure aligned.
- Do not include Chinese characters in the English `SKILL.md`.
- Update both README files and the changelog for user-visible changes.
- Run `git diff --check` and verify all relative Markdown links before committing.

## Commits

Use Conventional Commits. Keep each commit focused and reviewable.
