# GitHub portfolio strategy

## Portfolio objective

The GitHub portfolio should make Binita's AI Product Management judgment visible: problem selection, prioritization, architectural boundaries, risk management, evaluation, delivery, and honest learning.

## Why separate repositories

Each substantial product should have one clear user, problem, hypothesis, architecture, evidence set, and roadmap. Separate repositories prevent the master Lab narrative from becoming a monolith and let a reviewer understand one product without navigating unrelated code.

`ai-lab` connects those stories. It does not absorb their implementations.

## How each repository tells a product story

Every product homepage should make the following clear within the first screen:

- the problem and intended user;
- the product hypothesis;
- current status and demonstrated behavior;
- the key architectural decision;
- a credible demo or evidence link;
- important limitations;
- the next product question.

## README standards

- Lead with the product outcome, not installation commands.
- Use a one-sentence positioning statement and a concise problem explanation.
- Include one useful architecture diagram.
- Separate what works today from future scope.
- Link evaluation, deployment, security, decisions, roadmap, and changelog.
- Keep setup reproducible and never expose private infrastructure details.

## Demo standards

- Use real output from a versioned, documented environment.
- Make the scenario understandable to a non-specialist reviewer.
- Show the differentiating decision or workflow, not routine setup.
- State what the demo proves and what it does not prove.
- Remove secrets, identity data, hostnames, network addresses, and private paths.
- Never fabricate, splice, or simulate evaluation evidence.

## Architecture diagram standards

- Use the smallest diagram that explains ownership and data flow.
- Name boundaries by responsibility rather than framework alone.
- Distinguish selection, orchestration, execution, tools, memory, and storage.
- Keep diagrams synchronized with actual behavior.

## PM interview narrative

For each project, be prepared to explain:

1. **Context:** What user or market problem mattered?
2. **Choice:** Which risk was prioritized, and what was deliberately deferred?
3. **Design:** How did architecture support the product principles?
4. **Evidence:** What was tested, and how strong is the evidence?
5. **Learning:** What changed because of the result?
6. **Next step:** What investment is justified now—and what is not?

The strongest narrative connects a working artifact to a disciplined product decision.
