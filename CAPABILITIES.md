# NIIRONA Capabilities

This document describes NIIRONA from a public capability perspective.

The labels distinguish implemented/demonstrated work, advanced integration work, and planned capabilities.

---

## Implemented / demonstrated

### Deterministic orchestration
A dedicated non-LLM control layer coordinates system actions.

### Separate chat and task paths
Conversation and explicit task execution use separate control paths.

### Explicit task activation
Ordinary conversation does not automatically become autonomous execution.

### Controlled integration spine
Subsystem integration is moving through controlled contracts rather than ad-hoc direct calls.

### Restart and long-session recovery
Long-running and restart scenarios have been exercised and validated.

### Execution evidence
Task attempts can preserve evidence for retry and review logic.

### Sandbox execution
Potentially unsafe or experimental work can execute through an isolated path.

### Test-aware execution
Validation is part of the execution lifecycle.

### Checkpoint / rollback direction
Known-good state can be preserved around risky changes and restored when necessary.

### Source / identity separation
User input, system signals, tool output, speech input, and synthesized output can be distinguished at the system level.

### Multi-provider LLM support
NIIRONA has been developed around both local and cloud model providers.

### Unity avatar client
A separate Unity application substantially implements the avatar-side experience, including bone discovery/mapping, rig handling, body/hand movement work, finger-control refinement, and graphical interaction.

---

## Advanced architecture / integration

### Orchestrator V2
The second-generation deterministic orchestrator has been implemented and is in advanced integration and validation.

### Advanced Context Manager
A dedicated subsystem maintains organized project context and supplies bounded, relevant context to reasoning models.

### Project Knowledge Graph
Structured project knowledge is kept separately from temporary prompt context.

### Confidence and uncertainty
Specialized components can express uncertainty without directly owning control flow.

### Hypothesis-driven investigation
The architecture supports evidence-gathering before committing to a first explanation.

### Failure learning
Failed attempts can become reusable evidence rather than disappearing as transient logs.

### CAN-only direction
The system is moving toward a single controlled subsystem-integration path with obsolete direct fallbacks removed.

---

## Next major capabilities

### LLM Runtime & Routing Manager
A dedicated model infrastructure subsystem will manage:

- model profiles;
- local and cloud providers;
- GPU mapping;
- process lifecycle;
- active-model state;
- health monitoring;
- controlled hot switching;
- explicit multi-model modes;
- future automatic model selection based on available hardware.

### Intent Gate
A universal intent classifier will sit between conversational input and deterministic control.

It will distinguish discussion from action and classify supported execution intents without relying on fragile magic phrases.

### Cloud-to-local teaching
A separate subsystem will coordinate controlled teacher/student workflows between stronger cloud models and local models.

---

## Autonomous engineering direction

NIIRONA is being designed to support increasingly autonomous software-engineering loops:

1. understand the requested change;
2. retrieve minimal relevant context;
3. form a candidate solution;
4. implement in isolation;
5. run targeted tests;
6. review evidence;
7. integrate;
8. observe behavior;
9. keep, repair, or roll back.

No single LLM call should own the entire lifecycle.

---

## Client and interaction direction

NIIRONA is designed to support:

- text chat;
- speech-to-text;
- text-to-speech;
- Windows graphical client;
- Unity avatar interaction;
- future mobile clients;
- visual runtime controls;
- voice-issued actions routed through the same intent/control protections as typed input.

---

## What NIIRONA is not

NIIRONA is not intended to be:

- a single-agent prompt framework;
- a thin LLM wrapper;
- a monolithic planner;
- a chatbot with unrestricted shell access;
- a single-provider cloud product.

Its design goal is a modular AI environment whose reasoning model and user interface can both be replaced without replacing the system.
