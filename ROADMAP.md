# NIIRONA Public Roadmap

This roadmap describes user-visible capability direction. Exact private milestones, protocols and implementation details are intentionally omitted.

## 1 — Reliable persistent AI foundation
**Status: largely implemented / advanced validation**

Goals:

- keep conversation separate from explicit execution;
- preserve useful task state;
- support long sessions;
- recover after restart;
- isolate risky work;
- test changes;
- preserve known-good states;
- roll back failed changes;
- retain useful failure evidence.

## 2 — Smarter context
**Status: implemented foundation, continuing development**

Goals:

- give each task only the context it needs;
- expand context when evidence shows something is missing;
- avoid repeatedly sending irrelevant project history;
- learn from previous context-selection outcomes;
- improve how tasks are prepared for both local and cloud LLMs;
- reduce unnecessary cloud-token use.

## 3 — Replaceable models and live runtime management
**Status: major active/next infrastructure work**

Goals:

- register multiple local and cloud models;
- manage local model lifecycle;
- map models to available GPU resources;
- track active model state and health;
- switch models in a controlled way during operation;
- support explicit multi-model modes;
- later recommend/select suitable models for available hardware.

## 4 — Controlled self-extension
**Status: development direction**

Goal: allow NIIRONA to build a requested new capability without blindly changing the working system.

Target cycle:

**request → isolate → build → test → inspect → repair → integrate → observe → keep or roll back**

Failure evidence should inform the next attempt.

## 5 — Cloud helping local
**Status: designed / future subsystem**

A stronger cloud model should be able to teach a local model narrow behaviors through controlled tasks, tests and evaluation rather than uncontrolled prompt imitation.

## 6 — Human interfaces
**Status: Unity client substantially implemented; broader integration ongoing**

Goals:

- text chat;
- speech input/output;
- Windows client;
- interactive Unity avatar;
- mobile interface;
- visual model/hardware controls;
- replaceable future clients.

## Long-term direction

NIIRONA is moving toward an AI environment that becomes less dependent on any single model over time.

The system should preserve its useful working knowledge, improve how it prepares context, recover from failures, control risky changes and let the user choose when local or cloud intelligence is worth using.
