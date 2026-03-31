# AI Implementation Guide — Design System

## 1. Purpose

This document explains how to use the Design System files to generate UI components **without ambiguity**.

You must strictly follow the structure and rules defined here.

---

## 2. Source Files

You are provided with the following files:

### Core Files

* `tokens.json`
* `component-api.json`
* `component-mapping.json`
* `component-behavior.json`
* `component-examples.json`

---

## 3. System Architecture

The system follows a strict dependency chain:

```txt
_root → global → theme → mapping → components → UI
```

---

## 4. Token Usage Rules

### 4.1 Token Layers

#### `_root` (Primitives)

* Raw values (colors, spacing, typography)
* NEVER use directly in UI

#### `global`

* Layout and typography
* Used for spacing, grid, font styles

#### `theme`

* UI styling tokens
* ONLY source for:

  * background
  * text
  * icon
  * border
  * focus
  * elevation

---

### 4.2 Mandatory Rule

```txt
UI MUST use only theme.* tokens
```

---

### 4.3 Mode Handling

Tokens define:

```json
{
  "light": "...",
  "dark": "..."
}
```

You must:

* support both modes
* never hardcode colors

---

## 5. Component Generation Process

You must follow this exact order:

---

### Step 1 — Read component API

From `component-api.json`:

* identify props
* identify variants
* identify states
* identify slots (children)

---

### Step 2 — Apply mapping

From `component-mapping.json`:

* map tokens to:

  * background
  * text
  * border
  * icon
  * elevation
  * focus

For each:

* variant
* state

---

### Step 3 — Apply behavior

From `component-behavior.json`:

* state transitions
* interaction logic
* keyboard handling
* accessibility rules

---

### Step 4 — Validate with examples

From `component-examples.json`:

* ensure valid combinations
* avoid invalid states
* replicate real patterns

---

## 6. State System

### 6.1 Available States

```txt
default
hovered
pressed
focused
disabled
```

---

### 6.2 State Priority

```txt
disabled > focused > pressed > hovered > default
```

---

### 6.3 Rules

* Disabled overrides all states
* Focus always includes a ring (focus token)
* Hover and pressed must not be simulated

---

## 7. Component Structure

### 7.1 Base Pattern

Each component must:

* use props from `component-api.json`
* render slots properly
* apply tokens from mapping

---

### 7.2 Composition

Some components are composed:

```txt
input-field → input-base
combobox-field → combobox-base
select-field → select-base
```

---

## 8. Styling Rules

### 8.1 Mandatory

* Use tokens only
* No inline values
* No hardcoded colors
* No manual opacity

---

### 8.2 Forbidden

* ❌ Using `_root` directly
* ❌ Creating new tokens
* ❌ Inferring missing styles
* ❌ Modifying colors manually

---

## 9. Interaction Rules

### 9.1 Hover

* triggered on pointer hover
* uses `hovered` state tokens

---

### 9.2 Pressed

* triggered on pointer down
* uses `pressed` state tokens

---

### 9.3 Focus

* triggered on keyboard navigation
* must display focus ring

---

### 9.4 Disabled

* blocks all interaction
* overrides all visual states

---

## 10. Accessibility Rules

You must:

* use semantic HTML elements
* support keyboard navigation
* ensure visible focus
* use ARIA when needed

Examples:

* button → `<button>`
* input → `<input>`
* combobox → ARIA combobox pattern

---

## 11. Behavior Rules

From `component-behavior.json`:

* define open/close logic
* manage internal states
* synchronize UI and interaction

---

## 12. Validation Rules

Before generating code, ensure:

* all props are valid
* no invalid combinations
* mapping exists for all states
* behavior is defined

---

## 13. Output Requirements

You must generate:

* React components
* TypeScript types
* Token-based styling
* Accessible interactions

---

## 14. Error Handling

If something is missing:

```txt
DO NOT GUESS
ASK FOR CLARIFICATION
```

---

## 15. Final Rule

This system is deterministic.

```txt
No visual or behavioral decision should be inferred.
```

Every UI element must be:

```txt
Token → Mapping → Component → UI
```

---

## 16. Example Workflow

```txt
Generate Button:

1. Read Button API
2. Identify variant + state
3. Apply mapping tokens
4. Apply behavior rules
5. Validate with examples
6. Generate component
```

---

## 17. Summary

To build components:

* Follow the token hierarchy
* Use mapping for styling
* Use API for structure
* Use behavior for interaction
* Use examples for validation

---

This ensures:

* consistency
* scalability
* AI reliability
* production readiness

---
