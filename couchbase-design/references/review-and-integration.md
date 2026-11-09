# Review and integration

## Verify the rendered state

Review the actual app at desktop (~1280/1440), tablet (~768/1000) and phones (390 and 320px), including a short desktop viewport. Test the affected component in light and dark. Resize, scroll to the bottom, and open the controls being changed.

Check relevant states: selected/unselected workload, all selected, cleared, long labels, full estimate, editing and returning, invalid/zero amounts, open dropdowns, expanded methodology and keyboard focus. Confirm no horizontal overflow, no clipped model/input-output fields, no overly tall blank inputs card, no sticky panel hiding expanded content, and no theme-dependent geometry shift.

For motion, sample rendered transforms/positions at separate times and inspect visibility behind actual panels. Verify reduced-motion CSS and, when supported, emulate it. State whether it was inspected or runtime tested. A desktop browser viewport check is not physical-device performance testing.

Contrast: body text 4.5:1 minimum, large text and meaningful UI edges 3:1. Decorative background need not meet a text contrast target, but cannot obscure information. Do not claim a full accessibility audit from a color check alone.

Save a current screenshot with enough context to review the requested change. Report observed results, not an unsupported "everything is perfect" or fabricated usability score.

## Mathematical behavior in calculator work

Pure styling changes should preserve the math. If calculator logic changes, use an independent expected-cost calculation and meaningful edge cases: input/output separation, cache savings on both token types, prompt reduction on input only, overlapping reductions, zero and complete reduction, finite/infinite break-even, reservations versus billed on-demand hours. Never claim GPU fleet costs fall automatically just because prompt tokens fall. Distinguish estimated model savings from net savings after Couchbase/implementation costs.

The existing calculator has 17 tests including one million seeded cases; that count belongs to that project, not this skill. Run available appropriate tests and report actual outcomes. Do not invent a required million runs for a new page or rerun math tests for every color tweak.

## Host website integration

The reference TCO app lives inside a WordPress site. Scope component CSS, custom properties and events to a calculator root; avoid global body/button/input rules or unscoped document listeners that conflict with the host. Reuse approved host typography, container widths, navigation and footer. Avoid depending on a local filesystem or a particular Vercel/GitHub account.

The demo source accumulated many overrides during exploration. Copy visual decisions, not that cascade. Consolidate active component rules when the task touches them; avoid unrelated refactors. Shared tokens and component styles should have predictable specificity.

## Evidence, preferences and validation scenarios

For a reference update, record: inspected URL/date, state/viewport, font resource and computed family, exact colors, component size/border/radius, and which values are measured versus inferred. No need to scrape the whole website for a small known fix.

Scenario checks for this skill:
1. "Make it more on-brand" → inspect reference controls and typography, preserve accepted structure; do not launch a full redesign.
2. "Green checks look dull" → compare geometry, border and tick as well as #21EA2A; do not choose an arbitrary brighter green.
3. "Accent is invisible" → inspect occlusion, opacity and actual movement; do not only slow down a tiny animation or reintroduce the rejected corner graphic.
4. "Small estimate has gaps" → inspect container widths, grid/flex behavior, spacing and copy before adding decoration or enlarging type.
5. "Demo recap should follow choices" → align and conditionally pin on desktop, verify short-height/expanded states; retain normal mobile flow.
6. "Apply to a different app" → use brand tokens/assets and appropriate UI patterns, not the calculator's wizard, math, hardcoded selectors or deployment targets.
7. "Looks good" → finish requested work; do not infer permission to publish to upstream. A specific push/deploy instruction should be followed using verified current destinations.
