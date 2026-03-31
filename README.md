# AI-Ready Design System Documentation

## 1. Overview

This design system is built for **scalable UI development and AI-driven implementation**.

It follows a strict multi-layer architecture:

```
_root (Primitives)
→ global (Semantic tokens: typography, layout, spacing, shadow)
→ theme (Semantic tokens: UI colors, states, interactions)
→ components
→ UI
```

---

## 2. Token Architecture

### 2.1 Root (Primitives)

Defined in 

* Contains all raw values:

  * colors
  * alpha
  * typography base values
  * spacing
  * sizing
  * radius
  * grid
* Prefixed with `_root.*`
* **Never used directly in UI**

Example:

```
_root.color.neutral.500
_root.alpha.brand.200
_root.space.16
_root.radius.8
```

---

### 2.2 Global Tokens

Defined in 

Used for **structure and layout only**:

* Typography (font, size, weight, leading, tracking)
* Layout (grid, spacing, padding, gap)
* Radius, border width
* Shadow primitives

👉 These tokens map directly to `_root`

Example:

```
global.font.size.heading.h1 → _root.font.size.48
global.layout.padding.md → _root.space.8
```

👉 Global tokens are **not state-based**

---

### 2.3 Theme Tokens

Defined in `theme.json`

Used for **UI rendering only**:

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

Each token supports:

* Light mode
* Dark mode

Structure:

```
{
  "light": "...",
  "dark": "..."
}
```

---

### 3.2 Variants

```
neutral
brand
danger
warning
success
```

---

### 3.3 Intensity Scale

Each variant follows:

```
faint → lighter → medium → moderate → bolder → strong
```

Example:

```
theme.background.state.brand.medium.default
```

---

### 3.4 Fixed Tokens

Some tokens are mode-independent:

```
theme.text.global.neutral.fixed
```

👉 Same value in light and dark

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

```
theme.[category].state.[variant].[intensity].[state]
```

Example:

```
theme.background.state.neutral.faint.hovered
```

---

### 4.3 Shared States

Global states:

```
theme.background.state.shared.disabled
theme.text.state.shared.disabled
theme.icon.state.shared.disabled
```

---

## 5. Interaction Rules

### 5.1 Hover / Pressed

* Always use state tokens
* Never use opacity or manual color changes

---

### 5.2 Focus

Focus is handled via tokens + effects:

* Tokens: `theme.focus.*`
* Effects: defined in styles

Structure:

```
theme.focus.[variant].inner
theme.focus.[variant].offset
```

Rendering:

* dual ring (inner + offset)
* no background override

---

### 5.3 Disabled

* Overrides all states
* Uses shared tokens

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

* `state` = visual representation
* interaction → maps to state
* `focused` always uses focus tokens

---

### 6.3 Composition Pattern

Components are composable:

```
input-field → input-base
combobox-field → combobox-base
select-field → select-base
datepicker-field → datepicker-base
```

👉 Field = structure (label, hint)
👉 Base = interaction

---

### 6.4 Behavioral Flags

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

Based on global tokens:

```
heading → h1, h2, h3, h4
content → lead, emphasis, base, subtle, caption
```

Properties:

* Font: Inter
* Weight: 400 → 700
* Size: 12px → 48px
* Line-height from `_root.font.leading`
* Tracking from `_root.font.tracking`

---

## 8. Layout System

Grid:

```
lg → 12 columns
md → 8 columns
sm → 4 columns
```

Includes:

* margin
* gutter
* padding
* gap

---

## 9. Elevation System

Based on:

* global shadow tokens
* theme elevation tokens

Levels:

```
elevation.sm
elevation.md
elevation.lg
```

---

## 10. Strict Rules (CRITICAL)

### MUST

* Use ONLY `theme.*` tokens in UI
* Use `global.*` for layout and typography
* Respect naming structure exactly
* Use predefined states only
* Use focus tokens for focus

---

### MUST NOT

* ❌ Use `_root` tokens in UI
* ❌ Hardcode values
* ❌ Create new tokens
* ❌ Infer missing values
* ❌ Apply manual color transformations

---

## 11. AI Implementation Rules

When generating code:

1. Use `theme.*` for UI styling
2. Use `global.*` for layout and typography
3. Never resolve `_root` manually
4. Never guess missing tokens → ask
5. Respect component API strictly
6. Prefer composition over duplication
7. Ensure accessibility (ARIA, focus visible)


---

## 12. Development Workflow

1. `_root` = raw values
2. `global` = layout & typography
3. `theme` = UI styling
4. `components` = API contract

👉 Always follow this chain:

```
_root → global/theme → component → UI
```

---

## 13. Important Notes

* This system is deterministic
* No visual decision should be inferred
* Every UI element must map to a token
* If a token is missing → STOP and ask

---
