# Ecosystem decision index

This directory records durable decisions that affect more than one AI Lab product. Product-specific decisions belong in the repository that owns the behavior.

## Decision record format

Use one Markdown file per decision:

```text
NNNN-short-decision-title.md
```

Each record should contain:

- **Status:** proposed, accepted, superseded, or deprecated
- **Date**
- **Context**
- **Decision**
- **Alternatives considered**
- **Consequences**
- **Affected repositories**

## Accepted foundations

The following foundations are currently documented in [`PROJECT_CONTEXT.md`](../../PROJECT_CONTEXT.md) and should become individual records when their trade-offs need deeper history:

1. `ai-lab` is documentation-only; products remain separate repositories.
2. The MacBook is the development environment and a GPU workstation is the finished runtime.
3. OpenClaw owns conversations, orchestration, credentials, and execution.
4. AI Decision Engine is the single model-selection authority.
5. Telegram and future channels remain interface layers.
6. Tools are explicit and deny arbitrary shell execution.
7. Memory is consent-based, user-scoped, attributable, correctable, and deletable.
