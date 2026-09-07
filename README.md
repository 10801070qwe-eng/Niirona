# NIIRONA

**NIIRONA is a local-first AI system built to keep the useful parts of an AI assistant — conversation, coding, tools, memory and reasoning — without making the whole system depend on one LLM.**

A model is only one replaceable part of NIIRONA. The surrounding system keeps the project context, execution history, recovery state and working process alive.

That means the user can start with a local model, use a cloud model when a harder task needs it, and later move to another model without rebuilding the whole AI environment.

> This repository describes what NIIRONA is intended to do without publishing the private implementation recipe.

## Why NIIRONA exists

A normal AI coding session can become inefficient very quickly. A long conversation accumulates irrelevant history. A model receives more context than it needs. Failed approaches are forgotten. Changing the model can mean rebuilding the session. A bad code change can damage a working project.

NIIRONA is being built around a different idea:

**the AI should keep the useful experience of the system outside the temporary mind of one model.**

## What this gives the user

### Use local AI without being trapped by one local model
NIIRONA is local-first. Local models can be used on your own hardware, while cloud models remain optional resources for tasks where extra capability is useful.

The long-term goal is not “choose one model forever.” The goal is to let the system use different reasoning engines while the surrounding working state remains intact.

### Change the brain, not the whole system
Model runtime work is being developed so a user can move from one LLM to another during operation — for example from a local Qwen model to a cloud model and later to another local model — without treating every switch as a new AI project.

Controlled hot switching is a major capability currently being integrated.

### Adaptive Context Intelligence — give the LLM what it actually needs
NIIRONA does not want to dump an entire project and an entire conversation into every request.

It maintains organized project knowledge and builds a smaller working context around the current problem. When more information is needed, context can be expanded deliberately.

This is useful in two ways:

- smaller local models receive a cleaner problem instead of unnecessary noise;
- cloud models can receive fewer unnecessary tokens, reducing avoidable inference cost.

### Improve the way context is selected
The context system is intended to do more than retrieve files.

NIIRONA can use the outcome of previous work as feedback: what information was selected, what turned out to be missing, what was unnecessary, and what later became important. That experience can be used to improve future context selection.

In other words, the model itself does not have to be retrained for NIIRONA to become better at **how it prepares a problem for the model**.

**The goal is not more context. It is the right context, at the right time, in the right amount — with the selection strategy improving from experience.**

→ [Read more about NIIRONA Adaptive Context Intelligence](ADAPTIVE_CONTEXT.md)

### Conversation and work are different things
A long chat should not automatically become the working memory of every coding task.

NIIRONA separates ordinary conversation from explicit task execution. You can discuss an idea for a long time, then explicitly start a task. The execution path receives the relevant working information rather than blindly treating the entire conversation as an instruction set.

The result of the task can return to the conversation, but conversation itself is not unrestricted execution.

### Failed work can become useful experience
When an approach fails, NIIRONA is designed to preserve useful evidence from that failure instead of simply forgetting the attempt.

The goal is simple: do not keep paying the model to rediscover the same bad solution.

### Test before trusting
Experimental changes can be isolated, executed and tested before they are accepted.

The engineering direction is:

**understand → prepare context → change in isolation → test → inspect evidence → integrate → observe → keep, repair or roll back**

### Recover instead of starting from zero
Restart recovery and long-session behavior are first-class concerns.

NIIRONA has already been validated across restart and long-session scenarios. Risky work can be associated with known-good state so a failed change can be reversed instead of leaving the project in an unknown condition.
### Deterministic orchestration instead of LLM-controlled execution

NIIRONA keeps system control outside the reasoning model. The LLM can analyze, propose and reason, but deterministic orchestration owns execution flow.

Orchestrator V2 is being developed as a deliberately minimal coordination layer. Complex behavior is divided into independent modules, while the orchestrator coordinates their signals rather than becoming another intelligent monolith.

The architecture is designed around explicit state, acknowledgements, restart recovery and failure isolation so that individual components can be restarted or replaced without turning the LLM into the control authority.

→ [Read more about NIIRONA Orchestrator V2](ORCHESTRATOR_V2.md)
### Grow new capabilities safely
The longer-term autonomous engineering direction is that a user should be able to request a capability the system does not yet have.

For example: “I want NIIRONA to understand a photo sent from my phone.”

Rather than blindly modifying itself, the intended workflow is to create the capability in isolation, test it, inspect the result, integrate it only after validation, and roll back if the new behavior causes problems. Evidence from failure should inform the next attempt.

This controlled self-extension is a development direction, not a claim that every arbitrary capability can already be created autonomously today.

## More than a chat window

NIIRONA is being developed for text, voice, desktop and future mobile interaction. A separate Unity client with an interactive avatar is already substantially implemented and is being refined.

The avatar is a client, not the AI core. NIIRONA can operate without it.

## Current state

As of September 2026, the modular core, controlled task execution, local/cloud model support, restart/long-session behavior, sandbox/test workflows and separate chat/task paths have substantial implementation and validation.

Model hot switching, broader runtime management, safer autonomous self-extension, cloud-to-local teaching and final client integration are ongoing development areas.

## Public repository

This repository is a public overview, not a production source release. It intentionally explains the capabilities and design goals while withholding internal contracts, routing rules, recovery protocols, context-selection formulas, private prompts, security internals and production source code.

See:

- [Capabilities](CAPABILITIES.md)
- [Adaptive Context Intelligence](ADAPTIVE_CONTEXT.md)
- [Architecture Vision — Why NIIRONA is built this way](NIIRONA_ARCHITECTURE_VISION_RU_PUBLIC.md)
- [Deterministic Orchestrator V2](ORCHESTRATOR_V2.md)
- [Architecture — public view](ARCHITECTURE.md)
- [Current status](STATUS.md)
- [Roadmap](ROADMAP.md)
- [Russian overview](README_RU.md)
- [Public disclosure policy](PUBLIC_DISCLOSURE.md)
- [Source availability notice](LICENSE-NOTICE.md)
---

## Unity Avatar Client

NIIRONA includes an interactive Unity-based avatar client that provides a visual interface for interaction with the system.

### Interactive interface

![NIIRONA Unity Avatar Interface](Снимок%20экрана%20(726).png)

### Avatar rig and skeleton tools

NIIRONA includes custom Unity tooling for avatar analysis, humanoid skeleton detection, finger-bone mapping, rig construction, and avatar control.

![NIIRONA Avatar Rig Tools](Снимок%20экрана%20(729).png)

### Development view

![NIIRONA Avatar Development](Снимок%20экрана%20(728).png)
