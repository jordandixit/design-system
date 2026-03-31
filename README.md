# AI-Ready Design System Documentation

## 1. Overview

This design system is built for **scalable product development and AI-driven implementation**.

It enforces a strict architecture:

```
_root (Primitives)
→ global (Semantic tokens: typography, spacing, layout, elevation)
→ theme (Semantic tokens: UI colors, states, interactions)
→ components
→ UI
```

### Core Principles

* Single source of truth via tokens
* No hardcoded values
* Strict naming and hierarchy
* Explicit rules (no assumptions)
* Designed for programmatic consumption (AI-ready)

---

## 2. Token Architecture

### 2.1 Root (Primitives)

* Contains raw values (colors, alpha, spacing, etc.)
* Prefixed with `_root.*`
* Never used directly in UI

Example:

```
_root.color.neutral.100
_root.color.brand.500
_root.alpha.neutral.050
```

---

### 2.2 Global Tokens

* Semantic tokens for **structure and layout**
* Includes:

  * Typography
  * Spacing
  * Layout
  * Elevation (shadow)

👉 Not tied to interaction states

---

### 2.3 Theme Tokens

* Semantic tokens used in UI
* Covers:

  * background
  * text
  * icon
  * border
  * elevation
  * focus

👉 All UI must use `theme.*` tokens

---

## 3. Color System

### 3.1 Modes

The system supports:

* Light mode
* Dark mode

Each token defines both values:

```
{
  "light": "...",
  "dark": "..."
}
```

---

### 3.2 Variants

Available variants:

```
neutral
brand
danger
warning
success
```

---

### 3.3 Intensity Scale

Each variant follows a consistent scale:

```
faint → lighter → medium → moderate → bolder → strong
```

Example:

```
theme.background.state.brand.medium.default
```

---

### 3.4 Fixed Tokens

Some tokens are identical across modes:

```
theme.text.global.neutral.fixed
```

👉 These must not change between light and dark

---

## 4. State System

### 4.1 Standard States

```
default
hovered
pressed
focused
disabled
```

---

### 4.2 Token Structure

States are defined as:

```
theme.[category].state.[variant].[intensity].[state]
```

Example:

```
theme.background.state.neutral.faint.hovered
```

---

### 4.3 Shared States

Shared states apply globally:

```
theme.background.state.shared.disabled
theme.text.state.shared.disabled
theme.icon.state.shared.disabled
```

---

## 5. Interaction Rules

### 5.1 Hover / Pressed

* Always use state tokens
* Never simulate with opacity or color manipulation

---

### 5.2 Focus

Focus is handled using dedicated tokens:

```
theme.focus.[variant].inner
theme.focus.[variant].offset
```

Rendering:

* Dual ring system (inner + offset)
* No background modification

---

### 5.3 Disabled

* Overrides all other states
* Uses shared disabled tokens

---

## 6. Component Architecture

### 6.1 Standard Props

All components follow:

```
size
variant
state
```

Plus:

* boolean flags (`isOpen`, `isSelected`, etc.)
* content props (`label`, `icon`, etc.)

---

### 6.2 State Logic

* `state` controls visual appearance
* Interaction maps to state
* `focused` always uses focus tokens

---

### 6.3 Composition Pattern

Components are composable:

```
input-field → input-base
combobox-field → combobox-base
select-field → select-base
```

👉 Field = structure (label, hint, etc.)
👉 Base = interactive element

---

### 6.4 Behavioral Flags

Common flags:

```
isSelected
isOpen
isFilled
isRequired
isInteractive
```

👉 These control behavior, not styling directly

---

## 7. Typography System

Structure:

```
text.heading (h1 → h4)
text.content.lead
text.content.emphasis
text.content.base
text.content.subtle
text.content.caption
```

Properties:

* Font: Inter
* Weights: 400 → 700
* Sizes: 12px → 48px
* Consistent line-height scale

---

## 8. Elevation System

Levels:

```
elevation.sm
elevation.md
elevation.lg
```

* Implemented via box-shadow
* Defined in tokens and effect styles

---

## 9. Layout System

Grid system:

```
lg → 12 columns
md → 8 columns
sm → 4 columns
```

Includes:

* gutters
* margins

---

## 10. Strict Rules (CRITICAL)

### MUST

* Use only `theme.*` tokens
* Respect naming conventions strictly
* Use predefined states only
* Use focus tokens for focus state
* Use effect styles for elevation and focus

---

### MUST NOT

* ❌ Use `_root` tokens in UI
* ❌ Hardcode values
* ❌ Create new states
* ❌ Infer missing tokens
* ❌ Modify colors manually

---

## 11. AI Implementation Rules

When generating code:

1. Always map UI → theme tokens
2. Never guess missing values → ask instead
3. Respect component API strictly
4. Prefer composition over duplication
5. Ensure accessibility (ARIA, focus visibility)

---

## 12. Expected Output

The system is designed to generate:

* React components
* TypeScript interfaces
* Tailwind-compatible styles
* Accessible UI (WCAG compliant)

---

## 13. Development Workflow

1. Use `tokens.json` as source of truth
2. Use `components.json` for component API
3. Follow README rules strictly
4. Do not deviate from token system

---

## 14. Important Notes

* This design system is deterministic
* No visual decision should be inferred
* Every UI element must be traceable to a token
* If a token is missing → stop and ask

---
