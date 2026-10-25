# Product design standards

## Purpose and scope

Design digital products around the people using them, the work they need to complete, and the conditions in
which they work. This standard establishes reusable principles for creating interfaces that are
understandable, accessible, reliable, secure, adaptable, performant, and appropriate to their context.

It applies to public-facing pages, authenticated applications, internal tools, administrative interfaces,
documentation, data-intensive workspaces, and other digital experiences, to the extent relevant to the product
being built.

The standard defines expected qualities and behaviors without prescribing a universal brand, visual style,
color palette, typeface, technology stack, component library, or layout. Product requirements determine which
capabilities exist and what they are allowed to do. Design makes those capabilities understandable and usable.
Implementation enforces their actual behavior, permissions, and constraints.

Apply requirements in proportion to the capabilities, risks, audiences, and operating conditions of the
product. Guidance about charts, collaboration, offline work, authentication, assistants, or other specialized
interactions does not authorize adding those features. A requirement becomes applicable when the corresponding
capability, risk, or user need exists.

The objective is not to maximize visual polish, feature count, engagement, or compliance-checklist completion
in isolation. It is to help people complete legitimate tasks accurately, efficiently, confidently, and with
appropriate control, while avoiding preventable harm, confusion, exclusion, and loss of work.

## 1. Requirement language and applicability

Use the following terms consistently throughout this standard.

- **MUST:** A mandatory requirement when its stated conditions apply. An unmet MUST requirement remains
  non-conforming until it is satisfied. A formally documented exception may authorize a release decision only
  when this standard's governance permits it and all applicable legal, safety, security, and external
  conformance obligations remain satisfied. An exception does not make the requirement satisfied, establish
  compliance, or justify a conformance claim. Every accepted deviation MUST identify its scope, rationale,
  residual risk, mitigation, accountable owner, and review condition.
- **SHOULD:** A strong default that is expected to be followed unless a specific, evidence-based reason
  justifies an alternative.
- **MAY:** An optional approach that can be used when it supports the context and does not conflict with
  applicable requirements.
- **WHEN APPLICABLE:** A conditional requirement that applies only when the associated capability,
  interaction, risk, or user need exists.
- **RECOMMENDED TARGET:** A practical design or engineering goal that supports quality but is not, by itself,
  a universal conformance requirement.

These terms describe the strength of a requirement, not the relative importance of the user need. An
applicable legal obligation, security control, accessibility requirement, or safety-critical behavior remains
binding regardless of whether a design team considers it visually important.

Every requirement MUST be interpreted in its actual context. Its stated scope and defined exceptions
determine applicability. Platform conventions, user needs, and technical constraints inform implementation;
they do not independently waive an applicable MUST requirement. Any unmet MUST requirement MUST follow the
non-conforming-deviation process and MUST NOT be silently treated as compliant.

A criterion-defined exception or permitted alternative, whose conditions are actually met, is different from
accepting an unmet requirement. The former can satisfy the applicable criterion; a release deviation leaves
the unmet requirement non-conforming. Establish the conditions rather than using either label as a blanket
waiver.

Distinguish four kinds of guidance:

1. **Principles** explain the outcomes that design should achieve.
2. **Requirements** define expected behavior or constraints.
3. **Patterns** describe reusable ways to meet those requirements.
4. **Acceptance criteria** define observable evidence that a particular implementation satisfies a
   requirement.

A pattern is not mandatory simply because it appears in this document. Choose the implementation that best
meets the requirement in the given context.

Capitalized requirement words carry the strength defined above. Unmarked prose explains intent, examples, and
recommended practice; it does not introduce additional universal MUST requirements. A recommended target can
become a project acceptance criterion through an explicit product decision. Do not turn a contextual example
into a blanket rule.

When requirements appear to conflict, first check their scope, platform, conditions, and exceptions. Resolve
the intended behavior explicitly rather than selecting whichever statement is easier to satisfy. Design
preferences cannot waive an applicable accessibility, security, safety, or legal obligation.

## 2. Understand the context before designing

### 2.1 Identify the people, tasks, and environment

Before materially changing an interface, establish the intended audience, primary tasks, frequency of use,
content characteristics, user capabilities, operational environment, risks, and success criteria.

Consider the differences between a first-time visitor evaluating a service, an expert handling dense records,
an administrator managing permissions, and a reader consuming long-form information. These users may need
different information density, navigation, feedback, safeguards, and levels of explanation.

Account for relevant conditions such as limited bandwidth, intermittent connectivity, older devices, small
screens, noisy environments, assistive technology, language proficiency, time pressure, and the consequences
of mistakes.

Establish the supported browsers, platforms, devices, input methods, assistive technologies, and network
conditions. Define acceptable fallback behavior and meaningful exclusions. Browser support is a maintained
compatibility decision, not an assumption based on one development machine.

Use research, analytics, support evidence, observation, stakeholder knowledge, and representative user
evaluation as appropriate. Distinguish verified findings from assumptions, preferences, and hypotheses.

Do not treat personal taste, current design trends, stakeholder preference, or ease of implementation as
sufficient evidence of user benefit.

### 2.2 Inspect existing experiences before changing them

For existing products, inspect current journeys, information architecture, navigation, terminology, brand
assets, component behavior, accessibility strengths, established expectations, and known failures before
redesigning.

Preserve useful conventions unless changing them serves an identified purpose. Avoid unnecessary disruption to
familiar workflows, bookmarks, URLs, keyboard behavior, or user expectations.

Coordinate consequential changes to routes, information architecture, terminology, legal wording, product
identity, permissions, and system behavior with their responsible owners.

Identify dependencies between screens and shared components before making changes that could affect multiple
workflows.

Capture the relevant baseline: URLs, fragment anchors, direct links, page titles and metadata, indexed or
prerendered content, form names and autofill behavior, and shared interaction contracts. When destinations
change, plan redirects and update links and metadata deliberately. Verify direct loading and navigation after
the change, not only the route reached through an already-running application.

### 2.3 Explore meaningful alternatives

Sketch or prototype significant flows and layout alternatives before committing to implementation. Compare
alternatives against the actual task, content, risk, accessibility, and technical constraints.

Use proportionate effort. Small, low-risk corrections do not require an elaborate discovery process; major
changes to critical workflows warrant stronger investigation and validation.

State the intended design direction and explain consequential decisions, including known trade-offs. Familiar
patterns are appropriate when they serve the task. Novelty alone is not a reason to replace them.

Describe the intended visual character through the subject, audience, identity, and task. Choose coherent
relationships among typography, imagery, spacing, density, color, and motion. Expressiveness can strengthen
identity or comprehension, while repeated and consequential controls benefit from stable behavior. Neither
ornamental novelty nor visual neutrality is a universal goal.

Review the whole composition: where attention goes first, what remains memorable, how sections relate, and
whether the main task stays clear. Repetition can support comparison; variation can express hierarchy. Neither
a fixed template for every subject nor a different layout for every section is a design requirement.

### 2.4 Use representative content and realistic scenarios

Work with representative content from the earliest practical stage. Include long names, dense tables, empty
and populated collections, multilingual text, mixed-direction content, large numbers, unusual dates, lengthy
errors, and difficult user-entered values.

Identify demonstration data and placeholder content clearly. Content MUST NOT invent customer endorsements,
performance claims, availability, statistics, testimonials, or screenshots presented as evidence of a real
product. Synthetic data can exercise realistic conditions, but realistic-looking numbers do not become real
evidence.

Test both ordinary and exceptional scenarios. A polished default state does not establish that the complete
experience is usable.

### 2.5 Define outcomes before implementation

For each important workflow, identify:

- The user’s goal and the expected successful outcome.
- The necessary actions, decisions, permissions, and prerequisites.
- The information required to make those decisions.
- The likely errors, interruptions, and recovery paths.
- The risks of delay, misunderstanding, duplication, or lost work.
- The evidence needed to determine whether the workflow works.

Define success in terms of correct task completion, understanding, effort, error rate, recovery,
accessibility, and appropriate user control. Time, activity, retention, and engagement can be useful
diagnostic measures, but none independently proves that a user experience is better.

### 2.6 Commit to a deliberate visual direction

Apply this process when no established design language exists, when a brief leaves visual choices open, or
when a redesign is explicitly authorized to change visual identity. An existing design system, brand
guideline, or explicit brief takes precedence over it; follow stated direction exactly, including when it asks
for a familiar look.

1. **State the design read.** In one sentence, name the subject, audience, primary job, and intended
   character, such as "an internal scheduling tool for dispatch staff under time pressure, calm and dense." If
   the subject or audience is unknown and the choice would materially change the result, ask one focused
   question instead of guessing.
2. **Draft a compact direction before building.** Describe color roles with named values, typeface roles,
   a layout concept with its alignment and density, a motion stance, and the one element meant to be
   memorable. Draw the direction from the subject's world: its materials, vocabulary, artifacts, and
   conventions.
3. **Test the draft against the default.** For each axis, ask whether the same choice would appear for any
   similar product. Where it would and the brief does not require it, revise that axis and record what changed
   and why. A familiar choice is acceptable when it is selected for this task rather than by inertia.
4. **Build, then critique the rendered result.** Review the actual interface, using screenshots where
   available. Check where attention lands first, whether structure encodes real relationships, and whether
   each decorative element serves the direction. Remove decoration that does not.

Spend expressiveness deliberately. One distinctive element supported by disciplined surroundings usually
communicates identity better than effects distributed everywhere. Repeated and consequential controls keep
stable, recognizable behavior regardless of the direction.

Treat the following as defaults to examine, not prohibited patterns. Each can be appropriate when chosen for a
reason:

- The same rounded card, radius, and shadow applied to every grouping regardless of hierarchy.
- Gradients, glows, blurs, or textures used as filler rather than meaning.
- An identical section rhythm, such as a centered hero followed by equal three-column feature cards.
- A small uppercase label above every heading, or a single accented word in each headline.
- Entrance animation on every section and hover motion on every surface.
- Framework or system default typefaces, colors, and spacing kept without a decision.
- Numbered markers on content that is not a sequence (see 3.1).
- Generic placeholder names, round invented figures, and copy that could describe any product (see 2.4).

A distinctive direction does not relax accessibility, content accuracy, performance, or localization
requirements. Verify contrast, focus visibility, reflow, reduced motion, and script coverage for the chosen
direction as for any other.

## 3. Establish visual hierarchy and a coherent design system

### 3.1 Prioritize information and actions

Make the most useful next action and the relationships between information clear through position, size,
weight, spacing, contrast, and grouping.

Establish priority within each task context. A screen can contain several independent tasks, each with a
legitimate primary action. Do not force every screen into a single-button hierarchy when that misrepresents
the work.

Group related content and separate unrelated tasks. Use cards when content forms a meaningful, independent
unit. Prefer whitespace, headings, lists, or dividers when those structures communicate the relationship more
clearly.

Numbering implies a real sequence, rank, or ordered relationship. Do not use numbering merely as decoration.

Borders, shadows, elevation, gradients, textures, animation, and illustrations MUST support information
hierarchy, interaction, or an intentional identity. Do not add visual effects simply to fill empty space or
make an interface appear more elaborate.

### 3.2 Define and maintain reusable visual rules

Establish a compact design system covering the visual properties and interaction patterns that recur across
the product. Depending on the product, this can include:

- Typography roles and text behavior.
- Spacing and layout conventions.
- Control dimensions and interaction states.
- Radii, borders, elevation, and layering.
- Semantic color roles and contrast requirements.
- Iconography and asset treatment.
- Motion and transition behavior.
- Responsive layout rules.
- Focus, validation, loading, success, and error states.
- Theme behavior and relevant platform variations.

Document the purpose of reusable rules, their appropriate contexts, their states, and justified exceptions.

Consistency means predictable relationships and behavior, not identical styling for every element. A table,
form, reading view, dashboard, and marketing page can appropriately use different density and composition
within the same coherent system.

Prefer extending an established pattern when it meets the requirement. Avoid accumulating page-specific
overrides, duplicate components, or speculative abstractions before repeated needs are established.

Before adding or replacing a component system, typeface, icon set, or motion dependency, inspect existing
capabilities and verify availability, compatibility, licensing, and relevant performance or maintenance costs.
Adopting a library does not itself establish accessible behavior or a coherent design.

### 3.3 Choose typography for the audience and language

Select typefaces and text styles for identity, readability, supported languages, and the environments in which
the product is used.

Define distinct roles for page titles, section headings, body text, labels, controls, captions, metadata, and
other recurring text. Distinguish roles through a deliberate combination of size, weight, line height,
spacing, and context rather than size alone.

Inspect actual glyphs, weights, punctuation, emphasis, numerals, descenders, and line wrapping. Verify font
coverage for all supported scripts and languages. A successful Latin-script sample does not establish correct
rendering for Arabic, Persian, or other non-Latin scripts.

Check optical alignment, diacritics, italic descenders, line boxes, fallback fonts, and clipping in the
rendered interface. Prefer text that can grow over tightly fixed geometry. Aligned or tabular numerals can
help comparisons when the language and typeface support them; they are not required for all numeric content. A
coherent hierarchy may use one type family or several with deliberate roles.

Use a comfortable reading measure for long-form content, and allow working canvases, code, and data tables to
use widths appropriate to their task.

Do not apply tracking, forced capitalization, text transformations, or fixed line heights that damage
legibility or script shaping. Text containers MUST accommodate realistic content without unintended clipping
or overlap.

Use real text when the intended presentation can be achieved with text. Images of text need the applicable
customizability or essential-presentation exception; a logotype can have a legitimate essential visual form.
A screenshot may depict text as part of an interface, but it is not a blanket exception for rasterizing
ordinary headings, instructions, or body content. Preserve the appropriate text alternatives.

### 3.4 Use semantic color and verify rendered states

Define color by role, such as surface, primary content, secondary content, action, boundary, focus, selection,
success, warning, and error.

Keep action fills and text colors conceptually separate. A color suitable for a large button background may
not provide adequate contrast when used for small text.

Evaluate actual foreground and background pairs, including transparency, overlays, gradients, nested surfaces,
disabled states, and layered components.

Test every supported theme independently. Verify initial rendering, persistence, autofill, selection, hover,
focus, active, validation, loading, and error states wherever applicable.

Do not rely on color alone to communicate status, selection, errors, or meaning. Add appropriate text,
iconography, shape, or other perceptible cues.

Choose initial theme, user preference persistence, and first-paint behavior deliberately. Theme changes MUST
NOT make content unreadable or silently reset unrelated preferences.

Where web themes are supported, keep browser-rendered controls, scrollbars, autofill, and other native
surfaces compatible with the selected theme. Verify the applicable `color-scheme` behavior in supported
browsers rather than assuming custom component colors also style browser-owned surfaces.

### 3.5 Use recognizable, consistent assets and icons

Use icons that are recognizable, consistently weighted, and stable in meaning across the product. A repeated
action should not change its icon arbitrarily between screens.

Preserve legitimate asset proportions and use assets appropriate to the task, context, and licensing
constraints.

Choose imagery for an informational or expressive purpose. A text-led page can be appropriate; there is no
image quota. Photographs, illustrations, generated assets, real screenshots, and component previews serve
different purposes and MUST NOT imply unverified people, products, capabilities, or endorsements. Preserve
required credits and usage rights.

Verify cropping, focal points, aspect ratios, resolution, and readable embedded information at the actual
rendered sizes. Define a usable missing-asset state. Prefer reusable, suitable iconography before creating
alternatives, while allowing justified custom vectors or identity assets. No file format or component library
automatically supplies accessible semantics.

Distinguish user-authored emoji from structural interface icons. Emoji may communicate a user's own expression
or content, but MUST NOT be the only indicator for a critical control, required status, or safety-related
meaning.

Decorative assets MUST NOT obscure information, reduce essential contrast, or become necessary to complete a
task.

### 3.6 Keep style ownership and layering predictable

Give shared styles and components clear ownership. Establish a deliberate cascade for base styles, components,
utilities, and contextual overrides. Keep selector specificity understandable and avoid escalating selectors
or routine `!important` fixes. Inspect computed styles in combined real states, including nested components,
rather than relying only on isolated examples.

Define layer roles for ordinary content, sticky navigation, menus, dialogs, and other overlays. Account for
stacking contexts created by transforms, opacity, isolation, and containment. A larger stacking number cannot
escape ancestor clipping or repair incorrect geometry. Verify top-layer controls, portals, focus, and pointer
behavior together.

Decorative overlays and pseudo-elements MUST NOT intercept intended input or hide focus. Coordinate animation
and style systems so competing mechanisms do not repeatedly overwrite the same property or own the same
lifecycle.

### 3.7 Provide resilient visual fallbacks

Essential content and task outcomes MUST NOT depend on an optional reveal effect, decorative asset, or
animation callback. Provide usable fallbacks when an enhancement is unsupported, interrupted, unavailable, or
fails to load. Define behavior for missing critical resources according to the product's actual support
requirements; this does not require every application to work without JavaScript.

Transparent or blurred surfaces need legible rendering over their actual backdrops and a suitable solid
fallback. Honor reduced-transparency preferences where supported, while retaining a usable baseline where
preference detection is unavailable. Effects must not be the only source of hierarchy or meaning.

## 4. Write clear, consistent interface content

### 4.1 Name actions by their outcomes

Use specific action labels that make the resulting operation clear, such as “Save changes,” “Download report,”
or “Remove member.”

Use consistent terminology for the same concept across navigation, forms, help, notifications, and
confirmation dialogs. Avoid changing labels for stylistic variety when users need to recognize a repeated
action.

Use familiar language for the intended audience. Expose implementation terminology only when it helps users
make an informed decision.

### 4.2 Preserve essential context

Keep copy concise without removing context necessary for understanding, consent, safety, or successful task
completion.

Essential instructions MUST remain available when needed. Do not rely exclusively on placeholders, hover
tooltips, clipped labels, or transient notifications to communicate information required for a task.

Write empty states that explain what is happening and offer a relevant available action when one exists.
Distinguish a genuinely empty collection from a failed request, a permission restriction, or a search with no
matching results.

Error messages SHOULD identify the problem, explain its consequence when necessary, and state the next useful
step without blame. Avoid vague messages such as “Something went wrong” when more precise, truthful
information is available.

Do not make a recovery promise unless the system can actually deliver it.

### 4.3 Adapt writing to the context

Use capitalization, punctuation, tone, grammatical forms, pluralization, and date conventions appropriate to
the language and audience.

Use a conversational tone when it aids understanding. Avoid humor, personality, or marketing language where
precise account, financial, legal, security, safety, or other consequential information is needed.

Do not use text as decorative filler or fabricate urgency, popularity, scarcity, or social proof.

### 4.4 Make dynamic and asynchronous content understandable

When content changes after an action, make the result understandable without requiring users to infer what
happened from a visual movement alone.

When data is delayed, stale, incomplete, or approximate, communicate its relevant status and limitations. Do
not present stale, unverified, predicted, or illustrative content as confirmed current information. Cached
content can be current and authoritative; communicate its freshness when that matters to the task.

## 5. Design responsive, adaptable layouts

### 5.1 Design for content constraints, not device labels

Choose breakpoints where content or interaction needs change, rather than relying solely on device categories
or framework defaults.

Use fluid layouts and progressive disclosure where they help users complete the same essential tasks in
constrained space. Do not remove necessary capabilities from smaller screens simply to make a layout fit.

Allow headings, labels, controls, values, and action groups to wrap or grow with content. Give grid and flex
children enough room to shrink, and handle long unbroken values deliberately.

Use truncation only when appropriate. When identification or decision-making depends on the complete value,
provide a clear way to access it.

Do not solve local sizing defects by globally clipping document overflow or disabling normal scrolling.

For native applications, support the platform's semantic controls, user text scaling, navigation and Back
behavior, safe areas, and relevant system gestures. Use platform-specific units and conventions rather than
copying web measurements mechanically. Haptic feedback, when appropriate and enabled, supplements perceptible
feedback; it must not be the sole way to recognize a result.

### 5.2 Manage scrolling and fixed elements deliberately

Keep ordinary page content within the usable viewport. Genuinely two-dimensional tables, boards, canvases, and
visualizations MAY scroll inside bounded regions when doing so supports their task.

Make necessary scrolling discoverable and usable with keyboard and touch. Nested scrolling MUST have a clear
purpose and MUST NOT make content inaccessible or difficult to navigate.

Fixed and sticky elements MUST account for safe areas, changing viewport height, browser chrome, enlarged
text, and on-screen keyboards.

Choose minimum heights and viewport units according to these conditions and content growth. Do not force a
full-height hero or working surface when it clips content or obstructs a short viewport.

Reserve sufficient space so navigation, banners, feedback widgets, floating controls, and sticky actions do
not obscure essential content or keyboard focus. Increasing stacking order alone does not resolve a layout
collision.

Preserve normal browser navigation, scrolling, zoom, and gesture behavior unless an interaction has a clearly
justified reason to alter it.

### 5.3 Test reflow, zoom, and varied viewport conditions

Verify layouts at narrow and wide widths, short landscape heights, text enlargement, and browser zoom levels.

Where the web criteria apply, text MUST resize to 200% without loss of content or functionality, subject to
the defined exceptions for captions and images of text. Ordinary vertically scrolling content MUST reflow
without two-dimensional scrolling at a width equivalent to 320 CSS pixels. For content designed to scroll
horizontally, the corresponding height is 256 CSS pixels. A familiar 400% desktop-zoom check produces 320 CSS
pixels from an initial 1280-pixel-wide viewport; the percentage alone does not establish the test condition.

Apply two-dimensional-layout exceptions to the parts that actually require them, not automatically to an
entire page or every cell within a table. Do not restrict an experience to one orientation unless that
orientation is essential.

In applicable markup and writing systems, content MUST remain functional without lost information when users
simultaneously override line height to 1.5 times the font size, paragraph spacing to 2 times the font size,
letter spacing to 0.12 times the font size, and word spacing to 0.16 times the font size. These are supported
user adjustments, not mandatory authored typography. Apply the properties used by the relevant script rather
than imposing tracking that damages connected writing.

Check that controls remain operable, content remains understandable, action labels remain identifiable, and
necessary information is not hidden when the viewport or text size changes.

Document any genuinely task-essential two-dimensional interactions and verify their bounded scrolling,
keyboard access, and alternatives.

## 6. Treat accessibility as a core quality requirement

Use WCAG 2.2 Level AA as the baseline target for web experiences. This target is a practical baseline, not an
exhaustive specification of accessibility obligations, a guarantee of usability, or proof of legal
conformance.

Consider accessibility from discovery and information architecture through content, implementation,
validation, and maintenance. Do not defer it to a final visual review.

For native and other non-web software, use the platform's accessibility APIs, conventions, and assistive
technologies together with the applicable WCAG-derived criteria. Do not assume that web-specific techniques or
measurements transfer unchanged.

### 6.1 Use semantic structure and predictable focus

Prefer native semantic elements: links navigate, buttons perform actions, and tables express tabular
relationships.

Provide meaningful page titles, hierarchical headings, landmarks, and a way to bypass repeated navigation
where appropriate. Visual styling MUST NOT determine heading levels.

Maintain logical reading order and focus order. Identify the current destination visually and semantically,
distinguishing an exact current page from a parent section.

Every interactive control MUST have an understandable accessible name, appropriate role, and accurate state.
Informative images MUST have meaningful text alternatives. Decorative images and icons SHOULD be hidden from
assistive technology when their content is redundant or irrelevant.

When a control has a visible text label, its accessible name MUST contain that label. Prefer matching wording,
with necessary distinguishing context afterward. A separate accessible label must not replace visible wording
in a way that breaks speech activation. Icon-only controls need an accessible name; an explicit ARIA label is
one technique, not a requirement to add redundant attributes to every icon.

Media MUST meet the applicable requirements for alternatives, captions, audio description, and accessible
controls. A transcript is not universally interchangeable with synchronized captions or audio description.
Existing narration may already convey the necessary visual information; determine what the actual content
requires rather than classifying inconvenient content as unimportant.

### 6.2 Support keyboard operation and focus visibility

Functionality MUST be keyboard operable except where the underlying function genuinely depends on the path of
movement rather than only its endpoints. Freehand drawing can qualify; ordinary selecting, moving, sorting,
and resizing do not become exempt because they were implemented as pointer-only controls. The exception does
not exempt unrelated controls in the same interface.

Preserve native keyboard behavior before adding custom handlers. Keep application shortcuts scoped and avoid
overriding browser or assistive-technology commands. Single-character shortcuts need an appropriate disable,
remap, or focus-only mechanism so they do not activate while users type.

Keyboard focus MUST remain visible and predictable. Interfaces MUST NOT introduce keyboard traps or remove
native focus indicators without a suitable replacement.

Use initial autofocus deliberately. Check for unexpected scroll movement, interrupted reading, and an
unrequested on-screen keyboard, especially on small screens. A justified task-entry focus is different from
repeatedly taking focus back from a person already interacting with the page.

Author-created content MUST NOT entirely obscure a focused component under the applicable WCAG 2.2 AA
criterion. Keeping the entire control and focus indicator visible is a stronger practical goal.

Composite controls MUST implement their complete semantic and keyboard behavior. Adding ARIA roles alone does
not implement arrow-key navigation, selection, dismissal, focus management, or other required interaction
behavior.

### 6.3 Implement modal and overlay behavior correctly

Use a page-level or inline interaction instead of a modal when a modal would introduce unnecessary
interruption.

When a modal dialog is necessary, it MUST have an accessible title, an appropriate initial focus destination,
a clear closing path, suitable keyboard focus containment, appropriate background interaction restrictions,
and focus restoration after dismissal.

The background of a modal MUST genuinely be inactive while it is open; a visual scrim or an ARIA attribute
alone does not enforce that behavior. For dismissible menus and overlays, support the expected dismissal and
cancellation interaction. Restore focus to the trigger or another meaningful control when the current context
remains; successful navigation into a new context may need focus there instead. When the focused item is
deleted, filtered out, or collapsed, deliberately choose the next meaningful focus destination.

Avoid stacked modals unless there is a compelling, validated requirement. Ensure popovers, menus, tooltips,
and other overlays are usable with the relevant pointer, keyboard, and assistive technology interactions.

### 6.4 Meet contrast, target-size, and non-color requirements

At minimum, apply WCAG 2.2 AA contrast requirements accurately:

- Normal text generally requires a contrast ratio of at least 4.5:1 against its background.
- Large text generally requires at least 3:1. Large text is at least 18 points regular or 14 points bold,
  approximately 24 or 18.67 CSS pixels, or an equivalent size for the relevant font and writing system.
- Required non-text visual information generally requires at least 3:1 contrast against adjacent colors under
  the applicable criterion.

Evaluate relevant exceptions correctly rather than treating every visual element or inactive state
identically.

Do not round a failing contrast ratio up to the threshold. Supporting text, placeholders, and tooltip text
still need their applicable text contrast; ordinary brand-colored text is not exempt merely because it uses a
brand color. Decorative dividers do not automatically have the same requirements as essential control
boundaries.

The WCAG 2.2 AA minimum pointer-target criterion is generally 24 by 24 CSS pixels, subject to its defined
spacing, equivalent-control, inline, user-agent, and essential exceptions. Approximately 44 by 44 CSS pixels
is a useful ergonomic target for frequently touched controls, but it is not the AA minimum itself.

Evaluate the interactive hit area, not only the visible glyph. The spacing exception uses
24-CSS-pixel-diameter circles centered on undersized target bounding boxes. Each such circle must not
intersect another target or the corresponding circle of another undersized target. This is not a universal
fixed gap between controls.

Platform-specific point and density-independent-pixel recommendations are not interchangeable with CSS-pixel
measurements. Assess the actual environment and applicable criterion.

Links MUST be distinguishable within their context and MUST NOT rely on color alone when the applicable
requirement calls for an additional visual indicator. Status, errors, required fields, and selection MUST have
appropriate non-color cues.

### 6.5 Make help and feedback accessible

For content triggered by hover or focus, meet the applicable dismissible, hoverable, and persistent
conditions. Users must be able to dismiss it without moving the pointer or focus when required, move the
pointer over it when applicable, and read it until hover or focus is removed, it is dismissed, or its
information becomes invalid. Essential instructions cannot depend on a tooltip. Content containing interactive
controls usually needs a suitable popover or dialog pattern rather than tooltip semantics.

Announce meaningful asynchronous status changes without needlessly moving focus. Use suitable live-region
behavior for ordinary updates, validation results, and operation outcomes according to their importance.

Actual assistive-technology behavior MUST be tested directly for important workflows. Passing automated
accessibility checks does not prove complete accessibility or usability.

When repeated help mechanisms are provided across related pages, keep their relative order consistent unless
the user initiates a change. This does not require adding a help feature or fixing it to identical screen
coordinates at every breakpoint.

### 6.6 Support sensory, timing, and user-environment needs

Instructions MUST NOT rely only on color, shape, sound, orientation, or screen position. Identify the relevant
control or information in a way users can perceive and act on.

For content-controlled time limits, provide the required ability to turn off, adjust, or extend the limit, or
establish the applicable exception. If warning and extension are the chosen mechanism, give at least 20
seconds to request an extension through a simple action and permit extension at least ten times. This is one
permitted mechanism, not a minimum duration for every session or permission to extend an immutable external
deadline. Explain relevant expiry and recovery behavior without treating every timeout as proof that work
failed.

Avoid unnecessary autoplay sound. Automatically playing audio lasting more than three seconds needs an
appropriate pause or stop mechanism, or volume control independent of overall system volume. Test
forced-colors or high-contrast modes where supported; required boundaries, selection, and focus must survive
the loss of decorative backgrounds or shadows.

## 7. Design forms and input flows as complete interactions

### 7.1 Label and group fields clearly

Give form controls persistent, understandable labels and associate relevant hints, instructions, and errors
programmatically.

Use appropriate fieldsets and legends to group related checkboxes, radio buttons, or other related options.
Ensure that activating a checkbox or radio label activates its associated control.

Floating labels MAY be used when labels remain visible, readable, and unambiguous. Placeholders MUST remain
supplementary rather than becoming the sole label or source of essential instructions.

Explain required fields, constraints, and formats where useful, especially when an invalid submission would be
costly or difficult to recover from.

### 7.2 Configure inputs for the actual data

Choose input types, input modes, autocomplete values, spelling behavior, and text direction based on the
information being entered.

A numeric identifier is not necessarily a numeric quantity. Do not expose inappropriate numeric steppers or
apply numeric validation to identifiers that can legitimately contain leading zeros, letters, or punctuation.

Support paste, autofill, password managers, and other expected browser and platform assistance. Do not impose
unnecessary restrictions on text entry or prevent users from entering a valid value character by character.

Preserve input-method-editor composition and valid intermediate values. Do not submit on a composition Enter
key or rewrite partially composed text. Distinguish stored and editable values from display formatting. Where
length limits exist, explain the relevant constraint and avoid splitting visible characters unexpectedly.
Credentials MUST NOT be silently truncated or transformed to make them fit.

Authentication MUST meet the applicable accessible-authentication requirement across the complete supported
process, including relevant multifactor and recovery steps. A cognitive-function test needs a permitted
alternative, assistance mechanism, or defined exception. Password-manager, autofill, paste, and full-code
entry support can provide necessary assistance; a separate authentication method is not always required. Do
not force unsupported manual transcription or memorized partial passwords. A permitted exception does not by
itself establish practical usability.

When password-reveal controls are provided, make them keyboard operable and expose their state. Do not make a
focus change or a value edit unexpectedly submit a form, navigate, or otherwise change context without
appropriate advance explanation.

### 7.3 Validate at an appropriate time

Usually introduce validation errors after a field loses focus or after submission, then reflect corrections
promptly.

Choose timing for the field and task. An untouched field need not become invalid merely because focus moves to
another prerequisite. Clear stale errors for the field being corrected without hiding unrelated failures, and
reset interaction state appropriately when entering a new step.

Avoid rejecting valid intermediate input, repeatedly interrupting users while they type, or disabling
submission merely because an untouched form is incomplete. Genuine prerequisites MAY justify a disabled
control when the reason is visible and understandable.

Place specific errors near the relevant fields and associate them programmatically. For long forms, provide a
suitable error summary linked to the affected fields.

After a submission is rejected for invalid input, deliberately focus the first invalid field or the error
summary, depending on the form's length and structure. Preserve understandable focus behavior as validation
messages update.

This focus rule concerns invalid input. For a service or form-level failure, preserve or move focus to
meaningful feedback as appropriate; there may be no invalid field. Ordinary step advancement MUST NOT override
the chosen failure focus. Move focus into the next step only after a successful transition, and do not steal
focus on routine successful saves.

Give actionable field-constraint errors without exposing protected identity information. A general credential
rejection may need to avoid revealing which identity or secret matched. Specificity must remain compatible
with confidentiality.

Distinguish user-input validation failures from service, network, authentication, and authorization failures.
Retain entered information whenever its sensitivity and security requirements permit.

### 7.4 Define submission and saving states

#### Prevent consequential submission errors

For applicable web workflows involving legal commitments, financial transactions, modifications or deletion
of user-controllable stored data, or submission of user test responses, at least one appropriate
error-prevention mechanism MUST apply: reversibility; checking entered information for input errors with an
opportunity to correct them; or a mechanism to review, confirm, and correct information before final
submission. Apply the corresponding WCAG 2.2 Level AA requirements and their defined scope and exceptions.

The chosen safeguard MUST make the relevant information and consequences understandable, remain accessible,
and reflect the operation the system actually performs. Do not treat a generic confirmation dialog as
sufficient when it fails to expose the information needed to detect a consequential error. When relying on
reversibility, make the actual recovery mechanism and any relevant limits clear.

This does not mandate an extra dialog for every save or routine edit. A preventive review or correction
opportunity and feedback about a completed operation have different purposes; success feedback does not
replace error prevention. Test the selected safeguard against the actual consequential error it is intended
to prevent.

#### Represent submission outcomes accurately

Submission flows MUST distinguish the relevant states, including:

- Ready for input.
- Invalid input.
- Submission pending.
- Successful completion.
- Recoverable failure.
- Unrecoverable or permission-related failure, when applicable.
- A prolonged wait or timeout that needs an explanation or recovery option.

Show pending submission feedback, prevent accidental duplicate operations where appropriate, and define
timeout, success, failure, and retry behavior.

Do not represent an operation as successful until the relevant success condition is confirmed. A click,
animation, or optimistic interface update does not independently prove that the underlying operation
persisted.

Preserve readable labels and control geometry during loading. Distinguish readonly, disabled, and pending
states according to their actual behavior.

If users can edit fields while a save is in progress, acknowledge only the submitted snapshot as saved. Newer
edits MUST remain unsaved unless they have also been persisted successfully. An earlier response MUST NOT
erase or incorrectly mark later edits as saved.

Alternatively, suspend conflicting editing for the duration of the operation when that behavior is appropriate
and clearly communicated.

### 7.5 Handle multistep flows and unsaved work

For multistep forms, show meaningful progress when the sequence is substantial, preserve permitted values when
navigating backward, and make requirements before final submission clear.

Within the same process, information already supplied MUST be populated or readily available to select when it
is needed again, except where re-entry is essential, necessary for security, or the information is no longer
valid. Browser autocomplete alone does not establish this behavior. This requirement does not authorize
retaining sensitive information across sessions.

Choose unsaved-work warnings, autosave, and draft retention according to the value, sensitivity, and expected
lifespan of the work. Do not warn on every navigation or persist sensitive information by default.

Define behavior for dismissal, refresh, logout, session expiration, device interruption, and recovery from a
failed save.

Resolve a user-initiated leave decision before carrying out an irreversible navigation or logout side effect.
Clear a guard only for work that is actually saved or deliberately discarded. Security-driven session
revocation can take precedence over draft preservation; communicate the actual result and retain only what is
permitted.

Autosave MUST distinguish pending, saved, failed, and recovered states truthfully. Provide an understandable
path to retry or recover where the system supports it.

Do not promise recovery after dismissal, loss of connectivity, expiration, or data deletion unless the
underlying system can deliver it.

## 8. Keep navigation and feedback predictable

### 8.1 Structure navigation around information and tasks

Organize navigation around the information hierarchy and the tasks users need to complete.

Sidebars, tabs, breadcrumbs, menus, and mobile navigation are options, not mandatory patterns. Use patterns
appropriate to the structure, depth, and frequency of the destinations.

Avoid competing controls for the same information level and keep essential destinations discoverable.

Provide meaningful page titles and appropriate focus movement or announcements after navigation. Distinguish
an exact current destination from a parent section that merely contains it.

### 8.2 Preserve URLs and browser behavior

Use meaningful URLs for destinations and, where appropriate, useful shareable state such as filters,
pagination, or selected non-sensitive views.

Keep sensitive input, credentials, private information, and unnecessary transient interaction state out of
URLs.

Support direct loading and refresh of valid destinations. Preserve native link behavior, including opening
links in another tab or window and navigating through browser history.

Back and Forward navigation SHOULD restore useful context, such as relevant position and filters, without
fighting deliberate user scrolling or recreating stale state incorrectly.

Distinguish a deterministic action such as “Back to search results” from browser-history navigation when the
two behaviors have different outcomes.

### 8.3 Place feedback near its owning operation

Provide feedback in a location and form that makes its subject clear.

Toasts can communicate brief, non-critical updates. Persistent errors, consequential warnings, and important
undo opportunities need sufficiently durable access. Their duration and prominence MUST reflect the importance
of the information and the risk of missing it.

Avoid competing duplicate notices and repeated announcements at parent and child levels. A linked error
summary and field-level messages serve complementary purposes and may intentionally describe the same
problems. Explain unavailable actions when useful instead of relying on grey styling alone.

Ensure that important feedback is available to assistive technology and does not obstruct controls, focus, or
other essential content.

### 8.4 Handle destructive and bulk actions carefully

Protect consequential destructive operations with proportionate confirmation, reliable undo, or another
appropriate safeguard.

For operations within the consequential-submission scope, the safeguard MUST satisfy at least one of its
required error-prevention mechanisms. Proportionality does not permit an arbitrary substitute that leaves
the applicable requirement unmet.

State the object, scope, and consequence of an action clearly. Do not promise recovery or undo unless the
system can actually provide it.

Distinguish removing a shortcut, view, association, or membership from deleting the underlying resource.
Labels and confirmation copy MUST describe the actual scope, including retained data and delayed deletion
where relevant.

For bulk operations, distinguish selected rows, the current page, and all matching results. Clarify whether
the operation applies to a selection or an entire collection.

When an operation partially succeeds, identify the successful and failed items or groups, preserve their
results, and offer appropriate recovery without implying that the entire operation succeeded.

Do not add confirmation dialogs to every action indiscriminately. Safeguards should be proportionate to the
consequences and likelihood of mistakes.

## 9. Represent application state and reliability truthfully

### 9.1 Distinguish loading, empty, unavailable, and failed states

Design distinct behavior for each applicable state:

- Initial loading.
- Refresh or revalidation.
- Confirmed content.
- Confirmed empty content.
- No matching search results.
- Insufficient permissions.
- Expired authentication.
- Network failure.
- Service failure.
- Partial results.
- Stale data.
- Cancelled or interrupted operations.

A failed read is not evidence that a collection is empty. Model missing records, restricted access, and
service failures accurately, but use the same generic unavailable or not-found presentation when revealing
existence would disclose protected information. Internal distinctions do not require disclosing them to the
user. A search with no matches is not the same as a collection containing no records.

Previously confirmed content MAY remain visible during refresh when its stale or pending status is clear and
displaying it remains appropriate for the task and risk.

When a state changes, communicate the change in a way that supports the user's next decision.

Use determinate progress only when the amount of work and its completion can be measured meaningfully. Do not
invent percentages. Distinguish dismissing a progress display from cancelling the underlying operation, and
show a useful next step for supported no-results recovery.

### 9.2 Prevent stale responses and incorrect state updates

Prevent obsolete requests from replacing newer searches, filters, navigation contexts, or edits.

Associate asynchronous responses with the request or data version they belong to. Apply results only when they
remain relevant to the current state.

Guard conflicting operations while required data or revisions are unresolved without indiscriminately
disabling unrelated work. Preserve the last confirmed order or result where it remains valid, and reconcile
uncertain or conflicting outcomes with authoritative state. Make proposed, pending, or stale state explicit
rather than restoring a result that concurrent work has already superseded.

Separate read failures from write failures. A failed refresh does not necessarily invalidate previously
confirmed data, and a failed write does not necessarily mean the existing data has changed.

Retry behavior MUST be appropriate to the operation. Retrying a read is often different from retrying a
payment, purchase, message, invitation, or other action that may create duplicate effects.

Where the result of an operation is uncertain, communicate that uncertainty and use safe recovery mechanisms
rather than blindly repeating a potentially consequential action.

### 9.3 Use optimistic updates responsibly

Optimistic updates MAY improve responsiveness when the expected behavior and recovery strategy are well
defined.

They MUST reconcile with the authoritative result or roll back when necessary. They MUST NOT falsely claim
confirmed persistence.

When a change fails, restore a truthful state, explain the failure when appropriate, preserve the user's
intended work where possible, and provide an actionable recovery path.

Avoid visual updates that can appear successful while leaving the actual underlying data inconsistent.

### 9.4 Handle disconnection, concurrency, and stale revisions

Define disconnection and timeout behavior for operations that depend on remote services.

Do not imply offline editing, automatic synchronization, or background completion unless those capabilities
exist and behave as described.

Preserve appropriate work after reauthentication. Explain relevant conflicts, stale revisions, or simultaneous
changes when users need to resolve them.

When concurrent edits are possible, define the actual conflict strategy. Depending on the task, this may
involve reloading, comparing revisions, merging permitted changes, choosing between versions, or preserving a
copy.

Do not silently overwrite newer work or imply that unsynchronized data has been safely saved.

### 9.5 Make account, workspace, and permission scope visible

Show the active account, workspace, organization, or other relevant context before consequential operations.

Private, shared, organizational, and public scopes MUST be understandable and must match permissions actually
enforced by the system.

Make the distinction between viewing, editing, sharing, publishing, exporting, deleting, and administering
clear when those actions have different consequences.

The interface MUST NOT imply that a user has permission, that an item is private, or that an action has
succeeded when the underlying system does not support that claim.

### 9.6 Respect attention, autonomy, and the meaning of progress

When onboarding is needed, introduce it progressively and allow unrelated setup to be skipped where possible.
Do not block first value behind information or configuration the current task does not require.

Match notification prominence to importance. Provide suitable control over nonessential interruptions and
avoid treating every event as an urgent message. Optional characters and incidental effects must not cover
work or demand interaction before the task can continue; provide suitable ways to reduce or disable them.

Rewards, streaks, activity counts, and progress systems MUST NOT fabricate completion, shame people, or
present activity as a definitive measure of personal worth or work quality. Define relevant day boundaries,
time off, and timezone behavior before presenting a streak as authoritative.

Declining, cancelling, unsubscribing, or withdrawing consent SHOULD be no harder than the corresponding
acceptance or sign-up, apart from proportionate safeguards for consequential operations. Do not steer choices
through guilt-inducing wording, visually suppressed alternatives, preselected optional purchases, or costs
revealed only at the final step.

When assistants are present, distinguish suggestions, drafts, actions awaiting authorization, work in
progress, and confirmed completion. Make scope and consequential effects understandable. A generated
recommendation or a request sent to a service MUST NOT be presented as an executed or successful action.

## 10. Design privacy and security into the experience

Design security-related behavior so that people can understand the relevant risk, make informed choices, and
recover appropriately without unnecessary exposure of sensitive information.

These principles apply to capabilities and risks that exist in the product. They do not independently
authorize new security features or additional data collection.

### 10.1 Make data use and disclosure understandable

Request only the information needed for a defined purpose, subject to the product's requirements and
applicable obligations.

Explain consequential data collection, access, retention, sharing, and disclosure when users need that
information to make an informed decision.

Do not use interface wording that obscures who can access information, where it may be shared, or what happens
after a user takes an action.

Do not imply that a system-selected default represents informed user consent, or present a control as offering
a choice it cannot change. An editable default can still be a genuine choice. A control MUST NOT claim to
revoke access or delete information unless the underlying system performs the stated action.

### 10.2 Protect sensitive information in the interface

Avoid unnecessarily exposing credentials, personal data, financial details, confidential records, recovery
codes, or other sensitive information in visible content, notifications, URLs, browser history, logs exposed
to users, or shared screens.

Use masking, reveal controls, session safeguards, or confirmation steps when they materially reduce a relevant
risk without obstructing legitimate use.

If revealing or copying sensitive information is necessary, make the action understandable and ensure it does
not inadvertently disclose unrelated information.

Do not retain secrets or sensitive form values in drafts, local persistence, analytics, or error reports by
default. Any necessary retention MUST follow the product's security requirements and clearly defined
data-handling rules.

Render untrusted text and addresses as untrusted content rather than granting them trusted markup or
navigation behavior. Explain meaningful destination or context changes where needed. Redact sensitive
information from demonstrations, screenshots, shared reports, and support evidence.

### 10.3 Make authorization and sensitive actions explicit

Ensure that the interface reflects permissions enforced by the underlying system. Hiding a control is not an
authorization mechanism.

Explain denied or expired access and provide a valid next step where one exists. Do not disclose confidential
information merely to explain why a user lacks permission.

For high-risk actions, provide proportionate safeguards, which may include confirming the target, explaining
consequences, requiring appropriate reauthentication, or supporting reliable recovery.

Use these safeguards according to actual risk. Avoid unnecessary authentication prompts and repeated
confirmation for low-risk actions.

### 10.4 Handle session and identity transitions carefully

Define behavior when a session expires, a user switches accounts, permissions change, or access is revoked.

Preserve permitted work across reauthentication when safe and appropriate. Do not expose the previous user's
private information after an account switch or imply that work was saved when the system cannot confirm it.

Communicate security-relevant changes without revealing sensitive details through inappropriate channels.

If a security incident, suspicious operation, or access change affects the user's next action, present
accurate information and the appropriate recovery path. Do not invent guarantees or claims about protection.

## 11. Localize language, direction, and regional behavior

### 11.1 Translate meaning, not just individual strings

Translate complete messages using language-appropriate grammar, pluralization, terminology, and tone.

Maintain a terminology glossary for recurring product concepts and actions. Keep labels, help content, errors,
notifications, and related documentation consistent.

Test text expansion, contraction, wrapping, punctuation, and layout with representative supported languages. A
successful sample in one language does not establish readiness for all supported languages.

Avoid building layouts around fixed English string lengths or concatenating fragments in ways that break
grammar or translation.

For web content, the page's language and meaningful changes in language MUST be identified where the criteria
apply; text direction alone does not establish language. Initial locale inference must not override a
deliberate user preference. Format numbers, currencies, units, and dates for the chosen locale while
identifying ambiguous currencies or units when decisions depend on them.

### 11.2 Support right-to-left and mixed-direction content

Use logical start/end and inline/block layout properties rather than hard-coded left/right assumptions
wherever appropriate.

Page-level right-to-left direction is not sufficient for mixed-direction content. Isolate names, URLs, email
addresses, identifiers, codes, and other directionally distinct values so they remain readable and correctly
ordered.

Multiline user-generated content may require paragraph-level direction detection.

Mirror directional icons, navigation indicators, and motion when their meaning requires it. Do not
automatically mirror logos, media controls, or nondirectional symbols.

Preserve punctuation, text shaping, numerical meaning, and selection behavior across supported writing
systems.

### 11.3 Separate language, calendar, timezone, and numeral conventions

Treat language, calendar system, timezone, numeral presentation, and date interpretation as distinct settings
and requirements.

Specify how the product represents date-only deadlines, exact timestamps, relative times, day boundaries, and
daylight-saving transitions when those values affect decisions.

A date-only value is a civil date, not an instant to shift silently through timezones. Identify the relevant
timezone for appointments and deadlines, and define how ambiguous or nonexistent local times are handled when
scheduling makes them relevant. Recurrence at a local clock time differs from a fixed elapsed interval. Date
controls need keyboard operation, understandable unavailable values, and an appropriate accessible input path.

Provide precise context when relative wording is insufficient. A deadline or event should not become ambiguous
because the user crosses a timezone or the display language changes.

Where appropriate, accept equivalent local digit forms and define search normalization deliberately. Preserve
original user-entered text and opaque values.

Do not normalize credentials or identifiers as a cosmetic localization fix. Language changes SHOULD preserve
the relevant destination and permitted work without silently resetting unrelated preferences.

## 12. Use motion and interactions responsibly

### 12.1 Make motion purposeful

Motion SHOULD communicate feedback, hierarchy, spatial relationships, continuity, or a meaningful change in
state.

Choose duration, easing, and movement according to the interaction rather than applying one timing value to
everything.

Keep transitions interruptible where appropriate and ensure tasks remain responsive. The final state MUST NOT
depend solely on the completion of an animation.

Prefer efficient animation properties such as opacity and transform when they are appropriate, and measure
alternatives when they may have a meaningful performance cost. Name transition properties explicitly instead
of applying a broad transition to every changing property. Immediate or static updates are valid; an
interaction does not require an animation simply because it can be animated.

### 12.2 Respect reduced motion and accessibility

Honor reduced-motion preferences while preserving the information or feedback that motion was intended to
communicate.

Avoid harmful flashing, disorienting movement, and unnecessary parallax. Provide pause, stop, or hide controls
for prolonged automatically moving content when required by the applicable accessibility criteria.

Moving content that starts automatically, lasts more than five seconds, and appears alongside other content
MUST provide pause, stop, or hide controls unless it is essential. Automatically updating information
presented alongside other content needs pause, stop, hide, or update-frequency control unless the updating is
essential; it does not have the same five-second condition. Reduced-motion support does not replace required
user controls. Stop automatic carousel advancement during relevant keyboard interaction and avoid unexpected
resumption. Apply the actual flashing thresholds rather than treating a frequency slogan as a complete safety
test.

Ensure that animation does not become the only way to understand a status, locate a control, or complete a
task.

Clean up animation-related work, listeners, and resources when components become inactive or are removed.

Cancel superseded animation work and establish the correct final state explicitly when an effect is
interrupted, disabled, or unsupported. Keep optional continuous motion from causing unnecessary application
rerenders or background work.

### 12.3 Provide alternatives to gesture-dependent interaction

Core operations MUST NOT depend solely on hover, swipe, dragging, or another gesture that excludes relevant
users or input methods.

Provide keyboard operation and an appropriate single-pointer alternative where required.

These are separate requirements: keyboard operation alone does not provide a non-dragging pointer alternative.
Reordering buttons, destination menus, or direct value entry can support both when correctly implemented.
Distinguish ordinary browser scrolling from an author-created dragging interaction.

Prefer native activation on pointer release so users can cancel before release. Pointer-down feedback can be
immediate without prematurely executing the action. Use the applicable cancellation, reversal, or
essential-function exception when an operation needs different activation timing.

For drag interactions, make the origin, destination, cancellation, and resulting save behavior clear. A
suitable alternative might be buttons, menus, direct selection, or another interaction appropriate to the
task.

Scope gesture suppression narrowly. Preserve ordinary browser scrolling, zooming, pointer behavior, and
assistive technology interactions elsewhere.

## 13. Design charts, tables, and data-intensive interfaces honestly

Apply this section when the product includes charts, analytical views, data tables, dashboards, or other
data-intensive interactions.

### 13.1 Match the visualization to the question

Every chart SHOULD answer a clear question that matters to the user.

Choose a chart type and visual encoding that communicate the underlying comparison, trend, distribution,
composition, or relationship without introducing avoidable ambiguity.

Represent units, scales, ranges, categories, and uncertainty accurately. Do not use misleading axis ranges,
decorative three-dimensional effects, or visual emphasis that distorts the significance of the data.

Length-encoded bars ordinarily need a zero baseline. Nonzero or logarithmic scales require deliberate, clear
communication; this does not mean every chart axis must start at zero. Expose relevant denominators, periods,
freshness, and material rounding. Sampling or aggregation must not conceal important outliers without
explanation.

Distinguish missing, unavailable, invalid, and zero values. Explain material aggregation, sampling,
estimation, or filtering where users need that context to interpret the result.

### 13.2 Make exact data and alternatives available

Do not make essential values available only through mouse hover or visual estimation.

Provide suitable textual, tabular, keyboard-accessible, or other nonvisual alternatives according to the
chart's purpose and complexity.

When a visualization depends on a selected period, filter, unit, or aggregation method, make the applicable
context understandable.

A chart's appearance MUST NOT imply greater precision or certainty than the underlying data supports.

Choose direct labels or legends according to the task. Interactive legends need suitable semantics and
keyboard behavior. A short image label is insufficient when the task depends on a complex comparison, but
forcing every plotted point into the Tab order is not a universal solution.

### 13.3 Design tables for real tasks

Use clear column and row relationships, appropriate headers, understandable labels, and useful alignment.

Where sorting exists, expose its state and communicate the resulting order. When tables are complex, provide
appropriate relationships between headers and data cells for assistive technology.

Support horizontal scrolling inside a bounded region when necessary for genuinely two-dimensional data.
Preserve access to meaningful row and column context.

Add filtering, export, pagination, or drill-down only when they support an established user task. More
controls do not automatically produce a better data interface.

Ensure that data-heavy interfaces remain usable at relevant viewport sizes and input methods.

Do not infer totals, completion, or progress from a preview, sample, loaded page, or partial response unless
the derivation is valid and its scope is clear. Keep useful row, column, and selection context when data is
refreshed, reordered, filtered, or paginated.

## 14. Maintain performance and responsive implementation

### 14.1 Protect perceived and actual performance

Treat performance as part of the user experience, especially for frequent, time-sensitive, low-bandwidth, and
high-impact tasks.

Reserve appropriate dimensions for images, embeds, media, and other content that could otherwise produce
layout shift.

Choose suitable formats, compression, responsive image sizes, and loading priorities. Lazy-load noncritical
offscreen media when appropriate, without delaying essential initial content.

Preserve required glyph coverage when optimizing fonts. Preload only resources that materially improve the
critical rendering path.

Keep text legible while fonts load or fail. Choose suitable fallback fonts and metrics to limit disruptive
changes in wrapping and layout, and verify the result with the actual supported scripts.

### 14.2 Keep interactions responsive

Typing MUST feel immediate. Debounce costly downstream work rather than delaying visible input or suppressing
normal text entry.

Measure actual rendering and data costs before adding complex optimization. Choose virtualization, pagination,
caching, and other strategies according to the task and observed constraints. Verify their effects on keyboard
operation, reading order, focus retention, freshness, search, and navigation. No fixed item count universally
determines when an optimization is necessary.

Avoid unnecessary synchronous layout measurement, repeated rendering work, excessive animation, and loading
large optional features before they are required.

Keep initial server-generated and client-rendered content consistent. Do not hide hydration defects, stale
content, or loading failures behind visual workarounds.

### 14.3 Define and verify performance budgets

Establish performance budgets using representative routes, devices, data volumes, and network conditions.

For web experiences, useful initial field targets at the 75th percentile are:

- Largest Contentful Paint (LCP): at most 2.5 seconds.
- Interaction to Next Paint (INP): at most 200 milliseconds.
- Cumulative Layout Shift (CLS): at most 0.1.

Use these as measurable targets, not guarantees. Their relevance depends on the experience and should be
evaluated with field data, laboratory measurements, and actual user impact.

Evaluate relevant mobile and desktop populations separately. These metrics describe web experience
performance, not accessibility conformance or complete usability.

Laboratory testing helps diagnose problems but does not guarantee equivalent field performance. Record the
tested page, device and network conditions, measurement method, observed result, and relevant limitations.

## 15. Verify the design at three levels

No single testing method proves that an interface is complete, accessible, secure, or usable. Verification
MUST be proportionate to the impact, novelty, and risk of the change.

### 15.1 Automated validation

Use appropriate automated checks for defined behavior, type safety, rules, regressions, and repeatable
interface conditions.

Depending on the feature, tests MAY cover:

- Component states and interaction outcomes.
- Valid and invalid form submissions.
- Loading, timeout, success, and failure behavior.
- Retained values and draft recovery.
- Keyboard focus and focus restoration.
- Overflow and responsive constraints.
- Rendered contrast for selected states.
- Navigation, URL, and browser-history behavior.
- Delayed requests and obsolete-response handling.
- Permissions, authorization-dependent UI, and error paths.
- Duplicate submissions and safe retry behavior.
- Localization and right-to-left layout regressions.

Tests MUST reflect the actual requirements and expected behavior. A test that passes while asserting the wrong
behavior is not evidence of quality.

Automated accessibility tools are useful for detecting defined classes of issues, but they do not establish
complete WCAG conformance or practical accessibility.

### 15.2 Direct browser and device review

Review the rendered product with realistic content and complete workflows.

Inspect applicable combinations of:

- Narrow and wide layouts.
- Short landscape viewports and enlarged text.
- Browser zoom and reflow.
- Keyboard-only navigation and visible focus.
- Reduced-motion settings.
- Supported themes.
- Relevant assistive technologies.
- Right-to-left and mixed-direction content.
- Empty, loading, populated, stale, and failing states.
- Authentication, permission, and session transitions.
- Form corrections, interrupted saves, and recovery.
- Large content collections and difficult user-entered values.

Check the actual rendered interface rather than relying entirely on source inspection, a design file, or a
screenshot.

Wait for the intended content and state before asserting or capturing evidence. An empty authentication
bootstrap frame, a pending preference restoration, or a racing request can produce a false result. Review the
whole scroll journey and complete interaction cycle, including native controls and combined component states.

Use isolated accounts and data for consequential test operations. Keep private data out of screenshots and
reports. Test destructive and failure paths without risking real user work.

Emulation is not equivalent to physical-device testing. Perform real-device testing where device-specific
behavior is consequential.

### 15.3 Representative user evaluation

For important or uncertain workflows, evaluate the design with representative users or an appropriate
user-research method.

Examine whether participants can complete the correct task, understand the information, recognize the relevant
outcome, avoid preventable mistakes, and recover from failures.

Use evidence to identify where users struggle and whether the proposed solution improves the intended outcome.

Time spent or engagement alone is not proof of a better experience. Consider task completion, accuracy,
effort, confidence, recovery, accessibility, and unintended consequences.

When direct user testing is not feasible, document the alternative evidence used and the uncertainty that
remains.

### 15.4 Record evidence precisely

For meaningful releases and high-impact changes, record:

- The tested product or component revision.
- The requirements and scenarios evaluated.
- The devices, browsers, assistive technologies, and environments used, as relevant.
- Test results and observed failures.
- Known limitations and untested conditions.
- Criterion-defined exceptions or alternatives used, with evidence that their conditions apply.
- Any authorized release deviations, remaining non-conformities, and their rationale and mitigations.
- Outstanding issues, ownership, and next action.

Distinguish actual observations from hypotheses, estimates, and assumptions. A targeted rerun is not a
complete test suite, a palette calculation is not rendered verification, and a polished screenshot is not
proof of a usable workflow.

## 16. Define acceptance criteria and manage exceptions

### 16.1 Make important requirements verifiable

Every high-impact requirement SHOULD have an appropriate acceptance criterion or verification method.

A well-defined acceptance criterion identifies the expected behavior, its applicable conditions, and the
observable result that demonstrates success.

Where meaningful, include the relevant failure and recovery paths rather than validating only the ideal
scenario.

For example, a requirement that a form preserve user input after a service failure should define the
conditions of the failure, the values that must remain, the feedback that must be shown, and the permitted
recovery action.

Not every visual principle needs a numeric score or automated test. For qualitative decisions, use explicit
evaluation questions, annotated examples, documented rationale, and appropriate design review.

### 16.2 Scale verification to risk

Prioritize verification according to the potential consequences of failure.

Areas that commonly warrant stronger review include:

- Loss, corruption, or unintended disclosure of user data.
- Authentication, authorization, and privacy.
- Financial or otherwise consequential operations.
- Destructive and bulk actions.
- Accessibility barriers in essential workflows.
- Incorrect information that can materially affect a decision.
- Concurrency, uncertain operation outcomes, and recovery.
- Large changes to core navigation or established user workflows.

A low-risk visual adjustment may require a smaller review than a change to data persistence, permissions, or
payment behavior. Verification MUST remain sufficient for the risk involved.

### 16.3 Govern non-conforming deviations explicitly

An accountable release decision-maker designated by the product's governance MAY authorize a scoped release
with an unmet internal requirement only within that decision-maker's granted authority and when all
applicable legal, safety, security, and external conformance obligations remain satisfied. This standard does
not grant authority to waive those obligations. If these conditions cannot be established, recording an
exception does not authorize release.

Every accepted deviation MUST have an explicit record identifying:

- The unmet requirement and the governance basis for the release authorization.
- The exact affected scope and rationale for the deviation.
- User impact and residual risk.
- Mitigation or an alternative approach, including its limits.
- The accountable owner and authorized release decision-maker.
- A review condition, such as a defined date, event, or change in circumstances.

Keep release authorization separate from requirement satisfaction and conformance assessment. An accepted
deviation remains non-conforming until the requirement is satisfied; it does not establish compliance or
justify a conformance claim. Neither a risk acceptance nor a documented mitigation may be presented as proof
that the original requirement was met.

Revisit the deviation under its recorded review condition and when the affected capability, technology,
user need, or risk changes. Record a criterion-defined exception separately: meeting its conditions is not
the same as accepting an unmet requirement.

## 17. Maintain components, decisions, and governance

### 17.1 Document reusable components through behavior

Document reusable components according to the roles they serve, their appropriate contexts, supported
variations, states, keyboard behavior, localization needs, accessibility considerations, and known
limitations.

Where relevant, specify:

- Default, hover, focus, active, selected, disabled, pending, success, and error states.
- Valid and invalid content.
- Responsive behavior.
- Loading and asynchronous updates.
- Keyboard and pointer interactions.
- Accessible naming and state.
- Relevant theme and directionality behavior.
- Appropriate alternatives or prohibited uses.

Components SHOULD reduce repeated decisions and improve predictable behavior. Do not create components simply
to satisfy an abstract notion of reuse when doing so introduces unnecessary complexity.

### 17.2 Maintain decisions and ownership

Record consequential design decisions along with their rationale, scope, relevant evidence, assumptions, and
known trade-offs.

When a decision is superseded, identify the newer decision and clarify what changes. Avoid retaining
contradictory rules without indicating which one takes precedence.

Define who is responsible for the product's design standards, shared components, accessibility decisions,
implementation constraints, and acceptance criteria.

Identify the authority to approve release deviations and the responsibility for assessing conformance.
Approval of a release MUST NOT be represented as authority to waive binding external obligations or to claim
that an unmet requirement is satisfied.

Review the standard periodically and after meaningful changes that could make it inaccurate or ineffective.
Use observed defects, support patterns, user research, audit findings, and changes to applicable standards to
guide revisions.

Do not update rules solely to follow a visual trend. Changes SHOULD have an understandable purpose and should
preserve or improve the standard's intended outcomes.

### 17.3 Correct reproducible barriers first

Prioritize reproducible barriers, harmful failures, misleading status, lost work, privacy risks, and other
material defects before low-impact aesthetic differences.

Distinguish observed failures from suspected causes. Verify fixes against the original scenario and relevant
regression cases.

Where an issue cannot be resolved immediately, communicate the limitation to the responsible stakeholders,
establish an appropriate mitigation, and track it until remediated. An authorized release with a
non-conforming deviation leaves that issue open and subject to its recorded review condition; risk acceptance
does not resolve the defect or establish conformance.

## 18. Definition of done

Release authorization and conformance are separate assessments. A release requires adequate evidence for its
scope and risk, with applicable MUST requirements either satisfied or subject to an explicitly authorized,
recorded non-conforming deviation under this standard's governance. All applicable legal, safety, security,
and external conformance obligations MUST remain satisfied. An unmet requirement still prevents a claim that
it conforms, even when a release is authorized. Review the following outcomes together:

- The intended tasks, information hierarchy, visual direction, and actual capabilities align.
- Content, controls, scope, and status accurately describe what the system does.
- Applicable accessibility, responsive, localization, and supported-environment requirements are verified.
- Relevant normal, pending, empty, invalid, failing, interrupted, and recovery paths are exercised.
- Persistence, concurrency, privacy, authorization-dependent presentation, and consequential actions have
  suitable evidence.
- Performance and complete interaction behavior are evaluated under representative conditions.
- Automated checks, direct interface review, and appropriate user evaluation support the claimed results.
- Known gaps, criterion-defined exceptions, authorized deviations, ownership, and maintained component
  decisions are explicit, with conformance status represented accurately.

Not every item applies to every interface. The responsible team MUST identify which requirements apply,
justify meaningful exclusions, and ensure that conditional requirements are not overlooked.

A completed checklist is evidence of process, not proof of a successful user experience. Risk-based
verification does not waive applicable mandatory requirements. Judge readiness from the actual implementation,
its users, observed outcomes, and the risks that remain.

## Guiding principle

Build interfaces that make the right action understandable, the system's actual state visible, consequential
choices informed, and errors recoverable.

Use evidence to build an experience that fits its purpose, respects its users, behaves honestly, and can be
examined and maintained. Neither novelty nor consistency is an end in itself.

## Appendix A. Web implementation checklist

Use this checklist to apply the standard to web implementation and code review. Items restate requirements
from the referenced sections or name common techniques for meeting them; they do not add requirements or make
a technique mandatory. Check each item only where its capability, platform, and browser support apply, and
confirm the result in the rendered interface.

### A.1 Semantics and focus (6.1–6.3)

- Actions use `<button>`; navigation uses `<a href>`. Clickable non-interactive elements are replaced rather
  than patched with roles and key handlers.
- Focus styles use `:focus-visible` or an equivalent. `outline: none` appears only with a visible replacement.
- Anchor targets clear sticky headers, for example with `scroll-margin-top`.
- Modal backgrounds are inert, for example through `<dialog>` with `showModal()` or the `inert` attribute.
- Asynchronous status uses an appropriate live region, such as `role="status"`, without moving focus.
- Icon-only controls have accessible names; decorative icons are hidden with `aria-hidden="true"`.

### A.2 Forms and input (7)

- Each control has an associated `<label>`, and hints and errors are linked with `aria-describedby`.
- `type`, `inputmode`, `autocomplete`, and `name` match the data; numeric identifiers do not use
  `type="number"`.
- Spellcheck and autocapitalization are disabled for codes, usernames, and email addresses where they
  interfere.
- Paste, autofill, and password managers are not blocked.
- Enter does not submit during input-method composition (`isComposing`).
- Submission stays available until a request starts, then shows pending state and prevents duplicates.

### A.3 Pointer and touch (6.4, 12.3)

- Hit areas meet the target-size criterion, extended with padding or a pseudo-element where the visible glyph
  is smaller.
- Checkbox and radio labels activate their controls without dead zones between them.
- `touch-action: manipulation` is used where double-tap zoom is not needed on a control.
- Scroll containers in overlays and drawers use `overscroll-behavior: contain` where scroll chaining is
  disruptive.
- Hover-only affordances have a focus and touch equivalent, gated with `@media (hover: hover)` where
  appropriate.

### A.4 Layout and viewport (5)

- The viewport meta does not set `maximum-scale=1` or `user-scalable=no`.
- Fixed and sticky elements account for `env(safe-area-inset-*)` when `viewport-fit=cover` is used.
- Full-height regions use `dvh` or `svh` deliberately, with a `min-height` that lets content grow.
- Flex and grid children that contain text can shrink (`min-width: 0`), and long values wrap with
  `overflow-wrap: anywhere` or are truncated with access to the full value.
- Document-level `overflow: hidden` is not used to hide a local layout defect.

### A.5 Typography and content (3.3, 4)

- Text uses relative units and can grow; containers do not depend on fixed heights.
- Columns of compared numbers use `font-variant-numeric: tabular-nums` where the typeface supports it.
- The ellipsis character and language-appropriate quotation marks are used where typography is controlled.
- Non-breaking spaces keep values with their units and short fixed phrases together.
- Brand names, code, and identifiers that must not be translated use `translate="no"`.

### A.6 Images, media, and fonts (3.5, 14.1)

- Images and embeds reserve space with `width` and `height` or `aspect-ratio`.
- Informative images have meaningful `alt`; decorative images use `alt=""`.
- Offscreen media uses `loading="lazy"`; the likely LCP image does not, and may use `fetchpriority="high"`.
- Responsive images use `srcset` and `sizes` with suitable formats.
- Fonts declare `font-display`, subsets keep the required script coverage, and only critical fonts are
  preloaded.

### A.7 Motion and preferences (3.7, 6.6, 12)

- Motion respects `prefers-reduced-motion`; transparency effects respect `prefers-reduced-transparency`
  where supported.
- Required boundaries, selection, and focus survive `forced-colors: active`.
- Animations prefer `transform` and `opacity` and name properties explicitly instead of `transition: all`.
- Final states do not depend on `animationend` or `transitionend` firing.

### A.8 Theming (3.4)

- `color-scheme` matches the active theme so native controls and scrollbars follow it.
- `<meta name="theme-color">` matches the page background where browser chrome uses it.
- The initial theme renders without a flash of the wrong theme, and native `<select>` options remain legible.

### A.9 Navigation and state (8, 9)

- Shareable state such as filters, tabs, and pagination is reflected in the URL when appropriate, and
  sensitive values are not.
- Links support opening in a new tab; Back and Forward restore useful position and filters.
- Responses are ignored when they belong to a superseded request, for example with `AbortController` or
  request identifiers.
- Text input updates immediately, and costly downstream work is debounced.

### A.10 Localization (11)

- `<html lang>` and `dir` are set, and changes of language within content use `lang`.
- Layout uses logical properties such as `margin-inline-start` and `inset-inline-end`.
- Directionally distinct values are isolated with `<bdi>` or `dir="auto"`.
- Numbers, dates, currencies, and lists are formatted with `Intl` APIs or equivalents for the chosen locale.

### A.11 Rendering and security (10.2, 14.2)

- Server and client output agree; time, locale, random, and storage-dependent values do not differ between
  them.
- Untrusted content is rendered as text, not inserted as HTML.
- Layout reads and writes are not interleaved in loops, and long lists are virtualized only after measurement.
