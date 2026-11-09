# Design skills for Codex and Claude

Two reusable instruction sets that help an AI coding agent build clear Couchbase interfaces and improve an existing UI consistently. They carry forward the design decisions and repair methods developed while building John’s AI savings calculator and Harborline hotel concierge demo.

**Couchbase Design defines the visual direction. UI Pattern Repair defines how to diagnose, fix, and verify a UI problem across matching components.** Use both for most improvements to an existing Couchbase demo.

These are instructions and supporting assets, not an application, a hosted service, or a connection to Couchbase. Installing them does not start cloud resources or incur hosting charges. They guide the agent; the agent still needs access to your project and appropriate tools to inspect, edit, and test it.

## What each skill does

| Skill | What it helps the agent do | When to use it |
|---|---|---|
| [Couchbase Design](couchbase-design/SKILL.md) | Apply consistent fonts, colors, logos, light/dark surfaces, controls, spacing, responsive layouts, and restrained motion. Make demos easy to follow. | Building a Couchbase interface, bringing a demo closer to the company website, or refining an existing design. |
| [UI Pattern Repair](ui-pattern-repair/SKILL.md) | Treat one reported defect as an example, find equivalent issues, identify the cause, repair the shared pattern, and verify relevant screen sizes and interaction states. | Dropdowns look inconsistent, text hierarchy is unclear, panels jump during updates, details appear blank, content overlaps, or scrolling behaves incorrectly. |

UI Pattern Repair also works on other brands: use that product’s design system instead of applying Couchbase styling. Couchbase Design is not intended for backend-only database tasks.

## Best way to use them

Give the agent the project, a concrete example of the issue, and what you want to preserve. A screenshot, page URL, or reproduction steps helps it inspect the actual problem. You do not need to enumerate every matching component.

A useful request:

> Use couchbase-design and ui-pattern-repair. The Activity details dropdown has crowded text and sometimes appears blank. Treat this as an example and inspect matching disclosures throughout the demo. Keep the approved colors, fonts, and panel layout. Verify opening, closing, scrolling, and live updates on desktop and a smaller screen. Explain what you fixed and what you tested.

For a new interface:

> Use couchbase-design to build a clean Couchbase demo. Make the request, current action, and result easy to distinguish, with short copy and optional details. Use the existing brand assets and check the layout in light/dark mode and at a narrow width.

For another brand:

> Use ui-pattern-repair to clean up inconsistent dropdown spacing throughout this app. Follow this project’s existing design system and preserve its accepted layout.

Ask for the outcome rather than prescribing every pixel. For example, “Make the active tool visible without scrolling the page” gives the agent room to inspect and fix the underlying interaction. State specific constraints when they matter, such as preserving the panel size or keeping saved activity in one location.

## What a good result should include

1. Inspection of the current implementation and affected UI states before edits.
2. A focused change that fixes the example and genuinely equivalent instances.
3. Clear hierarchy through grouping, weight, spacing, and concise copy; increasing every font size is not the default solution.
4. Verification appropriate to the change: rendered spacing, mobile layout, themes, keyboard access, and live/disclosure states where relevant.
5. A brief report of changes, evidence, and remaining uncertainty. Local, committed, pushed, and deployed are separate statuses.

The skills do not guarantee correctness or replace actual testing. A simulation can validate presentation without proving the real model, database, or memory service is connected.

## Background and design choices

### Couchbase Design

Created from repeated reviews of the AI savings calculator and Harborline demo. The intent is to feel at home on Couchbase’s website while keeping a demo simple enough to teach and present. The approximate “75% website / 25% custom craft” direction is a personal preference, not a compliance score.

The profile records website observations and John’s approved choices:

- Centra No2 Medium headings and Inter body text, with consistent sizes by role.
- Couchbase red actions, warm cream highlights, and neutral black/charcoal dark surfaces.
- Official-source logo geometry, a matching favicon, practical controls, clear outlines, and concise next actions.
- Activity that shows the current function, returned evidence, and a short decision explanation, with deeper detail available on demand.
- Stable live panels, useful internal scrolling, and restrained motion with reduced-motion support.

These are a personal reusable profile, **not an official Couchbase brand manual or verified company font package**. Proprietary fonts are not bundled. Use permitted project fonts and verify current website styles when exact parity is required. See [brand system](couchbase-design/references/brand-system.md), [agent demo guidance](couchbase-design/references/agent-demo-design.md), and [sources and provenance](couchbase-design/references/provenance.md).

Apple design principles informed hierarchy and familiar controls. Palette, Color System, Impeccable, frontend-design, and accessibility review informed feedback, semantic color, visual clarity, and verification. Their complete skills are not bundled or required; the useful principles are consolidated here. Source links and attribution are in the provenance reference.

### UI Pattern Repair

Created to address a recurring problem: fixing only the exact element mentioned while leaving the same defect elsewhere, or changing the whole layout to solve a small issue. It turns an example into a scoped audit of equivalent components.

The workflow emphasizes evidence, preserving the approved design, and checking multiple states. In the hotel demo this included crowded activity text, jumping panels, inconsistent dropdowns, lost scroll position, and disclosures that appeared blank. Those incidents inform diagnosis; they are not assumed to be the cause of every future bug.

## Install in Codex or Claude Code

Keep both skill folders side by side, including references and assets, because they link to each other.

| Agent | Personal installation location |
|---|---|
| Codex | `~/.codex/skills/couchbase-design/` and `~/.codex/skills/ui-pattern-repair/` |
| Claude Code | `~/.claude/skills/couchbase-design/` and `~/.claude/skills/ui-pattern-repair/` |

Clone this private repository, then copy the two folders to the agent’s skills directory. Inspect differences before replacing an existing installation. Start a new session after installation and ask the agent to read both skills to confirm availability. In Codex you can name `$couchbase-design` and `$ui-pattern-repair`; in either agent you can explicitly request both by name.

The `agents/openai.yaml` file is Codex-specific metadata. Shared instructions live in `SKILL.md` and linked references.

## Use in Claude web or desktop

Claude Code’s local installation is separate from cloud skill uploads. Package each skill folder as its own ZIP and upload through Claude’s custom skill settings, retaining `SKILL.md` at the skill folder root. Upload both and verify that the environment can read their supporting files and sibling references.

If that environment cannot resolve sibling references, supply both complete folders as project files and explicitly ask it to read both `SKILL.md` files and relevant references. A GitHub link alone does not guarantee the agent can access a private repository.

See [Anthropic’s skill documentation](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) for platform-specific availability and setup.

## Keep both agents up to date

This repository is the shared master copy. A push to GitHub does **not** automatically update Codex, Claude Code, or Claude cloud uploads.

1. Make durable instruction changes here, or bring intentional local skill edits back into this repository.
2. Review and commit the change, then push it to GitHub.
3. Pull the latest version on each machine and update the corresponding installed folders.
4. Re-upload changed ZIPs to cloud environments and confirm the agent reads the updated instructions.

Keep project-specific status, temporary workarounds, credentials, and deployment IDs in the project rather than turning them into universal skill rules. The user’s latest instructions take precedence over saved defaults.

## Boundaries

Neither skill grants permission to publish, change access, use paid resources, or push to somebody else’s repository. Preserve the user’s authorized scope and destination. Keep credentials and private project data out of skill packages. Couchbase marks remain Couchbase’s property; bundled assets do not establish a new license.
