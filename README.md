# interactor-sqlar-cas

A content-addressable chunk store specified in Lean: casync chunks in a sqlar database, encrypted with age and shared through key wraps.

## What it is for

The Lean specification is the source of truth. Each layer, from byte parsing through chunking, indexing, encryption and the archive tables, is its own Lake project that builds alone, and the top level composes them with theorems across layers. A Python reader under `scripts/` generates and verifies the test vectors in `testdata/`. The wire format is a draft, not a stable interface.

## Build and run

```sh
lake build
pixi run verify
```

## Licence

Apache-2.0 or MIT, at your option; see `LICENSE-APACHE` and `LICENSE-MIT`.
