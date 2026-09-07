# NIIRONA — Public Architecture View

This document deliberately describes **behavioral boundaries**, not the production implementation.

The private architecture, message contracts, routing rules, recovery sequences, context-selection algorithms and security boundaries are not published.

## The public idea

NIIRONA separates things that are often collapsed into one AI-agent loop.

A reasoning model can think about a problem, but it does not need to own the project's durable knowledge, the user's entire conversation, system recovery, code execution or the final decision to make a change.

From a user's point of view, this creates several useful boundaries.

## Conversation is not execution

A user can talk with NIIRONA without every sentence becoming an executable instruction.

When an explicit task is started, the working process is separated from ordinary conversation. The task can receive the information relevant to that work instead of blindly inheriting every old chat message.

When the task finishes, its result can return to the conversation.

## Context is not the model

Project knowledge can remain organized outside a single LLM prompt.

For a task, NIIRONA can prepare a bounded working set and expand it when evidence shows that more information is required.

The longer-term adaptive direction is to use previous task outcomes to improve future context preparation.

## The model is replaceable

NIIRONA is designed around local and cloud LLMs as replaceable reasoning resources.

The surrounding environment owns the continuity of the project. Runtime work is being integrated so registered models can be switched during operation without treating the switch as a complete reset of NIIRONA.

## Execution is not trust

A generated code change is not automatically considered correct.

Risky or experimental work can be isolated. Tests and execution evidence can be examined before a change is kept.

## Failure is not necessarily the end

The system direction includes known-good checkpoints, rollback, persistent state and restart recovery.

A failed attempt can also become useful evidence for another attempt.

## Self-extension is controlled

NIIRONA is being developed toward the ability to add new capabilities through the same safety principle used for code work:

**build separately → test → inspect → integrate → observe → keep or roll back**

The system should not need to modify a working environment blindly.

## User interfaces are replaceable

Chat, voice, desktop, mobile and the Unity avatar are interaction surfaces. They are not intended to become the owner of the AI core.

## What this public document intentionally does not show

It does not publish:

- exact internal topology;
- module identifiers where unnecessary;
- message schemas;
- routing tables;
- state machines;
- recovery ordering;
- retry thresholds;
- context ranking/scoring formulas;
- private prompts;
- sandbox security details;
- privileged interfaces;
- production configuration.

The goal is to make the engineering philosophy understandable without publishing a reconstruction guide.
