---
name: design
description: Design, implement, improve, and review digital interfaces using a framework-neutral product design standard. Use when creating or changing user-facing pages, layouts, components, forms, navigation, or interaction flows, or reviewing UI/UX, visual hierarchy, accessibility, responsive behavior, RTL, and interface states. Apply to relevant interface work even when the user does not explicitly ask for design guidance.
license: MIT
---

# Design

Use the bundled [DESIGN.md](references/DESIGN.md) as the authoritative standard. This skill supports both
implementation and review; it does not prescribe a brand, stack, library, or fixed visual aesthetic.

## Apply the standard

Understand the requested task, audience, primary actions, existing design system, supported environments,
and available evidence. Inspect relevant code and existing interfaces before changing them. Preserve the
user's product choices and authorized scope. Conditional guidance does not authorize adding capabilities.

Read the purpose and scope and section 1 of `references/DESIGN.md` for requirement language and applicability, and sections 16–18 for acceptance,
non-conforming deviations, governance, and completion. Read the full relevant sections using the routing
below; headings are navigation, not substitutes for the requirements. For a comprehensive design or audit,
read the complete standard. For a focused task, assess the relevant sections and describe the review boundary.
The reference is long: locate a section by searching for its heading, such as `^## 6\.` or `^### 7\.4`, and
read it through to the next heading of the same level. If the reference cannot be read, report that limitation
instead of claiming to have applied it.

An unmet MUST remains non-conforming. A permitted release deviation is different from meeting a requirement;
recording an exception does not establish compliance or authorize disregarding binding obligations.

## Find the relevant requirements

All section numbers below refer to `references/DESIGN.md`.

| Task or concern | Read |
| --- | --- |
| Audience, task discovery, existing experience, alternatives, realistic content | 2 |
| Visual direction for new or open-ended work, avoiding templated defaults | 2.6 |
| Visual hierarchy, typography, color, assets, tokens, layering, fallbacks | 3 |
| Labels, instructions, content, asynchronous messages | 4 |
| Responsive layout, scrolling, zoom, reflow, native-platform adaptations | 5 |
| Semantics, keyboard, focus, overlays, contrast, targets, timing, assistive technology | 6 |
| Forms, validation, consequential submission, saving, unsaved work | 7 |
| Navigation, URLs, feedback, destructive or bulk actions | 8 |
| Loading, empty/error states, stale responses, optimism, offline/concurrent work, scope, onboarding, notifications, deceptive choices, assistants | 9 |
| Privacy, sensitive information, authorization presentation, identity/session transitions | 10 |
| Translation, RTL, mixed direction, calendars, timezones, numerals | 11 |
| Motion, reduced motion, gestures and alternatives | 12 |
| Charts, exact data, accessible alternatives, tables | 13 |
| Font/image loading, responsiveness, performance budgets | 14 |
| Automated checks, rendered review, representative user evaluation, evidence | 15 |
| Acceptance, risk, deviations, maintained decisions, definition of done | 16–18 |
| Web implementation and code review techniques | Appendix A |

Apply overlapping sections together. For example, a consequential form needs sections 6–10 as relevant,
not just field styling; a chart needs the applicable accessibility and localization requirements too.

## Implement or improve an interface

Translate the relevant requirements into observable acceptance criteria for the requested scope. Use the
existing design language and components when appropriate. Where no system exists or the brief leaves visual
choices open, follow section 2.6 to set a deliberate direction. For web work, use Appendix A as a checklist.
Resolve normal, pending, empty, invalid, failed, interrupted, and recovery states for applicable flows. Keep
displayed state and promises aligned with actual persistence, permissions, scope, and recovery behavior.

Use representative content and relevant viewport, input, language, direction, and theme conditions.
Verify changes with available tools and direct interface inspection. Match the depth of verification to the
change and risk; do not substitute a screenshot or automated accessibility scan for complete behavior checks.
Use supplied or already-available tools without treating this skill as authorization for installations,
external writes, publication, or unrelated configuration changes.

## Review an interface

Inspect evidence before reporting a finding. For web code, use Appendix A to locate common defects. Where
possible, reproduce the behavior and identify the relevant requirement, affected users or task, location
(`file:line` for code), impact, and a concrete correction. Distinguish a reproducible failure from an
unverified risk or an aesthetic preference. Do not invent observed behavior from static code or a screenshot.

For a focused review, inspect the requested area plus directly related consequential interactions.
For a comprehensive review, assess the complete standard and explicitly distinguish applicable,
non-applicable, satisfied, unmet, and unverified requirements. Prioritize barriers, misleading states,
loss of work, privacy exposure, and consequential errors according to observed impact.

## Deliver the result

Report what changed or what needs correction, the relevant evidence and checks actually performed, and any
remaining limitations. Preserve the distinction between release readiness and conformance. Never claim full
accessibility, security, legal compliance, or usability from partial inspection or automated checks alone.
