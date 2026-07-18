# Contributing Guide

Thank you for improving this skill. Keep the purpose, trigger coverage, and output structure aligned across the English and Chinese versions.

## What to Contribute

- Fix triggers, review steps, or state-machine analysis logic
- Add anonymized UI/UX interaction examples
- Improve bilingual wording, examples, and terminology consistency
- Improve installation, usage, or maintenance documentation

## Submission Process

1. Create a branch focused on one concern.
2. Update both `SKILL.md` variants; do not change only one language.
3. Update the relevant README. User-facing changes also require a [changelog](CHANGELOG.md) entry.
4. Run these checks:

   ```bash
   git diff --check
   rg -n -P '[\p{Han}]' skills/en
   ```

5. Use a clear Conventional Commit, such as `docs: improve review output format`.
6. Use the pull request template to explain the change, validation, and scope.

## Skill Conventions

- English skill: `skills/en/ui-ux-interaction-review/SKILL.md`, with the name `ui-ux-interaction-review`.
- Chinese skill: `skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md`, with the name `ui-ux-interaction-review-cn`.
- Both files retain the `author` and `source` metadata.
- Keep `description` focused on activation conditions; put workflow details in the body.
- The English skill file contains no Chinese characters.

## Code of Conduct

Keep discussion respectful, specific, and actionable. Discuss proposals and evidence, never people.
