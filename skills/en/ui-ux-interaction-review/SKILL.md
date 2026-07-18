---
name: ui-ux-interaction-review
author: YangsonHung
source: https://github.com/YangsonHung/ui-ux-interaction-review
description: Use when reviewing or restructuring UI/UX interaction components and state logic, especially for screenshots, wireframes, toggles, linked controls, conditional UI, or UX design reviews.
---

# 🎛️ UI/UX Interaction & State Chain Review Expert

## Overview

This skill diagnoses and restructures complex UI component interaction logic. Core approach: don't judge the interface by aesthetics — treat every interactive component as a **state machine**, exhaustively review it, surface issues like ambiguous control ownership, missing state feedback, and ambiguous copy, then provide both a "best experience" and a "lowest cost" solution.

Applies to: toggles that gate tabs, nested radio/checkbox selections, auto/manual mode switches, lists that show/hide based on conditions, linked form validation — any interface where "changing one variable affects the visibility or availability of other components."

## When to use

- User uploads a UI screenshot or wireframe and asks for evaluation, optimization, or issue-finding
- User describes an interaction flow (e.g., "should this list change when the toggle switches?")
- User mentions state design, interaction review, UX optimization, or design critique
- User asks for "a few options" to improve a component's interaction

## Core Review Process (4 Steps)

Execute in order — do not skip steps:

### Step 1: Core Intent Deconstruction

Strip away the visual surface and answer two questions:
- What is the fundamental purpose of this UI area? What's the core user task?
- What is the relationship between components? Is there a "controlling vs. controlled" hierarchy hiding behind what looks like a parallel/independent relationship?

Common misjudgment: mistaking a "control relationship" for a "parallel relationship." For example, an "Auto/Manual toggle" and a "model list" look like two independent controls, but the toggle actually determines whether the list is operable — they are hierarchical, not parallel.

### Step 2: Full State Machine Enumeration

Compute the Cartesian product of all control variables to map every possible interface state, then check each state for two kinds of gaps:

- **Information Gap (unknown state)**: In a given state, is the system's outcome clearly fed back to the user? (e.g., in Auto mode, which option got selected — is that visible at all?)
- **Operational Gap (unauthorized control)**: In a given state, does something that looks clickable actually do nothing, or is something active that shouldn't be? (e.g., in Auto mode, list items still appear clickable)

### Step 3: Cognitive Friction Review

- **Copy ambiguity**: Does toggle/button text create confusion between "current state" and "destination state" when it changes? (Recommendation: fix the label text and let the toggle's On/Off position express the state, rather than changing the label itself.)
- **Visual metaphor**: Does grayed-out reliably mean disabled? Does highlighted reliably mean active? Does it match physical intuition?
- **Interaction depth**: Can a "two-layer radio selection" be flattened into "one layer" to reduce the click chain?

### Step 4: Multi-Tier Solution Output

Always provide at least two solutions — never just one:

- **Solution A (best experience)**: Follow Progressive Disclosure — restructure the information hierarchy, hide irrelevant content, and show controls only when needed.
- **Solution B (lowest cost)**: Keep the existing layout/framework unchanged; patch the logic with disabled overlays, state locks, tooltips, or highlight badges to keep page height/structure stable (no layout jump).

Weigh solutions against three dimensions: development cost, transition/motion stability, and visual cleanliness.

## Output Format

Structure the output exactly as follows:

```markdown
### 🔍 Current Diagnosis & Core Conflicts
- **Component Hierarchy Conflict**: [who controls what, where the cross-wiring is]
- **State Machine Logic Gap**: [missing feedback or ambiguous control in a specific state]
- **Cognitive Friction Point**: [ambiguity in copy or visual metaphor]

### 💡 Solution A: [Name] (Best Experience)
- **Core Approach**: [one sentence]
- **Interaction Behavior**:
  - State 1: [progressive disclosure details]
  - State 2: [corresponding change]
- **Advantages**: [...]

### 💡 Solution B: [Name] (Low Cost & Robust)
- **Core Approach**: [one sentence]
- **Interaction Behavior**:
  - State 1: [gray-out/overlay/lock rules]
  - State 2: [logic for restoring active state]
- **Advantages**: [...]

### 📐 Advanced Micro-Optimization Suggestions (Optional)
- **Copy Standards**: [how to unify and lock text]
- **Micro-animations / Feedback**: [tooltips, breathing highlights, etc.]
```

## Underlying Methodology (for reference — no need to expand in output)

- **First Principles**: Ask the underlying purpose before judging the surface.
- **State Machine Logic**: Enumerate all state combinations and check for gaps, rather than only reviewing the "happy path."
- **Cognitive Friction Minimization**: Fix copy, keep visuals intuitive, flatten hierarchy.
- **Progressive Disclosure**: Hide what shouldn't be shown to keep the interface clean; pair with a low-cost fallback for cases constrained by dev timeline or layout stability.
