---
name: ui-pattern-repair
description: Use when a user points out a UI problem as an example and wants matching issues repaired across an existing interface while preserving its approved design. Covers scoped visual cleanup and state-dependent layout regressions, especially live panels and disclosures.
---

# UI pattern repair

Treat the reported example as evidence of a reusable pattern, not permission for a redesign. Fix the example, inspect equivalent components, and preserve approved structure, colors, type families and behavior. For Couchbase work, apply the installed couchbase-design profile rather than inventing new branding.

## Pair with the product design profile

For Couchbase-branded work, read [couchbase-design](../couchbase-design/SKILL.md) for fonts, colors, assets and approved component treatment. Apply this skill for the repair method; do not substitute a new aesthetic or copy the brand rules into this file. The user's latest instruction takes precedence over both skills. For other products, use their existing design system instead.

## Establish the repair boundary

Inspect the current UI and implementation before editing. Identify the reference the user approved, the specific defect, related instances and what must stay unchanged. Do not ask the user to repeat known preferences. State the intended scope briefly; do not turn routine implementation choices into an approval process.

Group genuinely equivalent roles: disclosure headings, menu options, labels, statuses, input rows. Do not impose identical sizing on unrelated controls. Use hierarchy, shorter wording and consistent padding before globally increasing text.

## Diagnose state problems with evidence

A blank accordion is not automatically a missing-data bug. Compare its open state, DOM content, computed visibility, scroll position and viewport intersection. Check whether its content simply opened below a bounded scrollport. Distinguish a reproduced cause from a plausible hardening measure; do not claim an intermittent failure is solved merely because one toggle worked.

Capture the failing state or a targeted regression before changing renderer behavior. Inspect the actual served version: local and hosted builds, cache keys and asset versions can differ. Avoid stacking overrides on an unverified cached build.

## Preserve the live frame

For live activity, preserve stable node identity (or keyed components) so focus, open disclosures and reading position survive events. Measure panel dimensions at running and completion, not just in a static screenshot. Keep long content scrollable and reachable within the agreed frame. Do not enforce fixed sizing universally: empty states and unrelated panels may need natural height.

Make the current action discoverable without moving the entire page. A compact pinned current-tool label can coexist with an internally scrolling tool list. Follow a newly active row once per transition while follow mode is active, not on every render. Pause automatic following after manual scrolling; retain the pinned label. If the reader opens an explanation, preserve that reading position while the pinned label continues updating. Do not force a collapsed section open.

When a disclosure opens near the bottom, reveal its heading and some content within its own scroll container. Reset invalid stale offsets when collapsing/reopening or replacing a run; otherwise preserve useful reading position. Avoid smooth animation that competes with incoming updates. Respect reduced motion.

## Verify the pattern, not just the example

Choose checks based on the affected behavior:
- Idle, running, completion, blocked/skipped tools and a new request.
- Open, closed, nested-open and repeated toggles while updates arrive.
- Long tool names and outputs; keyboard focus and internal scroll access.
- Narrow phone, intermediate two-column layout and desktop; relevant themes.

Compare the same dimensions across states. Check for clipping and unintended page scrolling. Use targeted automated tests for state changes, with visual verification for geometry. Do not repeat unchanged checks after they pass unless new evidence warrants it.

## Check supporting screens and copy

When a user asks for consistency throughout a demo, include secondary navigation and reference pages, not just the primary workflow. Compare equivalent headings, cards, disclosures, status labels and empty states. Check that explanatory copy describes the current scenario and distinguishes simulated fixtures from live services; visual consistency cannot repair contradictory claims.

If sectioning increases card height, reduce repeated metadata, label stacking and surplus padding before shrinking reading text. Keep full user messages and outcomes accessible. Use the product profile for preferred treatments, such as aligned tool input/result blocks; do not spread a chat metaphor to unrelated components automatically.

## Deliver and retain

Report the concrete fixes, representative checks and remaining uncertainty. Distinguish local, committed and deployed status. Publishing requires the user's existing authorization for that destination; this skill grants none. If publishing is authorized, verify the actual shared URL and retain a screenshot of the served result.

Save durable preferences to the relevant design profile only when requested. Avoid encoding temporary pixel values, one demo's markup, or speculative root causes as universal rules.
