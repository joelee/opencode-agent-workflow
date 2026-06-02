# Directory Structure

Canonical project directory map maintained by the Design agent.

Update this file whenever project directories, package boundaries, config locations, container files, docs, tests, scripts, or release artifacts are added, removed, or reorganized.

## Current structure

```text
.
├── AGENTS.md                         # Active agent/project instructions; copied from the chosen AGENTS.*.md template.
├── AGENTS.python-uv-ruff.md          # Python/uv/Ruff instruction template.
├── AGENTS.rust-cargo-rustfmt.md      # Rust/cargo/rustfmt instruction template.
├── opencode.jsonc                    # Project OpenCode configuration.
├── .opencode/agents/                 # OpenCode role agents for the delivery workflow.
└── docs/                             # Project documentation and delivery records.
    ├── discovery-notes.md            # Brainstorm research and ideation log.
    ├── directory-structure.md        # Canonical project map.
    ├── plans/                        # Active feature plans.
    │   └── done/                     # Validated feature plans.
    └── release/                      # Release notes.
```
