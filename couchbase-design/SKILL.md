---
name: couchbase-design
description: Use when creating, refining, or auditing Couchbase-branded web interfaces, calculators, dashboards, or demos for John. Applies the measured Couchbase website visual language and his approved UI preferences, including light/dark themes, controls, responsive summaries, and restrained motion. Not for database/backend work without a design task.
---

# Couchbase Design

Design for a quick, legible product demonstration that feels at home on couchbase.com. This is John's reusable design profile, not an official Couchbase brand manual. Use the current user request over these defaults.

## Start with evidence

- Inspect the existing UI, current styles, assets, and active component states before editing. In a reference calculator, scroll down to the actual app and click its controls; the marketing header is insufficient evidence.
- Preserve the accepted product structure, wording, math, and behavior unless the task changes them. Do not answer complaints about hierarchy or crowded copy by merely enlarging everything.
- Read [brand-system.md](references/brand-system.md) for brand assets, colors and type. Read [interface-patterns.md](references/interface-patterns.md) for layout, controls and motion. Read [review-and-integration.md](references/review-and-integration.md) for audits, validation or website integration.
- For new UI, use [tokens.css](assets/tokens.css) as a scoped starting point. Adapt its root selector to the app. Do not paste the calculator's accumulated global CSS overrides into another project.

## Design priorities

1. **Brand alignment:** aim approximately 75% existing Couchbase website language, 25% custom demo craft. This is a qualitative preference, not a measurable compliance score. Match actual font family, size, weight, state colors, logo and spacing before inventing decoration.
2. **Clarity:** short headings, one useful supporting sentence, one obvious next action. Keep details available without showing them all at once. Never hide essential assumptions or caveats just to shorten the page.
3. **Layout:** aligned bounded sections, even tabs, practical buttons and a shared page centerline. Fix unused columns and intrinsic-width cards before filling space with art.
4. **Theme consistency:** light and dark share geometry. Dark is a black canvas with charcoal cards and lighter controls; the beige hero stays beige. No white card islands or blanket red panel outlines in dark mode.
5. **Character:** custom artwork may share the brand's geometric language without copying a whole page. Accent motion must be actually visible, smooth, behind content, and absent for reduced motion. No standalone decorative object in the lower-right gap.

For conversational agent demos, recovery/tool evidence, simulation reference pages, and activity inspectors, read [agent-demo-design.md](references/agent-demo-design.md). It records the approved compact layout, surface hierarchy and observable decision presentation.

## Consistent updates with UI pattern repair

For an existing Couchbase interface, when John identifies an example of confusing hierarchy, spacing, controls, or live-state behavior, also use [ui-pattern-repair](../ui-pattern-repair/SKILL.md). This profile owns the brand and approved visual direction; UI pattern repair owns diagnosis, matching-component cleanup, and state verification. New designs do not require the repair workflow unless a repair task is present.

Infer the shared pattern from the example and inspect equivalent components without requiring John to list each occurrence. Keep the scope tied to that pattern, preserve accepted layout and behavior, and explain material tradeoffs before expanding into a redesign. Use heading weight, grouping, spacing and quieter technical metadata before increasing all text sizes or adding copy. Color reinforces meaning; readable labels must carry it too.

A useful request is: “Use the Couchbase design and UI pattern repair skills. Treat this issue as an example, check matching places throughout the demo, preserve the approved design, and verify the affected states.” Naming Couchbase design alone is enough to trigger this pairing when the task fits.

## Latest preference wins

- Accepted compact demo banner: Hotel Concierge proportions, transferred to the savings calculator; see interface-patterns.md for responsive reference measurements. Keep the app close below the banner rather than using a tall marketing hero.
- Accepted: official logo linked to couchbase.com, matching favicon, Centra No2 headings and Inter body, warm cream banner and savings highlight, black/charcoal dark mode, concise CTA, red actions, uniform dropdowns, compact inputs summaries, desktop workload recap next to selections.
- Accepted selected checkbox: exact TCO green **#21EA2A**, **46px** square, **4px black border**, **16px radius**, bold rounded black tick. Color alone did not reproduce the reference's appearance.
- Accepted decorative accent: muted steel blue **#547D91** in light, **#789AAA** in dark. Rejected purple/periwinkle, blue-green tint on the annual-cost box, extra corner motif, and barely perceptible drifting lines.
- Rejected: excessive prose, tiny low-contrast subtext, oversized message text, tooltips covering content, nested box clutter, numbered decorative step badges, arbitrary top-header slogans, replay controls, and a visible pause-background control. Respect reduced motion and pause background work when the page is hidden. If a requested ongoing effect requires a pause mechanism for accessibility, prefer a finite effect or an accessible motion setting; explain that tradeoff rather than claiming reduced motion alone guarantees compliance.
- The calculator uses ordered Spend / Workload / Estimate tabs. Keep required steps gated, retain edits, and show actual answers only when enough input exists. Other products should use their own appropriate navigation; do not force this wizard on every app.

## Combine design disciplines, not entire skill packages

This profile consolidates the useful principles from Palette (cognitive load, feedback and state inspection), Color System (semantic accent roles and separate theme values), Impeccable/frontend-design (intentional visual hierarchy and rendered verification), Apple design (practical familiar controls), and UI/UX/accessibility review (responsive and keyboard behavior).

It is self-contained. Do not install or load all those skills for each edit. Use an available specialist only for a real gap, such as complex animation or a full accessibility audit. Their generic aesthetic defaults do not override this profile's deliberate brand choices. See [provenance.md](references/provenance.md) for sources and asset status.

## Delivery boundaries

A design request is not authorization to publish, grant access, push to another person's repository, or change production settings. Follow the current session's explicit destination and authorization. Report local, committed, pushed and deployed states separately. Never carry repository permissions from the original calculator conversation into a new project.

Finish by describing the concrete change and relevant visual/functional checks. For UI edits, show a current screenshot when supported. If production was requested, verify the actual production alias after deployment; a local screenshot does not prove it is live.
