# Instructions for coding agents

## Start here

1. Read `PROJECT_CONTEXT.md` completely before proposing or making changes.
2. If `PROJECT_CONTEXT.private.md` exists locally and the task involves this environment, read it after the public context. Never quote or publish its operational details.
3. Read `README.md` and the documents relevant to the task.
4. Inspect existing files and linked product repositories before recommending new work.

## Repository boundary

- This is the documentation-only master repository for Binita AI Lab.
- Do not add production code, runtime services, deployment assets, product-specific configuration, or generated application scaffolding.
- Keep product implementations in separate repositories such as `ai-decision-engine`, `telegram-assistant`, and `forge`.
- Keep shared infrastructure separate from product-specific code. Document cross-repository contracts here; implement them in their owning repositories.

## Working principles

- Prefer modular, cohesive, production-quality designs over temporary scripts or demo shortcuts.
- Avoid vendor lock-in, duplicated functionality, speculative abstraction, and hidden cross-repository coupling.
- Reuse an existing capability through an explicit contract before proposing another implementation.
- Think long term, but make the smallest change that completely addresses the current need.
- Optimize public artifacts for credible GitHub portfolio quality: clear problem, deliberate decisions, real evidence, and honest limitations.
- Remember that Binita is an AI Product Manager, not an ML engineer. Explain non-obvious commands and architecture choices concisely without diluting technical accuracy.

## Safety and quality

- Never commit `PROJECT_CONTEXT.private.md`, secrets, credentials, tokens, private prompts, personal data, private host details, or fabricated evidence.
- Do not claim that a system works because it is configured; distinguish planned, implemented, tested, and live-validated states.
- Keep documentation synchronized when architecture, behavior, ownership, status, or priorities change.
- Preserve clear responsibility boundaries between interfaces, OpenClaw, routing, tools, memory, models, and infrastructure.
- Develop on the MacBook. Deploy only finished, reviewed, reproducible services from their product repositories to the GPU workstation.

## Documentation changes

- Keep documents concise and durable; avoid copying transient chat history.
- Put ecosystem-wide decisions in `docs/decisions/` and product-specific decisions in the relevant product repository.
- Update the master roadmap when a workstream changes status.
- Update `PROJECT_CONTEXT.md` only when the Lab's source-of-truth context changes.
- Verify links, headings, status language, and diagrams before handoff.
