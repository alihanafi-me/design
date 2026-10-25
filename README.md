# Design

![Abstract interface panels connected by a luminous path above a precision grid.](assets/design-cover.png)

**Thoughtful interfaces. Complete interactions. A shared standard for your agent.**

An installable skill for designing, building, and reviewing digital products.
It gives your coding agent a coherent standard for visual craft, accessibility, interaction behavior,
and the details that make an interface dependable.

Works with your product, brand, and technology stack. Use it for a single component, an important flow,
or a comprehensive design review.

## Install

```sh
npx skills add https://github.com/alihanafi-me/design --skill design
```

Choose your coding agent when prompted. Add `--global` to use the skill across projects,
or `--agent codex` / `--agent claude-code` to select an agent directly.

## From visual polish to reliable behavior

Good design carries through the entire task: what people see, what they understand, what happens when
something fails, and how they recover. The [complete standard](skills/design/references/DESIGN.md) brings these concerns together
across 18 sections and a web implementation checklist.

| Area | What the skill helps you consider |
| --- | --- |
| **Purpose & visual craft** | Real tasks, representative content, a deliberate visual direction, hierarchy, typography, color, assets, and reusable design rules. |
| **Layout & access** | Responsive behavior, reflow, keyboard navigation, focus, semantics, contrast, and assistive technology. |
| **Forms & interactions** | Clear labels, validation, saving states, consequential submissions, navigation, and destructive actions. |
| **State & trust** | Loading, empty and error states, stale responses, concurrency, recovery, privacy, and sensitive information. |
| **Language & context** | Localization, RTL and mixed-direction content, calendars, timezones, and regional conventions. |
| **Motion, data & speed** | Reduced motion, gesture alternatives, honest charts, usable tables, and responsive performance. |
| **Evidence & ownership** | Observable acceptance criteria, rendered review, user evaluation, maintained decisions, and explicit deviations. |

Apply the parts relevant to the product and task. Guidance for a capability does not mean you need to add it.

## Put it to work

After installation, describe the interface work naturally. The skill is available for automatic selection
when your request matches its UI/UX scope; you do not need to mention its name. Provide the relevant screens
or files, the intended task, and any existing design constraints.

Codex implicit invocation is explicitly enabled. Automatic selection depends on the agent and its settings;
you can still invoke **design** explicitly when you want to ensure it is selected.

**Build a component**

```text
Build this settings form in our existing design system.
Include validation, pending saves, failures, and recovery.
```

**Review an important flow**

```text
Review this checkout flow.
Prioritize consequential errors, keyboard access, and unclear state.
Report reproducible findings with concrete corrections.
```

**Go deeper**

```text
Review this interface comprehensively against the complete design standard.
Distinguish verified behavior, unmet requirements, and areas that still need evidence.
```

The skill routes focused tasks to the relevant sections and uses the complete standard for comprehensive
work. It follows existing product constraints and keeps findings grounded in the evidence available.
Automated checks support the review; rendered interaction and usability still require direct observation.

## Inside the skill

```text
skills/design/
├── SKILL.md
├── references/DESIGN.md
├── agents/openai.yaml
└── LICENSE
```


[**SKILL.md**](skills/design/SKILL.md) is the agent entrypoint: workflow, scope, and navigation.
[**DESIGN.md**](skills/design/references/DESIGN.md) is the authoritative standard.
[**agents/openai.yaml**](skills/design/agents/openai.yaml) enables implicit invocation in Codex. The skill and its reference ship together, so the installed skill
can read the standard locally without fetching a separate document.

The standard distinguishes mandatory requirements, strong defaults, and conditional guidance.
It also separates an authorized release deviation from satisfying a requirement: accepting a risk does
not establish conformance. The skill supports implementation and review; it does not certify accessibility,
security, or legal compliance.

## Contribute

Read [AGENTS.md](AGENTS.md) before making changes. Keep the standard broadly reusable, preserve its
applicability and requirement language, and keep the skill's section routing synchronized.
[CLAUDE.md](CLAUDE.md) points to the same maintenance instructions.

## License

[MIT](LICENSE) © 2026 Ali Hanafi.
