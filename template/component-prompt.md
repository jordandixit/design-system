# Component: [ComponentName]

---

### 1. Summary

- **Figma name:** [Exact component name in Figma, e.g. "Button / Primary"]
- **Code name:** [Component name in code, e.g. `Button`]
- **Category:** [Atom / Molecule / Organism / Template]
- **Priority:** [High / Medium / Low]
- **Dependencies:** [Other required components, e.g. `Icon`, `Spinner` — or "none"]

---

### 2. Figma MCP link

> Attach the MCP link of the component.

Here is the link of the component and all its variables : [Component link]

---

### 3. Figma specs (Inspect panel)

> Copy-paste the content from Figma's "Inspect" panel for the master component.


```
Frame :

- Width : 
- Height : 
- Gap : 
- Padding : 
- Border Radius : 
- Fill : 
- Border :
- Border Weight :

─────────────────────────

Text :

- Text Style :

─────────────────────────

Icon Left :

- Width : 
- Height :
- Color :

─────────────────────────

Icon Right :

- Width : 
- Height :
- Color : 
```

---

### 4. Variants

> List all variation dimensions of the component.

| Properties   | Values                                                  |
|--------------|---------------------------------------------------------|
| size         | [sm, md, lg]                                            |
| variant      | [primary, secondary, tertiary, ghost, danger]           |
| state        | [default, hovered, focused, pressed, disabled]          |
| isOpen       | [true, false]                                           |
| hasIconLeft  | [true, false]                                           |
| hasIconRight | [true, false]                                           |
| IconLeft     | [instance swap]                                         |
| IconRight    | [instance swap]                                         |


---

### 5. State specifications

> Detail the visual changes for each state. Do not leave any field blank.

#### Default
- Background: `[token or hex value]`
- Text: `[token or hex value]`
- Border: `[token or "none"]`
- Cursor: `pointer`

#### Hovered
- Background: `[token or hex value]`
- Text: `[unchanged / new value]`
- Transition: `[e.g. background 200ms ease]`

#### Focused (focus-visible)
- Outline: `[e.g. 2px solid var(--color-brand-primary), offset 2px]`
- Background: `[unchanged / new value]`

#### Active (pressed)
- Background: `[token or hex value]`
- Transform: `[e.g. scale(0.98) / none]`

#### Disabled
- Background: `[token or hex value]`
- Text: `[token or hex value]`
- Opacity: `[e.g. 0.4 / fixed value]`
- Cursor: `not-allowed`
- Interaction: none (pointer-events: none)

#### Loading
- Shows: `[Spinner / Skeleton / other]`
- Label: `[hidden / replaced / preserved]`
- Interaction: blocked while loading

#### Error (if applicable)
- Background: `[token or hex value]`
- Border: `[token or hex value]`
- Message: `[error message behaviour]`

---

### 6. Behaviours & interactions

> Describe behaviours that are not visible in the screenshot.

- **Click:** [e.g. triggers `onClick`, blocked if `isLoading` or `isDisabled`]
- **Keyboard:** [e.g. activatable with `Enter` and `Space`]
- **Focus trap:** [e.g. yes inside a modal / no]
- **Loading animation:** [e.g. 16px spinner centred, label hidden with opacity:0]
- **Size transition:** [e.g. no animation on size change]
- **Icon only:** [e.g. forced 1:1 ratio, `ariaLabel` required, warn if missing]
- **Long label:** [e.g. truncated with ellipsis / wrapping allowed / min-content width]
- **[Other specific behaviour]**

---

### 7. Usage rules (do / don't)

**Do:**
- [e.g. Always pair a "danger" button with a confirmation dialog]
- [e.g. Use `ghost` for secondary actions inside forms]

**Don't:**
- [e.g. Never stack two primary buttons on the same line]
- [e.g. Do not use this component for navigation — use `Link` instead]

---


### 8. Additional information

> Anything that doesn't fit in the categories above.

- **Figma reference:** [Direct link to the component in Figma]
- **Existing Storybook:** [Link if applicable]
- **Similar components to avoid confusing with:** [e.g. do not confuse with `IconButton`, which is a separate component]
- **Designer notes:** [Any relevant Figma annotations]
- **[Other information]**
