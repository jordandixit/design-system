# Component Rules

> Generated from the current repo structure. Validate final visual details against Figma.

## accordion

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Keep trigger width and popup alignment consistent across states.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## avatar-base

**When to use**  
Use to represent a user, entity, or profile.

**When not to use**  
Do not rely on image presence only; provide fallback initials or placeholder.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## avatar-label

**When to use**  
Use to represent a user, entity, or profile.

**When not to use**  
Do not rely on image presence only; provide fallback initials or placeholder.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## badge

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## banner

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Keep content concise and action-oriented.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## breadcrumb

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## button

**When to use**  
Use for direct user-triggered actions.

**When not to use**  
Do not use to represent selected state without a persistent toggle model.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Reserve primary for the main action in a local area.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## button-icon

**When to use**  
Use for direct user-triggered actions.

**When not to use**  
Do not use to represent selected state without a persistent toggle model.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Reserve primary for the main action in a local area.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## button-icon-menu

**When to use**  
Use for direct user-triggered actions.

**When not to use**  
Do not use to represent selected state without a persistent toggle model.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Keep trigger width and popup alignment consistent across states.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## calendar

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## calendar-date

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## card-action

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## card-image

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## checkbox-base

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Using the wrong control type for the decision pattern.

## checkbox-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## chip-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## combobox-base

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Pair error state with helper or error text, not color alone.
- Keep trigger width and popup alignment consistent across states.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Treating open state as a separate visual variant unrelated to focus and popup behavior.

## combobox-field

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Use the field as a wrapper for label, required marker, hint text, and validation copy; keep interaction in the base control.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Embedding logic-only booleans in the field wrapper instead of the base control.

## datepicker-base

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Keep trigger width and popup alignment consistent across states.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Treating open state as a separate visual variant unrelated to focus and popup behavior.

## datepicker-field

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Use the field as a wrapper for label, required marker, hint text, and validation copy; keep interaction in the base control.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Embedding logic-only booleans in the field wrapper instead of the base control.

## divider

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## dropdown-item

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## dropdown-list

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## dropdown-search

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## dropdown-title

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## input-base

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Pair error state with helper or error text, not color alone.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## input-field

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Use the field as a wrapper for label, required marker, hint text, and validation copy; keep interaction in the base control.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Embedding logic-only booleans in the field wrapper instead of the base control.

## link

**When to use**  
Use for direct user-triggered actions.

**When not to use**  
Do not use to represent selected state without a persistent toggle model.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Use link only for navigation, never for destructive or form-submit actions.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## modal

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Keep content concise and action-oriented.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## pagination

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## pagination-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## password-base

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Pair error state with helper or error text, not color alone.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## password-field

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Use the field as a wrapper for label, required marker, hint text, and validation copy; keep interaction in the base control.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Embedding logic-only booleans in the field wrapper instead of the base control.

## progress

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## progress-value

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## radio-base

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Using the wrong control type for the decision pattern.

## radio-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## scrollbar

**When to use**  
Use to organize content, reveal structure, or group related actions.

**When not to use**  
Do not encode business state only through layout treatment.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## search-base

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Pair error state with helper or error text, not color alone.
- Keep trigger width and popup alignment consistent across states.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Treating open state as a separate visual variant unrelated to focus and popup behavior.

## search-field

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Use the field as a wrapper for label, required marker, hint text, and validation copy; keep interaction in the base control.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Embedding logic-only booleans in the field wrapper instead of the base control.

## segemented

**When to use**  
Use according to the nested content and semantics.

**When not to use**  
Do not repurpose without documenting behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## segmented-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## select-base

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Pair error state with helper or error text, not color alone.
- Keep trigger width and popup alignment consistent across states.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Treating open state as a separate visual variant unrelated to focus and popup behavior.

## select-field

**When to use**  
Use for data entry, search, selection, or date picking.

**When not to use**  
Do not use validation colors as the only way to explain errors.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Use the field as a wrapper for label, required marker, hint text, and validation copy; keep interaction in the base control.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Embedding logic-only booleans in the field wrapper instead of the base control.

## status-icon

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## switch-base

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Using the wrong control type for the decision pattern.

## switch-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## tab-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Expose selected state through both color and semantic/ARIA state.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## table

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Placing dense forms inside cells without spacing and focus management.

## table-body

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Placing dense forms inside cells without spacing and focus management.

## table-body-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Placing dense forms inside cells without spacing and focus management.

## table-header

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Placing dense forms inside cells without spacing and focus management.

## table-header-item

**When to use**  
Use when the user chooses one or more options.

**When not to use**  
Do not mix selection semantics across checkbox/radio/switch behavior.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
- Placing dense forms inside cells without spacing and focus management.

## tag

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## toast

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Keep content concise and action-oriented.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## tooltip

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Keep content concise and action-oriented.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.

## tooltip-icon

**When to use**  
Use to communicate status, context, or short metadata.

**When not to use**  
Do not overload with dense workflows or primary form logic.

**Best practices**
- Use only semantic theme tokens for UI rendering.
- Keep state handling explicit; never simulate hover/pressed with opacity-only changes.
- Pair error state with helper or error text, not color alone.

**Anti-patterns**
- Mixing disabled with any interactive affordance.
- Using hardcoded colors instead of token-driven rendering.
