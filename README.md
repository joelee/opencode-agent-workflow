# OpenCode agent workflow template

Copy `opencode.jsonc`, `.opencode/agents/*.md`, and the appropriate `AGENTS.*.md` template into a project root.

## Included files

Agent files:
- `.opencode/agents/brainstorm.md`: research and ideation; appends durable notes to `docs/discovery-notes.md`.
- `.opencode/agents/design.md`: docs-only architecture/design authoring; maintains `docs/directory-structure.md`.
- `.opencode/agents/plan.md`: overrides the default Plan agent with backlog, plan, and approval-gated documentation commits.
- `.opencode/agents/build.md`: overrides the default Build agent with strict TDD delivery workflow.
- `.opencode/agents/validate.md`: independent quality/security validation and done marking.
- `.opencode/agents/release.md`: SemVer version bump, changelog, and release note preparation.

Instruction templates:
- `AGENTS.python-uv-ruff.md`: Python project rules for `uv`, `ruff`, pytest coverage, containers, config, docs, and releases.
- `AGENTS.rust-cargo-rustfmt.md`: Rust project rules for `cargo`, `rustfmt`, `clippy`, coverage, containers, config, docs, and releases.

Included docs:
- `docs/discovery-notes.md`: durable ideation/research log maintained by Brainstorm.
- `docs/directory-structure.md`: canonical project directory map maintained by Design.
- `docs/plans/`: active feature plans.
- `docs/plans/done/`: validated feature plans.
- `docs/release/`: release notes.

## Install

From this package directory, copy the workflow files into your project root:

```bash
cp opencode.jsonc /path/to/project/
cp -R .opencode /path/to/project/
cp -R docs /path/to/project/
cp AGENTS.python-uv-ruff.md AGENTS.rust-cargo-rustfmt.md /path/to/project/
```

Then choose the project instruction template and rename it to `AGENTS.md`:

Python:

```bash
cp AGENTS.python-uv-ruff.md AGENTS.md
```

Rust:

```bash
cp AGENTS.rust-cargo-rustfmt.md AGENTS.md
```

Keep the original `AGENTS.*.md` files as reusable templates, or remove the unused one after choosing.

## Suggested workflow

1. `brainstorm`: explore options and append reusable notes to `docs/discovery-notes.md`.
2. `design`: document architecture, configuration, usage, developer workflow, and directory structure.
3. `plan`: convert designs into backlog entries and feature plans, then optionally commit docs/planning artifacts after user approval.
4. `build`: start from a clean repo, create the feature branch, implement through TDD, integration tests, coverage, and docs.
5. `validate`: independently verify quality/security and move accepted plans to `docs/plans/done/`.
6. `release`: bump the version, finalize `CHANGELOG.md`, and create release notes.

Use `Tab` in the OpenCode TUI to switch primary agents, or call a specific primary agent from CLI/GitHub configuration where supported.
