# NIIRONA Capabilities

This page focuses on **what NIIRONA can do for a user**, rather than listing its private internal modules.

## Available / demonstrated foundations

### Local-first AI
NIIRONA is designed to run on user-controlled hardware and has been developed with local LLMs as real runtime targets.

### Local and cloud reasoning
The system is not tied to one provider. Local and cloud models can both participate in the NIIRONA environment.

### Separate conversation and task execution
Conversation does not automatically become privileged execution. Explicit tasks follow a separate controlled path, so a long chat does not need to be blindly replayed as the working context for every task.

### Project-aware context
NIIRONA can build a bounded working context around a task instead of treating the entire project as one prompt.

### Isolated execution and testing
Experimental work can run through an isolated path and validation can be part of the execution lifecycle.

### Failure evidence
Failed attempts can leave reusable evidence. The goal is to reduce repeated bad approaches and make future attempts better informed.

### Checkpoints and rollback
Known-good state can be preserved around risky changes so failed work can be reversed.

### Restart and long-session recovery
Long-running sessions and restart scenarios have been exercised and validated.

### Explicit task activation
Talking about a change is not the same as authorizing the system to make the change.

### Interactive client work
A separate Unity client with an avatar is substantially implemented and continues to be refined.

## Advanced / integration capabilities

### Adaptive context delivery
NIIRONA's context direction is not only “find relevant files.”

The system is intended to evaluate its own context choices over time: what it selected, what later proved necessary, what was missing and what was unnecessary. That feedback can improve how future tasks are prepared for an LLM.

This can make a local model more effective by reducing noise and can reduce unnecessary cloud-token usage.

### Model independence
Project knowledge, task state and execution history are designed to live outside any single LLM session. This makes the reasoning model replaceable without replacing the whole AI environment.

### Controlled model hot switching
Runtime work is being integrated to support switching between registered local and cloud models during operation while preserving the surrounding NIIRONA state.

### Resilient execution
NIIRONA is being built to treat interruptions and failures as recoverable events rather than reasons to abandon the whole session.

## Development direction

### Controlled self-extension
The target workflow for a requested new capability is:

1. understand the requested behavior;
2. retrieve only the relevant context;
3. build the change in isolation;
4. run targeted tests;
5. inspect evidence;
6. repair if necessary;
7. integrate only after validation;
8. observe the result;
9. keep it or roll back;
10. use failure evidence to inform another attempt.

This is an engineering direction under active development, not a claim of unrestricted autonomous self-modification today.

### Cloud-to-local teaching
A future controlled workflow is intended to let a stronger cloud model help a local model learn narrow, testable behaviors.

### Hardware-aware model selection
Future runtime management is intended to help choose suitable models for available GPU/VRAM resources.

### Broader interfaces
Voice, desktop, mobile and avatar interfaces are intended to remain replaceable surfaces over the same core system.

## Why these capabilities belong together

NIIRONA's goal is not simply to make an LLM call more tools.

The goal is to build a persistent AI environment where:

- the reasoning model can change;
- useful project knowledge survives the model;
- tasks receive focused context;
- context selection can improve from experience;
- conversation stays separate from execution;
- failures can become evidence;
- risky changes are tested;
- bad changes can be rolled back;
- interrupted work can recover;
- new capabilities can eventually be added through a controlled engineering process.

That is the capability layer NIIRONA is being built toward.
