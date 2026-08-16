# Rebac

Relationship-based access-control hexagon (NoGod / ReBAC): dependency-free authorization core.

## Hexagon layout

- `core/` — dependency-free domain logic + proofs
- `ports/` — narrow driving (source) / driven (sink) contracts

There is no `adapters/` directory. Nothing here reaches concrete I/O yet.

## Sibling wiring

- (standalone — no sibling cores)
