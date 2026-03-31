# AI Implementation Guide — Design System

This document explains how to use the Design System files to generate UI components without ambiguity.

You must strictly follow the structure and rules defined here.

---

# 📚 Source Files

You are provided with the following files:

* `tokens.json`
* `component-api.json`
* `component-behaviour.json`
* `component-examples.json`
* `component-mapping.json`
* `component-rules.json`


---

# 🧱 Architecture Overview

The Design System follows a strict layered architecture:

```
_root (Primitives)
   ↓
global (Semantic - non-color)
   ↓
theme (Semantic - color)
   ↓
components
   ↓
UI
```

---

## 1. `_root` (Primitives)

Raw, non-semantic values.

Examples:

* Colors (grayscale, brand, success, danger, etc.)
* Numbers (spacing, radius, sizes)

❗ Never used directly in components.

---

## 2. `global` (Semantic – Structure)

Non-color semantic tokens.

Includes:

* Typography (font, size, weight, line-height)
* Layout (spacing, padding, gap)
* Radius
* Elevation (shadow)
* Grid

Used to define structure and layout.

---

## 3. `theme` (Semantic – Color)

Color tokens used by components.

### Naming convention

```
theme.[category].[type].[variant].[state]
```

Examples:

* `theme.background.state.neutral.faint.default`
* `theme.text.state.brand.bolder.hovered`
* `theme.border.state.danger.moderate.default`

---

## 4. Components

Components are defined in `components.json`.

Each component includes:

* props (variants, states, booleans)
* composition (nested instances)
* structural rules

---

# 🧩 Component Model

## Component Types

### Base

Core interactive element
Example: `input-base`, `button`

### Field

Wrapper for label + hint + validation
Example: `input-field`, `select-field`

### Item

Reusable list element
Example: `dropdown-item`, `radio-item`

---

## Props Types

### Enum

```json
"size": ["sm", "md", "lg"]
```

### Boolean

```json
"isOpen": true | false
```

### State

```json
"default", "hovered", "pressed", "focused", "disabled"
```

---

## Global State Rules

* `disabled` overrides ALL states
* `focused` uses focus tokens (ring)
* `hovered` and `pressed` are pointer states
* `isOpen` is NOT a visual state, but a structural one

---

# 🎨 Styling System

## Golden Rule

👉 Components ONLY use `theme` tokens
❌ Never use `_root` directly

---

## Token Mapping

Defined in:

```
component-mapping.json
```

Each component maps:

* background
* text
* border
* icon
* elevation
* focus

Example:

```json
"button": {
  "primary": {
    "default": {
      "background": "theme.background.state.brand.medium.default",
      "text": "theme.text.state.brand.bolder.default"
    }
  }
}
```

---

# ⚙️ Component API

Defined in:

```
component-api.json
```

Includes:

* props
* slots
* constraints
* accessibility roles

---

# 🔁 Behavior & Interactions

Defined in:

```
component-behavior.json
```

Includes:

* state transitions
* keyboard interactions
* accessibility rules
* open/close logic

---

# 📏 Rules & Usage

Defined in:

```
component-rules.md
```

Includes:

* when to use
* when NOT to use
* best practices
* anti-patterns

---

# 🧪 Examples

Defined in:

```
component-examples.json
```

Includes:

* valid combinations
* edge cases
* invalid states
* real UI scenarios

---

# 🎯 Design Principles

## 1. Deterministic System

No ambiguity. Every state and behavior is defined.

## 2. Token-Driven

All UI is driven by semantic tokens.

## 3. Scalable

Works for large SaaS products.

## 4. AI-Compatible

Structured for automated UI generation.

---

# ♿ Accessibility

* All interactive components support keyboard navigation
* Focus is always visible (focus ring)
* ARIA roles defined in `component-api.json`
* Validation must not rely on color only

---

# 🔧 Implementation Guidelines

## For Developers

* Do not hardcode values
* Always use tokens
* Respect state priority
* Follow component API strictly

---

## For AI Systems

* Use `component-api.json` as source of truth
* Use `component-mapping.json` for styling
* Use `component-behavior.json` for logic
* Use `component-examples.json` for generation

---

## Example Workflow

Generate Button: 1. 

1. Read Button API
2. Identify variant + state
3. Apply mapping tokens
4. Apply behavior rules
5. Validate with examples
6. Generate component

---

## Error Handling

If something is missing:

DO NOT GUESS
ASK FOR CLARIFICATION

---

## Validation Rules

Before generating code, ensure:

* all props are valid
* no invalid combinations
* mapping exists for all states
* behavior is defined

---

# 🚀 Final Goal

This Design System guarantees:

* Visual consistency
* Behavioral consistency
* Predictable implementation
* Zero ambiguity for AI and developers

---

# 📌 Notes

* Figma is the visual source of truth
* This repository is the implementation source of truth
* Both must stay aligned

---

# 🧠 Summary

This is not just a UI kit.

This is a **complete implementation contract** between:

* Design
* Development
* AI systems
