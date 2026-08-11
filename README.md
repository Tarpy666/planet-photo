# Planet Photo

Viewfinder math (exposure triangle, focal length FoV), develop pipeline, catalog store.

Part of the Counted fleet (planet-photo), generated from `seeds/seeds.yaml`.

## Architecture

- `src/modules.ts` — ExposureMath, DevelopPipeline, PhotoCatalog
- `src/index.ts` — public API (`SPEC`, `MODULES`, Registry)
- `src/rng.ts` — deterministic seeded PRNG (mulberry32)
- `tests/index.test.ts` — deterministic behavior suite

## Usage

```bash
npm install
npm run typecheck   # strict TS, zero errors
npm test            # deterministic, seeded
npm run build
```

## Determinism

All outputs are seeded; identical inputs produce identical results on any runtime.
