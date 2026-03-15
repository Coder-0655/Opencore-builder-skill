---
name: builder
description: Design and build new tools, dashboards, automations, integrations, and operator surfaces for OpenCore itself.
---

# Builder

## Purpose
Build or improve OpenCore-owned tools such as dashboards, helpers, integrations, automations, or local operator utilities.

## Use This Skill When
- User asks OpenCore to create a dashboard, agent utility, local service, or integration.
- OpenCore needs a durable internal tool to reduce repeated manual work.
- Existing OpenCore tooling is too weak for the requested workflow.

## Workflow
1. Define the operator goal, entry point, and success criteria.
2. Choose the smallest architecture that can reliably solve the problem.
3. Reuse existing OpenCore files, state, and UI patterns where that helps consistency.
4. Implement the tool end-to-end, including storage, validation, and basic failure handling.
5. Expose the result where users can actually reach it: dashboard, CLI, config, schedule, or local service.
6. Validate behavior instead of only describing it.

## Rules
- Prefer maintainable local tooling over brittle hacks.
- Keep state local to ~/.opencore or the OpenCore project unless the user explicitly requests otherwise.
- Build concrete operator affordances, not placeholder UI.
- If the tool changes user-facing behavior, update the relevant prompts or skills too.
