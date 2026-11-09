# Agent demo design

Use for conversational demos and adjacent activity inspectors. These preferences came from the hotel concierge demo reviewed on 2026-11-08; adapt the content and functions to each product. Preserve the approved calculator patterns elsewhere.

## One current action, optional evidence

Keep conversation and current activity alongside each other where width permits. Lead activity with a short current-action title, one reason or result, and the active function name when running. On completion, replace this with the outcome or confirmation. Keep policy, tools and saved state available without exposing them all at once.

Approved disclosure depth:
- **Activity details:** compact tool rows with function name, status and a short actual output; one saved-memory summary.
- **Why this decision:** policy and concise tool-selection explanation, collapsed by default.
- SDK examples are optional technical content inside the explanation, also collapsed.

Do not repeat the same policy, outcome or price in several visible sections. Keep necessary simulation labeling visible. Show facts used, tools called or skipped, returned evidence and a concise decision rationale; do not represent this as access to private model thoughts. Distinguish application-defined simulated functions from real SDK methods.

Apply the same presentation through search, selection, confirmation, unavailable results, edits and restored receipts. A confirmed demo booking should show its reference, total and what was saved. Never imply persistence beyond the actual storage lifetime.

## Stable, compact layout

Update existing activity rows in place. Rebuilding the entire panel on each event caused jumping, lost disclosure state and scroll drift in the hotel demo. Keep open disclosures stable during the same run. Use one restrained running indicator; avoid simultaneous pulsing, orbiting and entrance motion.

The empty state should hug its heading and short helper text, not reserve a tall timeline. Remove minimum heights, empty list margins and grid stretching where they create blank space. Use consistent 8–12px internal gaps and roughly 16–24px panel padding as starting points. Avoid stacking padding from nested wrappers. Keep bottom padding as deliberate as top padding.

A compact summary can follow the chat on desktop, but disable sticky behavior when expanded content cannot fit the viewport. Avoid separate competing scrollbars. Use normal stacked flow on narrow screens. Confirm expanded details and long function names remain accessible.

## Seamless surfaces and outlines

The user approved more visible neutral boundaries, not more content or decorative color. Keep a clear outer panel, compact outlined tool rows, a subtly filled saved-memory row and a bounded explanation disclosure. Avoid repeatedly nesting white cards within white cards.

The **Agent activity header must share its panel background**. An old sticky-header rule painted a white strip over the warm-gray panel and looked like an unrelated banner. Inspect inherited background, negative margins and sticky padding before altering the palette. Match light/dark geometry; make only the requested local adjustment when other colors are accepted.

Hotel-demo starting colors (personal approval, not official tokens):
- Light activity surface #F3F2EE; outer border #B9B6AE; white tool rows with #C4C0B7 borders; saved-memory fill #E9E7E0.
- Dark activity surface #242424; tool rows #303030; saved-memory fill #393939; boundaries #626262.
- Preserve the approved cream result and Couchbase red actions. Amber is restrained running-state feedback, not a blanket border.

Use semantic tokens rather than copying the prototype's accumulating CSS overrides. Header background should inherit its panel; readable disclosure text should use normal ink, with theme-appropriate emphasis when open. Validate contrast in the actual rendered theme.

## Consistent type roles

Keep Centra No2 headings and Inter body. The compact hotel demo approved this starting scale: panel heading 22px; result heading 20px; reading text 15px; controls and disclosure labels 14px; secondary statuses and function names 13px. Inputs remain 16px. These values are scoped to the compact demo, not replacements for the website scale.

Match equivalent roles across chat and activity, including nested disclosures. Use weight and spacing for hierarchy rather than many one-off sizes. Keep body line-height around 1.5–1.6; allow function names to wrap. Check computed sizes, not just declared CSS: inherited rules and mobile overrides previously caused inconsistencies.

## Focused validation

Inspect initial empty state, running tool, completed result, open Activity details, deeper explanation and confirmation. Check the affected view in both themes and at a narrow width; include a short desktop viewport for sticky layouts. Verify no clipped output, unexplained bottom gap or duplicate legacy panel. For a pure surface tweak, visual checks suffice; for renderer or state changes, test disclosure preservation, skipped tools and result restoration. Do not claim a live model integration from simulation tests.
