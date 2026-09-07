# NIIRONA — Current Public Status

**Public status: September 2026**

NIIRONA is an active engineering project. The public documentation distinguishes validated foundations from capabilities that are still being integrated or developed.

## Substantially implemented / validated

- local-first AI runtime work;
- support for local and cloud model providers;
- separate conversation and explicit task paths;
- explicit task activation;
- project-aware context retrieval;
- controlled execution paths;
- sandbox-oriented execution;
- testing and execution evidence;
- failure evidence / learning direction;
- checkpoint and rollback workflows;
- restart recovery;
- long-session stability testing;
- source/identity separation;
- controlled subsystem integration;
- a substantially implemented separate Unity/avatar client.

Restart, long-session and normal user-style task scenarios have been specifically exercised during integration.

## Advanced integration

### Context intelligence
Organized project context and bounded retrieval are part of the architecture. Further work is focused on making context selection increasingly adaptive: using task outcomes to learn what information was actually useful, missing or unnecessary.

### Model runtime management
NIIRONA already supports local/cloud provider work. Dedicated runtime management is the next major infrastructure step, including lifecycle control, GPU mapping, health state and controlled hot switching.

### Final architecture migration
Older duplicate control paths are being removed so the modern controlled architecture remains the single normal runtime path.

## In development / planned

- complete controlled hot switching between models;
- broader multi-model runtime modes;
- hardware-aware model selection;
- stronger adaptive context optimization;
- controlled self-extension loops;
- cloud-to-local teaching;
- deeper voice integration;
- mobile client work;
- final Unity/client-to-core integration;
- additional security hardening.

## Important wording

NIIRONA is **not** being presented as a finished commercial product.

It is also not a concept-only repository. Significant core, recovery, execution and client work exists and has been tested.

Where a capability is still a development target — especially full model hot switching and broad autonomous self-extension — the public documentation labels it accordingly.
