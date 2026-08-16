# entities-lean-rebac

Relationship-based access-control hexagon (NoGod / ReBAC): dependency-free authorization core. The production `NoGod` core is Mathlib-free; the research-tier `ReBAC` proofs use Mathlib.

> Split out of the [`lean-predictive-bvh`](https://github.com/v-sekai-multiplayer-fabric/lean-predictive-bvh) monorepo (now archived). Cross-cluster wiring is via Lake `require ... from git`.

## Dependencies

- `mathlib` @ `v4.30.0` — research tier only

## Build

```sh
lake build           # production gate: typecheck the Rebac cluster
lake build Research  # research-tier (non-gating; may fail)
```

## Hexagon layout

The triad sits one namespace down, under `Rebac/`:

- `Rebac/core/` — dependency-free domain logic + proofs (`NoGod.lean`, `ReBAC.lean`)
- `Rebac/ports/` — narrow driving (source) / driven (sink) contracts (`AuthQuery.lean`)

There is no `adapters/` directory. Nothing here reaches concrete I/O yet.
