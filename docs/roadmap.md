# Master roadmap

Status describes demonstrated progress, not ambition. A repository or configuration alone does not make a capability complete.

| Workstream | Status | Current evidence | Next decision or outcome |
|---|---|---|---|
| **AI Lab Core** | In Progress | Master repository structure, platform boundaries, and documentation standards established | Publish repository links and begin a cross-product decision log |
| **AI Decision Engine** | Completed | v0.1.0 shipped with local-first privacy, OpenClaw readiness, explainable selection, and tests | Preserve as standalone router; add a supported selection service only when an integration requires it |
| **Telegram AI Assistant** | In Progress | Product role and end-state architecture defined | Confirm OpenClaw Telegram channel and router contract; then build the first secure routed-chat slice |
| **Google Workspace Assistant** | Next | Product direction identified | Select one high-value Calendar, Gmail, or Drive workflow and define consent boundaries |
| **Family AI** | Next | Product direction identified | Define users, privacy model, shared versus personal memory, and a narrow first workflow |
| **Content Studio** | Next | Product direction identified | Choose a measurable research-to-content workflow and quality evaluation |
| **Forge** | Completed | Prototype demonstrates structured AI-assisted product building | Document transferable lessons and decide whether another validated use case warrants iteration |
| **AI Interview Coach** | Next | Product direction identified | Define target role, coaching loop, feedback rubric, and progress evidence |

## Completed

- Established the MacBook development and GPU-workstation runtime model.
- Installed the core self-hosted stack: Docker, OpenClaw, Ollama, and local model families.
- Shipped AI Decision Engine v0.1.0 as an independent repository.
- Completed the Forge prototype.

## In progress

- Establishing `ai-lab` as the portfolio homepage and architectural source of truth.
- Defining Telegram AI Assistant boundaries, contracts, security posture, and repository plan.

## Blocked

No workstream is formally blocked. The Telegram implementation intentionally waits for decisions about the deployed OpenClaw channel, the router's supported service boundary, tool ownership, memory policy, and runtime ingress. These are sequencing decisions, not permission to add temporary integrations.

## Next

1. Publish and link the master and completed product repositories.
2. Create a clean standalone `telegram-assistant` repository.
3. Verify the installed OpenClaw Telegram and plugin capabilities.
4. Define a versioned selection-only contract between OpenClaw and the AI Decision Engine.
5. Deliver authenticated Telegram-to-OpenClaw chat using a local model.
6. Add cloud routing only with explicit permission and end-to-end privacy tests.
7. Add ideas, todos, approved system operations, and memory as separate validated increments.

## Roadmap discipline

- Keep only one primary build workstream active at a time.
- Promote a capability to Completed only with tested behavior and documented evidence.
- Record changes in priority with their product rationale.
- Reassess later products using what the active workstream teaches.
