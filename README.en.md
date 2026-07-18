# UI/UX Interaction & State Chain Review Expert

[中文](README.md) | **English**

An AI-agent skill for reviewing UI/UX interactions. It treats interface behavior as state machines to identify ambiguous control ownership, state conflicts, missing feedback, and cognitive friction, then provides both best-experience and low-cost robust solutions.

## Capabilities

- Deconstruct the core task of a UI area and component control relationships
- Enumerate state combinations to identify information and operational gaps
- Review copy, visual metaphors, and interaction depth for cognitive friction
- Produce progressive-disclosure and low-cost implementation options in a fixed structure

## Use Cases

- Toggles that affect tabs or lists
- Auto/manual mode switching
- Radio, checkbox, and nested selections
- Conditional visibility, linked forms, and state-design reviews
- UI screenshots, wireframes, and interaction-flow critiques

## Files

- [`SKILL.md`](SKILL.md): Chinese skill definition and default entry point
- [`SKILL.en.md`](SKILL.en.md): English skill definition

## Usage

Place `SKILL.md` in the skills directory of Codex, Claude Code, or another compatible agent, then enable it for UI/UX interaction-review tasks.

## License

This project is licensed under the [MIT License](LICENSE).
