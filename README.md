🧠 1. Overview

This design system is designed for scalable product development and AI-driven implementation.

It enforces a strict architecture:

_root (Primitives)
→ global (Semantic tokens for layout, typography, elevation)
→ theme (Semantic tokens for UI colors & interactions)
→ components
→ UI
Core Principles
Single source of truth via tokens
No hardcoded values
Strict naming and hierarchy
Explicit rules (no assumptions)
Designed for programmatic consumption (AI-friendly)
🧱 2. Token Architecture
2.1 Root (Primitives)

Defined in

Raw values only (colors, spacing, alpha, etc.)
Never used directly in components

Example:

_root.color.neutral.100
_root.color.brand.500
_root.alpha.neutral.050
2.2 Global (Semantic — Structure & Layout)

Defined in

Used for:

Typography
Spacing
Layout
Elevation (shadow tokens)

👉 These tokens are not tied to UI states

2.3 Theme (Semantic — UI)

Defined in

Used for:

background
text
icon
border
elevation
focus
🎨 3. Color System
3.1 Modes

The system supports:

Light mode
Dark mode

Each token defines:

"value": {
  "Light": "...",
  "Dark": "..."
}

👉 Example:

theme.background.global.base
3.2 Fixed Tokens

Some tokens are mode-independent:

theme.text.global.neutral.fixed

👉 Same value in Light and Dark

3.3 Variants

Supported variants:

neutral
brand
danger
warning
success
3.4 Intensity Scale

Each variant follows a consistent scale:

faint → lighter → medium → moderate → bolder → strong

👉 Example:

theme.background.state.brand.medium.default
⚙️ 4. State System
4.1 Standard States

Used across components:

default
hovered
pressed
focused
disabled
4.2 State Structure

States are defined in tokens:

theme.background.state.[variant].[intensity].[state]

👉 Example from your system:

theme.background.state.neutral.faint.hovered
4.3 Shared States

Shared tokens exist for cross-component behavior:

theme.background.state.shared.disabled
theme.text.state.shared.disabled
theme.icon.state.shared.disabled
🎯 5. Interaction Rules
5.1 Hover / Pressed
Always use dedicated state tokens
Never apply opacity or color transformations manually
5.2 Focus

Focus is handled via focus tokens + effect styles

Defined in:

(tokens)
(effects)

👉 Structure:

theme.focus.[variant].inner
theme.focus.[variant].offset

👉 Rendering:

dual ring (inner + offset)
no background override
5.3 Disabled
Disabled overrides ALL states
Uses shared tokens
🧩 6. Component Architecture
6.1 General Pattern

All components follow:

size
variant
state
+ boolean props
+ content props
6.2 State Logic
state = visual state (not interaction logic)
Interaction (hover, focus) maps to state visually
focused ALWAYS uses focus tokens (ring)
6.3 Composition

Components are composable:

input-field → input-base
combobox-field → combobox-base
select-field → select-base

👉 Field = label + hint + base component

6.4 Controlled Flags

Common flags:

isSelected
isOpen
isFilled
isRequired
isInteractive

👉 These drive UI behavior (not styling directly)

🎨 7. Typography System

Defined in

Structure
text.heading.h1 → h4
text.content.lead
text.content.emphasis
text.content.base
text.content.subtle
text.content.caption
Properties
font-family: Inter
weight: 400 → 700
sizes: 12px → 48px
consistent line-height scale
🌫 8. Elevation System

Defined in:

(tokens)
(effects)
Levels
elevation.sm
elevation.md
elevation.lg

👉 Implemented as box-shadow

🔲 9. Layout System

Defined in

Grid
lg → 12 columns
md → 8 columns
sm → 4 columns

With:

gutters
margins
🚫 10. Strict Rules (CRITICAL FOR AI)
MUST
Use ONLY semantic tokens (theme.*)
Respect naming structure exactly
Use predefined states only
Use focus tokens for focus state
Use effect styles for elevation and focus
MUST NOT
❌ Use _root tokens in UI
❌ Hardcode colors
❌ Create new states
❌ Infer missing values
❌ Apply opacity manually
🧠 11. AI Implementation Rules

When generating code:

Always map UI → theme tokens
Never guess missing tokens → ask instead
Respect component API strictly
Prefer composition over duplication
Ensure accessibility (focus visible, semantic HTML)
⚛️ 12. Expected Output (for AI)
React components
TypeScript props
Tailwind-compatible structure
Accessible (ARIA compliant)
Token-driven styling only
