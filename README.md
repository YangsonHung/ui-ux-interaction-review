# UI/UX Interaction & State Chain Review Expert

**English** | [中文](README.zh-CN.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Skill](https://img.shields.io/badge/Agent%20Skill-UI%2FUX%20Review-1f6feb)](skills/en/ui-ux-interaction-review/SKILL.md)

An AI-agent skill for reviewing UI/UX interactions. It treats interface behavior as state machines to identify ambiguous control ownership, state conflicts, missing feedback, and cognitive friction, then provides both best-experience and low-cost robust solutions.

## ✨ Capabilities

- Deconstruct the core task of a UI area and component control relationships
- Enumerate state combinations to identify information and operational gaps
- Review copy, visual metaphors, and interaction depth for cognitive friction
- Produce progressive-disclosure and low-cost implementation options in a fixed structure

## 🎯 Use Cases

- Toggles that affect tabs or lists
- Auto/manual mode switching
- Radio, checkbox, and nested selections
- Conditional visibility, linked forms, and state-design reviews
- UI screenshots, wireframes, and interaction-flow critiques

## 🚀 Quick Start

After installing the English skill, give a compatible agent a UI screenshot, wireframe, or interaction description. You can also invoke it explicitly:

```text
$ui-ux-interaction-review Review the linked behavior between an auto/manual mode and a model list.
```

Every review includes a current diagnosis, a best-experience solution, a low-cost robust solution, and optional micro-interaction suggestions.

## 🗂️ Project Structure

```
skills/
├── en/
│   └── ui-ux-interaction-review/
│       └── SKILL.md
└── zh-cn/
    └── ui-ux-interaction-review-cn/
        └── SKILL.md
```

- [`skills/en/ui-ux-interaction-review/SKILL.md`](skills/en/ui-ux-interaction-review/SKILL.md): English skill definition
- [`skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md`](skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md): Chinese skill definition

## 📦 Installation

Install the English skill:

```bash
npx skills add YangsonHung/ui-ux-interaction-review --skill ui-ux-interaction-review
```

Install the Chinese skill:

```bash
npx skills add YangsonHung/ui-ux-interaction-review --skill ui-ux-interaction-review-cn
```

When using pnpm, replace `npx` with `pnpm dlx`.

## 🧭 Scope

- This skill focuses on interaction logic, state feedback, and cognitive friction; it does not replace visual brand design or usability testing.
- Both the best-experience and low-cost solutions must explain state changes, control ownership, and feedback.
- Base conclusions on the supplied UI, wireframe, or business rules. List open questions first when key information is absent.

## 🤝 Contributing

Contributions that improve triggers, interaction examples, bilingual wording, or the output structure are welcome. Read these documents before submitting a change:

- [Contribution Guide](CONTRIBUTING.md)
- [Changelog](CHANGELOG.md)
- [Security Policy](SECURITY.md)
- [Maintainer Guide](AGENTS.md)

Use the GitHub [issue templates](.github/ISSUE_TEMPLATE) to report defects or propose enhancements. Use the [pull request template](.github/PULL_REQUEST_TEMPLATE.md) when submitting code or documentation.

## 🛣️ Roadmap

- [ ] Add state-machine examples for common UI patterns
- [ ] Add a reusable review checklist
- [ ] Build a real-world interface case library

## 📄 License

This project is licensed under the [MIT License](LICENSE).
