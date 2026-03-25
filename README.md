# Skills Workflow

This repository documents a project-planning and implementation workflow inspired by [mattpocock/skills](https://github.com/mattpocock/skills). Full credit for the original method goes to Matt Pocock.

## The flow

1. Start with `grill-me`

   Use `grill-me` to pressure-test either:

   - a totally new project idea, or
   - a new feature for an existing product.

   The goal is to discuss the idea deeply before writing anything formal.

2. Move to `write-a-prd`

   Once the idea is clear, use `write-a-prd` to turn that discussion into a PRD and submit it as a GitHub issue.

   Compared to Matt's original approach, we do not center the workflow around tests or TDD. We intentionally avoid making the PRD opinionated about test strategy. The PRD stays focused on product value, scope, behavior, constraints, and open questions.

3. Run `prd-to-issues`

   After the PRD is ready, `prd-to-issues` breaks it into implementation issues.

   This is where our approach diverges again: we do not keep the tracer-bullet concept from the original repository. Instead, each issue should represent a full, meaningful feature slice. Backend and frontend are separated into different issues so they can be implemented by different agents.

4. Use `start-next-issue`

   Matt's original flow uses an agent that can fetch issues and implement them in order automatically. Here, `start-next-issue` adds another focused grilling step before coding starts.

   This second discussion is feature-specific and more technical. It helps clarify architecture, trade-offs, interfaces, and implementation details before work begins. We have found this especially useful when building the foundations of a new project.

5. Launch `start-implementation`

   Once the issue has been discussed thoroughly, run `start-implementation` to execute it through to completion.

## Why we changed the method

- We do not want the workflow to be opinionated around TDD.
- We want PRDs to stay product-focused rather than test-focused.
- We prefer full-feature issues over tracer bullets.
- We split backend and frontend issues so different specialized agents can implement them independently.
- We reintroduce grilling at the issue level because it improves technical clarity before implementation.

Matt Pocock's original method is excellent for adding new features. Our adaptation is aimed more at starting new projects cleanly and building stronger foundations early.

See also: https://x.com/sones3_/status/2035723909513785408?s=20

## Supporting skills

- `discuss-in-french`: lets you run the discussion in French while keeping deliverables in English (comes after `start-next-issue`).
- `discuss-in-{language}`: you can create your own variants for other languages using the same idea.
- `ubiquitous-language`: keeps a shared domain vocabulary between you and the agent, again inspired by Matt Pocock's work.

## Recommended sequence

`grill-me` -> `write-a-prd` -> `prd-to-issues` -> `start-next-issue` -> `start-implementation`

Don't hesitate to contribute!