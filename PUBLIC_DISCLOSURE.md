# NIIRONA Public Disclosure Policy

NIIRONA's public documentation follows one simple rule:

> **Explain what the system can do and why it matters. Do not publish the private recipe required to reproduce it.**

## Safe public capability claims

Public material may explain that NIIRONA:

- is local-first;
- can work with local and cloud LLMs;
- is designed so the reasoning model is replaceable;
- separates ordinary conversation from explicit task execution;
- prepares bounded task-specific context;
- is being developed to improve context selection using previous outcomes;
- can reduce unnecessary context sent to cloud models;
- uses controlled execution and testing;
- preserves useful evidence from failed attempts;
- supports checkpoint/rollback workflows;
- treats restart recovery as a first-class requirement;
- is being developed for controlled model hot switching;
- is being developed toward controlled self-extension;
- has a separate Unity/avatar client;
- is intended to support voice, desktop and future mobile interfaces.

## Status must remain clear

Public documentation must distinguish:

- capabilities already implemented or demonstrated;
- capabilities in advanced integration;
- development targets and long-term direction.

A planned capability must never be presented as fully available.

## Private implementation details

Do not publish information that turns the overview into a reconstruction guide, including:

- production source code;
- exact message schemas;
- internal capability contracts;
- private module identifiers where unnecessary;
- routing tables;
- state-machine definitions;
- retry counts and timing thresholds;
- recovery ordering;
- acknowledgement/barrier mechanics;
- exact dependency graphs;
- private prompts;
- context-selection formulas or ranking weights;
- failure-learning formulas;
- sandbox security boundaries;
- privileged-action enforcement rules;
- production model-launch commands;
- private configuration;
- sensitive deployment information;
- private test fixtures that expose protocols.

## Screenshots

Public screenshots should be cleaned of:

- API keys and tokens;
- account identifiers;
- local usernames and private paths;
- private IP addresses;
- unnecessary internal ports;
- sensitive logs;
- private source code.

Good public visuals include the avatar, client UI, high-level interaction states and non-sensitive demonstrations.

## Positioning

A useful short description is:

**NIIRONA is a local-first AI environment that keeps context, execution, recovery and learning around the model, allowing local and cloud LLMs to act as replaceable reasoning engines rather than becoming the whole system.**

A useful longer description should focus on user outcomes: focused context, lower unnecessary token use, separate chat and execution, failure learning, testing, rollback, restart recovery and controlled evolution.
