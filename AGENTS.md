# Repository instructions

Read `README.md` before modifying this repository.

- This repository contains a reusable design standard and an installable agent skill, not an application.
- Keep `skills/design/references/DESIGN.md` as the single authoritative standard. Keep the workflow and section routing in
  `skills/design/SKILL.md`; do not maintain a second copy of the standard.
- Keep content framework-neutral and generic. Do not introduce source-product names, private paths,
  credentials, application fixtures, or mandatory brands, stacks, palettes, fonts, or libraries.
- Preserve the MIT license and attribution. Keep `LICENSE` and `skills/design/LICENSE` identical
  so the installed skill retains its license.
- Preserve stated applicability, normative strength, accessibility thresholds, and defined exceptions.
  Distinguish criterion-defined exceptions from non-conforming deviations and release authorization
  from conformance. Do not imply that a risk acceptance satisfies an unmet requirement.
- Do not turn conditional capabilities into mandatory features or expand the user's authorized scope.
- Keep the skill self-contained: use relative references that remain available after installation.
  Keep its YAML name `design` synchronized with installation examples.
- Keep `README.md`, `AGENTS.md`, and `CLAUDE.md` focused on use and repository maintenance.
  The installed skill must not depend on maintenance instructions to function.
- Verify skill frontmatter, relative links, section routing, and installer discovery after packaging changes.
  Test installation in an isolated temporary project, not in a consuming application.
- Report actual verification and its limits. Static checks do not establish rendered accessibility,
  usability, security, legal compliance, or complete conformance.
- Do not add dependencies, lockfiles, generated output, application code, hooks, or CI unless requested.
