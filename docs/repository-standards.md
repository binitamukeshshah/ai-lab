# Product repository standards

These are defaults for substantial AI Lab product repositories. Use judgment for smaller research artifacts, but do not omit evidence or security because a project is early.

## Recommended structure

```text
product-name/
├── README.md
├── AGENTS.md
├── CHANGELOG.md
├── LICENSE
├── .env.example
├── docs/
│   ├── architecture.md
│   ├── decisions.md
│   ├── deployment.md
│   ├── evaluation.md
│   ├── roadmap.md
│   └── security.md
├── src/
├── tests/
├── deploy/                    only when the product owns deployment assets
└── assets/                    reviewed demos and supporting media
```

Adapt language-specific manifests and tooling without weakening the responsibility boundaries.

Commit a sanitized `.env.example` in each product repository when runtime configuration is required. It should list supported variable names with safe, non-secret example values and brief guidance. Ignore `.env` and other real environment files; inject production secrets through the runtime's approved secret-management mechanism. The `ai-lab` documentation repository does not need an `.env.example` because it has no runtime configuration.

## README template

1. Product name and one-sentence positioning.
2. User problem and product hypothesis.
3. Product principles.
4. Architecture diagram and component responsibilities.
5. What works today.
6. Evaluation evidence and limitations.
7. Quick start.
8. Roadmap and documentation links.

## Documentation template

- **Architecture:** components, data flow, ownership, contracts, and failure boundaries.
- **Decisions:** important choices, context, alternatives, and consequences.
- **Deployment:** environments, configuration, secrets, health, persistence, and rollback.
- **Evaluation:** cases, metrics, evidence, methodology, and limitations.
- **Roadmap:** current status, next product questions, and deferred scope.
- **Security:** identity, authorization, privacy, threat boundaries, logging, and recovery.

## Demo requirements

- Demonstrate the core product value with real, reproducible behavior.
- Record versions and relevant environment assumptions.
- Keep the scenario short and legible.
- Explain what the evidence supports.
- Review every frame and output for private information.

## Testing requirements

- Unit tests for domain behavior and validation.
- Contract tests for external boundaries.
- Integration tests for critical service paths, explicitly opt-in when live dependencies are required.
- Failure-mode tests for timeouts, unavailable dependencies, malformed responses, and partial state.
- Security tests for authorization, privacy propagation, redaction, replay/idempotency, and dangerous operations.
- CI must run formatting/linting, type checks where supported, and non-live tests.

## Architecture diagram expectations

- Show only relationships needed to understand the product.
- Label ownership and trust boundaries.
- Distinguish current behavior from proposed behavior.
- Avoid vendor logos when a functional label communicates the design more clearly.

## Product decision log

Record decisions that are durable, expensive to reverse, security-sensitive, or easy to misunderstand. Each entry should include context, decision, alternatives, consequences, date, and status. Product decisions stay in the product repository; ecosystem decisions belong in `ai-lab`.

## Changelog

Maintain a human-readable changelog for shipped behavior. Describe user-visible capability, architecture, security, or compatibility changes. Do not use it as a raw commit list.

## Security checklist

- [ ] Secrets and private data are excluded from Git and demos.
- [ ] Authentication uses stable identities; authorization denies by default.
- [ ] Service-to-service traffic is private and authenticated.
- [ ] Inputs, sizes, timeouts, and retries are bounded.
- [ ] Destructive actions are narrow, confirmed, and auditable.
- [ ] No user or model input becomes arbitrary shell execution.
- [ ] Logs redact prompts, memory, credentials, identity data, and raw diagnostics.
- [ ] Stored user data has isolation, retention, export, correction, and deletion rules.
- [ ] Services run with least privilege.
- [ ] Backups and restoration are tested where data is durable.
