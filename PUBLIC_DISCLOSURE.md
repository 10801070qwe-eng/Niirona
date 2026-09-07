# Public Disclosure Policy

NIIRONA's public documentation is intentionally informative but non-reproducible.

The project can disclose **what the system does**, **which responsibilities are separated**, and **which major components exist**, while withholding details required to reconstruct the production system.

---

## Safe to publish

Examples:

- NIIRONA is local-first.
- It uses deterministic orchestration.
- Chat and autonomous execution are separate.
- Context management is separated from control.
- LLMs are replaceable runtime resources.
- The system uses isolated execution and rollback.
- Restart recovery is a first-class design requirement.
- Multiple local/cloud models are supported architecturally.
- A dedicated model-runtime manager is planned.
- A teaching subsystem can coordinate cloud and local models.
- The Unity avatar exists as a separate client application.
- The client can discover/map avatar bones and manage rig/pose behavior.
- State, context, testing, confidence, and execution have dedicated responsibilities.

---

## Do not publish

Avoid publishing:

- exact internal message schemas;
- internal capability contracts;
- routing tables;
- private module identifiers where unnecessary;
- state-machine definitions;
- retry counts and timing thresholds;
- recovery ordering;
- acknowledgement/barrier implementation details;
- exact subsystem dependency graphs;
- private prompts;
- internal scoring/ranking formulas;
- context-selection formulas;
- sandbox security boundaries;
- security enforcement rules;
- model-launch command templates;
- production configuration files;
- source directory topology;
- private test fixtures that reveal protocols;
- sensitive deployment information.

---

## Screenshots

Screenshots are useful, but they should be reviewed before publication.

Safe screenshots should avoid exposing:

- API keys or tokens;
- account identifiers;
- private repository names;
- local usernames or home paths;
- private IP addresses;
- internal ports when unnecessary;
- production logs containing sensitive data;
- source code that reveals private implementation details.

Good public screenshots include:

- the avatar/client UI;
- a clean Unity client view;
- a high-level system dashboard mockup;
- non-sensitive visual interaction states.

---

## Diagrams

Public diagrams should show:

- layers;
- direction of control;
- separation of responsibilities;
- local/cloud model replaceability;
- conversation vs execution separation;
- client/core separation.

Public diagrams should not show:

- protocol fields;
- exact failure sequencing;
- private command maps;
- privileged interfaces;
- exact internal state transitions.

---

## Recommended public positioning

> **NIIRONA is a modular, local-first AI system with deterministic control, isolated execution, dedicated context management, restart recovery, replaceable local/cloud reasoning models, and a separate interactive Unity/avatar client.**

This communicates the engineering direction without revealing the implementation recipe.
