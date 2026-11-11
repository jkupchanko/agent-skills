# Approved demo defaults

Use these defaults for John's Couchbase demo family. They describe the accepted direction, not official company requirements. Inspect the current project and follow the latest explicit instruction. Do not rebuild an accepted interface to force a template.

## First-pass setup

| Role | Starting treatment |
|---|---|
| Shell | Linked Couchbase logo, matching favicon, compact cream banner, working UI directly below, existing footer links |
| Type | Permitted Centra No2 500 headings, loaded Inter body; 28–32px banner, 18–22px panel titles, 15–16px reading text, 14px controls, 13px technical metadata; inputs 16px |
| Surfaces | Clearly bounded neutral sections; 6–8px corners for compact process/evidence cards; preserve established larger outer-card corners |
| Color | Red actions, warm context, neutral evidence, quiet cream outcome; distinguish adjacent surfaces without flooding every card with color |
| Dark | Black canvas, charcoal cards and lighter controls; readable neutral edges; retain cream banner with dark ink |
| Density | One heading, brief supporting text only where useful, one obvious action; details on demand |

Use the `data-density="demo"` variant in the bundled tokens as a starting point for a new compact demo. It is not a CSS replacement for an existing product. Desktop width does not justify marketing-sized headings or tall empty cards. Match computed font roles across all views, including reference screens.

## Toolbar and disclosures

- Use a familiar sliding light/dark switch at the far right. Align its touch target with the other controls; its visible shape remains a switch, not an equal-width rectangular action button. Keep the thumb visibly light against the dark track. A compact share icon retains an accessible Copy link name and feedback.
- On phone and iPad widths, place main navigation on its own row beneath brand/actions when one row crowds. Preserve the established single-row desktop layout. Keep short labels on one line, including storm status; size the container rather than compressing words.
- Use plus/minus for expandable sections and the More menu, with readable red emphasis when open. Selection dropdowns retain their appropriate selection affordance and keyboard semantics; plus/minus is not a universal replacement for every select.
- Keep 44px touch targets, consistent trigger padding, visible focus and viewport-contained menus. Check open content as well as the trigger. Keep copy controls at the top right of each command with an accessible name and brief Copied feedback.

## Distinct content roles

**Conversations:** named passenger/guest and airport/concierge speakers, short messages in separate rounded bubbles, consistent reading size, distinct incoming/outgoing surfaces. A brief typing indicator and one-at-a-time arrival may show progression. Keep the scroll position stable; follow the latest message only while the reader is at the end. Keep complete message content accessible.

**Tool evidence:** aligned squared Input and Result sections, function name, readable status, concise returned evidence. These are not alternating chat bubbles. Separate the decision from the customer reply. Policy evidence shows why it matched and its version; tools distinguish selected, actually called, skipped and failed. Show observable execution and a concise rationale, never claim private model thoughts.

**Saved activity:** a coherent parent for prior runs with clearly grouped request, checks and outcome. Receipts expose reference, result and saved state, with review/edit where supported. Keep Saved activity anchored at the lower left of its panel in normal layout, with clearance from scrolling content; do not overlay it on a decision.

**Copy:** use sentence case, short familiar labels and vertically separated messages. Avoid decorative middle-dot separators, slash-heavy headings, raw urgency numbers without meaning, and bullets in the compact Decision summary. Use a short plain rationale. Keep necessary live/simulated and cost qualifications once in an appropriate context, not repeated filler on every card.

## Layout and live behavior

Use an explicit layout mode. An idle activity panel can hug its content. Once a run begins, keep its agreed frame stable through tool changes and completion, with internal scroll for overflow. In the hotel split view, Activity details is its own card below Agent activity; expanding details reallocates the right column rather than pushing it beyond the conversation. Give each scrollport a clear owner and use min-height:0/min-width:0 on shrinking grid/flex children. A natural mobile stack is preferable to forced desktop heights.

For paired dashboard panels such as flight map and message activity, keep aligned outer edges and stable desktop/iPad heights while statuses change. Reuse the approved compact view, not an arbitrarily huge min-height. Eliminate duplicate request lists. Keep conversation entry points visible and navigable without restarting the visitor's run; returning to the map can subtly highlight the previous request.

Animations follow real or explicitly simulated state: pending, running, returned, failed. Use a single clear current action with restrained motion. Keep the current tool visible even when evidence scrolls. Do not invent results to animate a live request. Honor reduced motion and preserve focus and reading position.

## Walkthrough and technical screens

Use one opt-in Show me around action in the banner/dashboard. Highlight the target and place brief text plus a small animated example beside or below it. Overlap unrelated UI if needed, never the highlighted target. Keep Next, Back and Close reachable on phone and short desktop screens. Avoid duplicate How it works pages when the guided tour serves that purpose.

Commands, Recovery, Cost and screens under More reuse the same type/surface/disclosure roles. Show actual connection state, SQL/model execution path and memory availability separately; a deployed or Healthy label is not proof of a successful inference. Keep per-command copy controls. Link interface claims to the current implementation, not old fixtures.

For multi-visitor demos, verify two separate sessions retain separate run IDs, storm state, selections and conversations. UI navigation must not restart a run. This is a verification requirement, not authorization to change cloud architecture or credentials.

## Minimum verification for the affected pattern

Check a narrow phone (about 390px), iPad (about 820px), and desktop (about 1440px), plus 320px when changing toolbar sizing. Test both themes, long labels and text zoom where relevant. Exercise idle, running, completion, failure, repeated disclosure toggles and manual scroll during updates. Check dimensions and reachable content, not just screenshots. Report any untested state honestly.
