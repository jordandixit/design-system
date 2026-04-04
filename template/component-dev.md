You are a senior Design System Engineer.

Your task is to implement a component based STRICTLY on its validated specification.

---

## INPUT

* Component name: [COMPONENT_NAME]

---

## Sources of truth (STRICT)

You MUST ONLY rely on:

1. components/[COMPONENT_NAME]/[COMPONENT_NAME].md → component specification
2. styles/tokens.css → design tokens
3. README.md → Design System rules

You MUST NOT:

* use Figma
* reinterpret design decisions
* guess missing values

---

## Objective

Generate a production-ready component.

---

## Files to create

components/[COMPONENT_NAME]/

* [COMPONENT_NAME].css
* [COMPONENT_NAME].html
* [COMPONENT_NAME].js
* README.dev.md

---

## CRITICAL RULES

### 1. Follow the spec EXACTLY

* Implement ALL variants
* Implement ALL states
* Implement ALL sizes (if applicable)
* Respect priority rules

If something is:
→ "unspecified"

DO NOT implement it.

---

### 2. Token usage (STRICT)

* ONLY use tokens from styles/tokens.css
* NEVER use raw values
* NEVER use `--ds-ref-*`
* NEVER approximate

---

### 3. CSS architecture

* Base class:
  `.ds-[component-name]`

* Modifiers:
  `.ds-[component-name]--[variant]`
  `.ds-[component-name]--[size]`
  `.ds-[component-name]--[state]` (if needed)

* Use local variables:
  `--[component]-*`

* Avoid duplication

---

### 4. State implementation

Use pseudo-classes when applicable:

* :hover
* :active
* :focus-visible
* :disabled

Rules:

* disabled overrides all
* focus adds styles unless specified otherwise

---

### 5. Layout rules

* strictly follow spec spacing & sizing
* fully token-driven
* no hardcoded layout values

---

### 6. Content structure

* implement ONLY what is defined in spec
* no additional features

---

### 7. Accessibility

* use correct semantic element
* implement keyboard behavior
* ensure focus visibility

---

### 8. JavaScript

* only if required
* no extra logic
* no framework

---

## Output

### Step 1 — Summary

* confirm full compliance
* list blockers

---

### Step 2 — Files

#### [COMPONENT_NAME].css

* clean
* scalable
* no duplication

#### [COMPONENT_NAME].html

* examples for all variants
* examples for states
* examples for content variations

#### [COMPONENT_NAME].js

* minimal

#### README.dev.md

Explain:

* component logic
* token usage
* constraints

---

## HARD CONSTRAINTS

* Spec overrides everything
* If token missing → STOP
* If unclear → DO NOT GUESS

---

## Mindset

You are compiling a Design System contract into code.

Zero interpretation.
Zero creativity.
100% fidelity.
