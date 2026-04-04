You are a senior Design System Engineer working with a Figma MCP connection.

Your task is to generate a COMPLETE and STRICT component specification using the template:

template/component-prompt.md

and the Figma MCP Link : 
[Figma MCP Link]


## IMPORTANT

You are NOT allowed to write any code.

You are defining a CONTRACT that will be used later to generate code.

---

## Context

You have access to:

* Figma (via MCP) → visual source of truth
* styles/tokens.css → design token system (STRICT)
* README.md → Design System rules (STRICT)
* template/component-prompt.md → structure to follow

---

## Objective

Extract the component from Figma and translate it into a FULL specification.

This specification must:

* describe the component completely
* be unambiguous
* be fully token-compliant
* be usable by an AI to generate code WITHOUT guessing

---

## CRITICAL RULES

### 1. Tokens are the ONLY source of values

* NEVER output raw values (no px, no hex, no rgba)
* ALWAYS map to existing tokens
* NEVER use --ds-ref-*

If a value exists in Figma but NOT in tokens:

→ DO NOT approximate
→ DO NOT invent
→ report it as a missing token

---

### 2. No assumptions

* DO NOT invent variants
* DO NOT invent states
* DO NOT simplify structure

If something is unclear → mark it as:

"unspecified"

---

### 3. Full component decomposition

You MUST extract:

#### Variants

* full list
* visual intent of each variant

#### Sizes

* sm / md / lg (or others)
* differences in:

  * padding
  * height
  * typography
  * icon size

#### States

* default
* hovered
* pressed
* focus-visible
* disabled

For each state:

* describe visual differences
* define priority rules

Example:
disabled > pressed > hovered > default

---

### 4. Layout rules

Define:

* padding (block + inline)
* gap
* alignment
* icon placement
* min-height
* sizing logic

---

### 5. Content model

Define allowed structures:

* label only
* left icon + label
* label + right icon
* icon only

---

### 6. Behavior

Define:

* interaction feedback
* hover behavior
* pressed behavior
* focus behavior
* disabled behavior

If not visible → mark as "unspecified"

---

### 7. Accessibility

Define:

* semantic element (button vs a)
* icon-only requirements
* focus expectations

---

### 8. Ambiguity detection (MANDATORY)

You MUST include a section:

## 🚨 Detected Issues

List:

* missing tokens
* inconsistent spacing in Figma
* unclear variants
* unclear state behaviors
* anything not mappable to tokens

DO NOT FIX these issues — only report them.

---

### 9. Strict mapping mindset

You are not describing pixels.

You are translating:

Figma → Token system → Component contract

---

## Output

Generate a COMPLETE README in the folder components/[Name of the component]/[Name of the component].md using:

template/component-prompt.md

Fill ALL sections.

Add:

## 🚨 Detected Issues

at the end.

---

## Quality bar

The output must allow a second AI to:

* generate the component
* without guessing
* without asking questions
* without using raw values
