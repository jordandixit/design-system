# Design System — AI Implementation Guide

This repository is the **single source of truth** for implementing UI components.  
Read this document fully before generating any code. Every rule here is non-negotiable.

---

## Repository structure

```
tokens/
├── root.json        ← Primitives (raw values, never used directly in components)
├── global.json      ← Semantic tokens — structure & layout (no color values)
└── theme.json       ← Semantic tokens — color (light & dark mode)

template/
└── component-prompt.md   ← Spec template to fill in for each component
```

---

## Token architecture

Tokens are organized in three strict layers. **Never skip a layer.**

```
root  (primitives)
  ↓
global  (semantic — structure)
  ↓
theme  (semantic — color)
  ↓
components
```

### Layer 1 — `root` (primitives)

Raw, non-semantic values. The source of all design decisions.

Contains: color palettes (neutral, brand, danger, warning, success + alpha variants), typography scale (font size, weight, line-height, letter-spacing), spacing, sizing, radius, border widths, grid columns and gutters.

**Never reference `root` tokens directly in component code.**  
They exist only to feed `global` and `theme`.

### Layer 2 — `global` (semantic — structure)

Named, reusable values for layout and typography. References `root` via `{root.*}`.

| Category | Tokens |
|---|---|
| `global.font.family` | `heading`, `content` |
| `global.font.size.heading` | `h1` (48px) → `h4` (28px) |
| `global.font.size.content` | `lead` (24px), `emphasis` (20px), `base` (16px), `subtle` (14px), `caption` (12px) |
| `global.font.weight` | `regular`, `medium`, `semibold`, `bold` |
| `global.font.leading` | Paired with each size level |
| `global.layout.padding` | `2xs` → `5xl` (2px → 64px) |
| `global.layout.gap` | `xs` → `4xl` (2px → 40px) |
| `global.layout.radius` | `xs` (2px) → `full` (999px) |
| `global.layout.border` | `thin` (1px), `thick` (2px), `thicker` (4px) |
| `global.layout.size` | `2xs` (4px) → `8xl` (64px) |
| `global.layout.grid` | `sm` (4 cols), `md` (8 cols), `lg` (12 cols) |

### Layer 3 — `theme` (semantic — color)

All color tokens. Every value has both a `Light` and `Dark` mode variant.  
**Components only use `theme` tokens for color. Never `root.color.*` directly.**

#### Token naming pattern

```
theme.[category].[type].[variant].[state]
```

**Categories:** `background`, `text`, `border`, `icon`  
**Types (for stateful tokens):** `global`, `state`  
**Variants (intensity scale):** `faint` → `lighter` → `medium` → `moderate` → `bolder` → `strong`  
**States:** `default`, `hovered`, `pressed`, `disabled` (disabled is under `state.shared`)

#### Examples

```
theme.background.state.brand.strong.default     → brand button background
theme.background.state.brand.strong.hovered     → brand button background on hover
theme.background.state.shared.disabled          → any disabled element background
theme.text.global.neutral.strong                → primary body text
theme.text.global.neutral.moderate              → muted/secondary text
theme.text.state.brand.bolder.default           → brand-colored interactive text
theme.border.state.danger.moderate.default      → danger input border
```

#### Light & dark mode

Each `theme` token contains both values. When generating CSS, always output both:

```css
/* Example: theme.background.state.brand.strong.default */
/* Light: root.color.brand.500 = #2b7fff */
/* Dark:  root.color.brand.500 = #2b7fff */

/* Example: theme.background.state.neutral.medium.default */
/* Light: root.color.neutral.100 = #f5f5f5 */
/* Dark:  root.color.neutral.900 = #171717  */
```

Implement dark mode using a CSS class or `prefers-color-scheme` media query — to be confirmed per component spec.

---

## State rules

These rules apply globally to every component.

- `disabled` overrides ALL other states. A disabled element never shows hover or focus styles.
- `focused` shows a focus ring. Use `theme.border.state.*` focus tokens.
- `hovered` and `pressed` are pointer-driven states.
- When `isLoading` and `isDisabled` are both true, `isDisabled` takes priority.

---

## Styling rules

- **Only use `theme` tokens for color.** No `root.color.*`, no hardcoded hex values.
- **Only use `global` tokens for spacing, sizing, radius, and typography.** No hardcoded pixel values.
- If a required token does not exist in the files, flag it with `⚠️ Missing token:` and stop. Do not invent a value.
- The visual source of truth is Figma. This repo is the implementation source of truth. Both must stay aligned.

---

## Accessibility

- All interactive elements must be keyboard-navigable.
- Focus is always visible. Never suppress `outline` without providing a custom focus ring using `theme.border` tokens.
- Disabled states use `aria-disabled="true"` in addition to (or instead of) the HTML `disabled` attribute where appropriate.
- Do not convey state or meaning through color alone. Always pair color with text, icon, or shape.
- Minimum contrast ratio: WCAG AA (4.5:1 for text, 3:1 for UI components).
- ARIA roles and attributes must be specified in the component prompt. If not specified, flag with `⚠️ ARIA role not defined`.

---

## Handling a component request

When you receive a component spec (from `template/component-prompt.md`):

1. Read the spec fully before writing any code.
2. Identify all variants, states, and props listed.
3. Map each visual property to the correct `theme` or `global` token.
4. Implement all states — do not skip any.
5. Apply state priority rules (disabled wins, etc.).
6. Verify accessibility attributes are included.
7. Generate the code.

---

## Handling ambiguity

If a spec is missing, incomplete, or contradictory:

1. Flag it at the top of your response with `⚠️ Ambiguity:` and describe what is unclear.
2. State your interpretation explicitly.
3. Generate the code using that interpretation.
4. Do not block or ask for confirmation — proceed and flag.

If a token mapping is missing from the files:

1. Flag it with `⚠️ Missing token:` and name the property.
2. Do not invent or approximate a value.
3. Leave the property as a clearly named placeholder: `/* TODO: missing token for [property] */`

---

## What you must not do

- Do not use `root` tokens directly in component styling.
- Do not hardcode any color, spacing, radius, or font value.
- Do not invent token names that do not exist in `root.json`, `global.json`, or `theme.json`.
- Do not simplify or merge states — implement every state as specified.
- Do not create unrequested wrapper components or abstractions.
- Do not reference files that do not exist in this repository (`component-api.json`, `component-mapping.json`, etc. do not exist — ignore any reference to them).
