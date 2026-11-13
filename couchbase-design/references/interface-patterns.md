# Interface patterns

## Layout and proportion

Use a shared content width/centerline for header, hero and app; reference content width is about 1260px. Container padding commonly 24–32px, section gaps 24–48px, cards 20–24px. These are starting points, not mandatory dimensions across all products. Restrained 12–16px corners and single borders define sections. No nested white illustration box inside the cream hero.

For compact demos and calculators, prefer the approved Hotel Concierge banner proportions: a shallow cream surface with concise copy and supporting custom geometry (coral, ochre, blue-gray and cream), so the working interface appears sooner. The savings calculator adopted this treatment on November 10, 2026. Keep artwork recognizable without letting it dictate an oversized hero.

Measured reference for this composition: approximately 189px desktop height, 20px vertical / 28px horizontal padding, 32px heading at 1.15 line-height, and artwork around 148px tall within a 360px-wide column. These are reference measurements, not universal fixed heights. Let longer copy and text zoom grow naturally; never clip to enforce the reference. On phones, stack and center copy/art with 24px padding, a 28px heading and approximately 110px artwork. Keep geometry identical in light/dark mode and check for horizontal overflow. Preserve the existing logo, wording and illustration unless separately requested. Verify the served CSS and invalidate its asset cache when needed; old overrides can silently win despite an edited stylesheet.

## Guided forms and controls

Use three evenly sized label tabs for the calculator, 52px high, 3px red active underline, stable widths between steps. Keep them left-aligned within their column; text is centered inside each tab. Do not add ornamental numbers/check badges to tabs. Required inputs gate advancement; optional refinements may be skipped only when valid defaults exist. Editing retains values and recomputes dependents.

Controls: at least 44px targets; main inputs roughly 48px. Keep chevrons, vertical centering, selected states, menu spacing and button radii consistent across billing/model/all other dropdowns. Inspect the opened menu, not only its trigger. Use accessible native behavior or a tested equivalent; custom menus need keyboard navigation, focus management, Escape dismissal and viewport containment.

Selected workload checkbox matches the measured TCO treatment:
- 46×46px border-box, 4px solid #000, radius 16px, fill #21EA2A.
- Tick SVG viewBox `0 0 28 28`, path `M7.5 14.5 12 19l8.5-9`, no fill, black stroke width 4, round caps/joins. Fit to the inner 38px square.
- Keep a real labeled checkbox and visible keyboard focus. Do not encode selection only with color.

Primary actions use red with white type, 12px corners, dark-red hover/pressed states. Secondary edits use a red outline, dark-red text in light mode and readable soft-red text in dark; fill red on hover. Edit spend/workload should match. Do not make every secondary action a primary button.

Use a compact pill-shaped light/dark switch with a sliding thumb and accessible state. Do not copy Apple fonts or glass treatments merely because the interaction resembles Apple's switch.

## Workload recap and compact estimates

During desktop demos the right-side inputs recap starts lower, aligned near the workload heading/choices, and stays alongside the form as the user scrolls. The calculator used a 180px initial offset and sticky viewport inset; treat those as a reference, not a universal magic number. Measure the actual header, sidebar height, expanded details and viewport. Never trap content below a short viewport; use normal scrolling or disable sticky when it cannot fit. A summary should be beside the active interaction, not stranded above it or centered halfway down a very long document.

Use empty space for existing supporting content before art. Methodology can sit below the recap. At narrow widths stack the summary with width:100%, min-width:0 and border-box sizing. Do not leave a content-sized card floating narrower than the results.

For the compact estimate summary, tablet layout uses two short fields across and workload across the full next row. Phones use compact label/value rows and two evenly sized edit buttons. Keep all inputs accessible without repeating them in several cards. Verify long workload names, currency ranges and empty/zero values.

For calculator results: lead with one cream-highlighted savings answer, then current/estimated cost, short essential caveat, and a single-sentence CTA with an obvious contact action. Advanced assumptions belong behind a well-aligned disclosure. Keep factual caveats about model-only savings, setup costs and workload assumptions intact. A demo is not a full explanatory diagram.

## Motion and background accent

Use the approved steel-blue secondary accent as a slowly moving background stroke behind opaque content panels. Keep the lower-right standalone graphic removed. No purple/periwinkle, new colored cost-box tint, replay button or ornamental widget. Use CSS/SVG geometry for this motif, not a generated raster.

An accepted starting range is 16 seconds per desktop sweep with about ±100px horizontal / ±55px vertical travel and ±3° rotation; mobile about 20 seconds with ±40px / ±28px and ±2°. Ease gently at each end. These values followed a rejected 48–56 second, ±8–24px drift that was effectively invisible. Judge visible movement over several seconds on the actual page, not from an animation declaration.

Use transform-based animation, clipped noninteractive decorative layers, stable mobile viewport units (svh), and separate theme opacity (roughly .48 light / .42 dark as a starting point). Keep readable text and footer surfaces clear. Stop for prefers-reduced-motion and when the document is hidden. Evaluate applicable pause/stop requirements for ongoing motion; for a surface that needs user control, use a finite animation or an accessible motion setting rather than a prominent decorative pause widget. Do not claim accessibility compliance from the media query alone. Do not assume a static screenshot proves motion; compare positions over time. A smaller screen needs its own composition, not only a scaled desktop motif.

## Methodology and footer

Methodology is left-aligned with balanced inner spacing, matching card colors and legible disclosure headers. Highlight the active question in the theme's readable red, animate expansion smoothly, and avoid clipped text or tooltip overlays. Do not center entire paragraphs simply because spacing is wrong.

Standalone footer: concise Explore / Learn / Connect groups, official social icons and actual verified destinations. Existing calculator uses X, LinkedIn, YouTube, Facebook, GitHub, Stack Overflow and Discord. Do not invent accounts or copy social URLs blindly to an unrelated organization. When integrating into couchbase.com, use the host header/footer instead of duplicating them.

## Feedback notifications

For the feedback workspace, keep a compact bell in the approved top toolbar. Its unread badge uses Couchbase red with white centered numerals, a circular shape for short counts and enough horizontal padding for `99+`. Hide it at zero; cap only the visible label, not the underlying unread total. Give the bell an accessible name with the actual unread count. Preserve the existing toolbar order and theme switch unless the user requests a change.

Keep the badge legible in light and dark mode with a border matching the surrounding surface. It must not clip at the viewport edge, collide with neighboring controls, or shrink the bell's touch target. Check 1, 99, and 105 unread at phone and iPad widths; 105 displays `99+`. Avoid fixed-width circles that squeeze three characters.

Clicking an update opens the relevant channel or DM and highlights the specific reply when available. Reading that conversation clears its unread state, while activity elsewhere and later arrivals remain unread. Closing a discussion must also refresh stale “New” labels. Mark all as read changes read state; dismissing an item is a separate action and does not delete its message.

Use the paired UI pattern repair skill's notification checks for polling, navigation, and read-state regressions. Test with disposable local accounts and records, preserving live messages and accounts.

## Feedback invitations and navigation contrast

Keep the admin dashboard's **Invite people** shortcut opening Invitations directly. Pending emails are clickable. Within the same page session, reopening reuses the link; after refresh, explicitly offer a replacement that preserves recipient and role and invalidates the old link. Do not rotate links just by opening the list. Never claim email was sent when it was only copied or downloaded.

Make the primary sharing action one portable PDF with embedded artwork and a real join-link annotation. Both the artwork's apparent button and the explicit Join button must open the same valid invitation. Use the stored expiry and role; never show User artwork for an Admin invitation. Phone file sharing uses the native share sheet when supported, with a Save/Download invitation fallback. Keep copy/link/image alternatives under **Other ways to share**, with comfortable touch targets and wrapping controls. A standalone PNG cannot contain a clickable link, and HTML clipboard formatting is not reliable across mail apps.

For the feedback app, distinguish the navigation rail using a neutral gray surface and visible divider against the conversation surface. Dark mode uses a darker neutral rail and a lighter selected row. Emphasize section headings and the active channel, keeping ordinary rows regular weight. Preserve Couchbase red for compact selection/action emphasis; do not turn every outline red. Keep the collapse control's backdrop opaque and matched to the rail while scrolling, and preserve the approved responsive frame.
