# John’s agent skills

Shared master copies for Codex and Claude. These are personal design instructions, not an official Couchbase brand manual.

- **couchbase-design**: approved typography, colors, assets, responsive layouts, and demo presentation.
- **ui-pattern-repair**: diagnose an example, repair equivalent UI patterns, and verify affected states without changing the approved design.

Keep both folders together: they reference each other. Supporting references and assets are part of the skills. Proprietary font files and credentials are not included.

## Codex and Claude Code

Clone this private repository, then copy both skill folders into the agent’s personal skills directory:

- Codex: `~/.codex/skills/`
- Claude Code: `~/.claude/skills/`

Inspect differences before replacing an existing installed skill. Reload/start a new agent session after installation. A GitHub push does not automatically update installed copies; pull the repository and copy the changed folders to each agent. Bring intentional local edits back into this repository before committing so it remains the master copy.

## Claude web/desktop

Upload each skill folder as its own ZIP through Claude’s custom skill settings, retaining SKILL.md at the skill folder root. Install both because the instructions reference their sibling skill. Cloud uploads are separate from Claude Code’s local installation; verify both are available in that environment. If the environment cannot resolve sibling references, supply both folders as project files and explicitly ask it to read both SKILL.md files and relevant references.

## Use

“Use couchbase-design and ui-pattern-repair. Treat this UI issue as an example, inspect matching components, preserve the approved design, and verify the affected states.”

## Sources

Claude skill format and installation: https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview

The `agents/openai.yaml` file is Codex-specific metadata; shared instructions live in SKILL.md and references. Neither skill authorizes publishing, paid resources, credentials, or access changes.
