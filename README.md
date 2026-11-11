# Couchbase design skills

Shared instructions for building and refining the interfaces in our demo library.

[Open the demo library](https://couchbase-demo-library.vercel.app/) · [Detailed guide](README-REFERENCE.md)

![Couchbase Internal Demo Library](docs/images/demo-library.png)

## What it helps with

- **Couchbase Design** sets the fonts, colors, controls, and layout patterns.
- **UI Pattern Repair** takes one UI problem and checks matching components for the same issue.
- Use both when improving an existing Couchbase interface.

<a id="install-in-codex-or-claude-code"></a>

## Start here

Copy `couchbase-design/` and `ui-pattern-repair/` together into `~/.codex/skills/` or `~/.claude/skills/`. Keep their references and assets.

Start a new session and ask your agent to read the skill. For cloud uploads, package each complete skill folder as a ZIP. Installation details and environment limits are in the [detailed guide](README-REFERENCE.md).

Try this request:

> Use couchbase-design and ui-pattern-repair. Fix the crowded dropdowns across this demo, keep the approved styling, and check phone and desktop layouts.

## How it works

These files guide the coding agent. They do not connect services, start paid resources, or grant access on their own. The agent still needs your project, tools, and permission for the work.

Use the [design skills](https://github.com/john-couchbase/agent-skills) for interfaces and the [setup skill](https://github.com/john-couchbase/couchbase-aidp-setup) for backend connections.

## Updates and feedback

- Pull the latest repository before copying skills to another machine.
- Update installed folders and cloud ZIPs after changes. A GitHub push does not update them automatically.
- Report the skill name, your request, and the result that needs improving.

The [detailed guide](README-REFERENCE.md) preserves background, boundaries, and supporting references. These are practical project skills, not an official Couchbase brand manual or support package.
