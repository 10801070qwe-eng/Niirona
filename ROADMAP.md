# NIIRONA Public Roadmap

This roadmap is intentionally high level.

Exact internal milestones, protocol changes, private test gates, timing thresholds, and implementation details are not public.

---

## Phase A — Deterministic modular core

- modular subsystem architecture;
- controlled integration fabric;
- deterministic orchestration;
- isolated execution;
- recovery and restart handling;
- separate chat/task paths.

**Status:** largely implemented.

---

## Phase B — Final architecture migration

- remove duplicate legacy control logic;
- preserve a single authority path;
- complete final integration cutover;
- validate normal-user workflows after migration.

**Status:** active / advanced.

---

## Phase C — LLM Runtime & Routing Manager

Create the dedicated model-runtime subsystem for:

- model registry;
- runtime profiles;
- GPU mapping;
- local/cloud lifecycle;
- hot switching;
- health state;
- explicit multi-model modes;
- future hardware-aware model selection.

**Status:** architecture fixed; implementation is a major next block.

---

## Phase D — Intent-controlled system actions

Add the Intent Gate between conversational input and deterministic control.

Goals:

- distinguish discussion from execution;
- support natural phrasing;
- avoid accidental privileged actions;
- emit structured action intents.

---

## Phase E — Security hardening

Dedicated work for:

- input/media boundaries;
- sandbox and network restrictions;
- capability authorization;
- anti-tamper controls;
- auditability;
- privileged-action policy.

---

## Phase F — Cloud-to-local teaching

Add a separate subsystem that can coordinate a cloud teacher model and a local student model.

The model-runtime subsystem provides infrastructure; the teaching subsystem owns the teaching/evaluation workflow.

---

## Phase G — Unity / desktop client completion

The Windows/Unity avatar client is already substantially implemented as a separate application.

Current / ongoing client work includes:

- avatar loading and control;
- automatic bone discovery/mapping;
- rig and pose handling;
- body movement;
- hand and finger behavior;
- neutral-hand calibration;
- menu/UI refinement;
- final connection to NIIRONA through controlled interfaces;
- voice/chat integration.

**Status:** substantial implementation exists; refinement and core integration remain.

---

## Phase H — Broader client surfaces

- richer local administration UI;
- mobile interface;
- deeper voice interaction;
- visual model/hardware management;
- additional replaceable clients.

---

## Long-term direction

NIIRONA's long-term direction is:

- stronger subsystem specialization;
- lower dependence on any single model;
- richer local autonomy;
- safer self-modification;
- better restart recovery;
- more efficient context use;
- controlled cloud assistance;
- replaceable user interfaces;
- lower recurring inference cost.
