# healthOS

A responsive web prototype for a future iPhone health and fitness app.

## Run

Requires Node.js 22.12+ (validated with Node 24).

```sh
npm ci --cache /workspace/.npm-cache
npm run dev -- --port 5173
```

`npm run build` produces `dist/`. `npm run preview` serves that build.

## Prototype scope

- Home: illustrative sleep stages, sleep need, recovery measurements, sleep trends, and daily signals.
- Health: proposed health scores and a conceptual body map.
- Training: sample session, completion counter, weekly calendar, goal-based local template, and a saved race.
- Nutrition: manual meal/macronutrient logging and temporary photo preview.
- Neuro: educational brain explorer and proposed tracking concepts.

Meals, session counts, and the latest race persist in this browser's localStorage. Photos are previewed locally and are not saved or analyzed. This is a prototype without authentication or secure health-data storage; use sample entries.

All health measurements are sample values. Undefined scores remain undefined. No wearable sync, continuous heart-rate monitoring, biomarker interpretation, AI generation, meal scoring, or neurological assessment is implemented.

## Integration direction

Target Apple Health, WHOOP, and Garmin. An iPhone app or native companion is needed for HealthKit access; web integration for the other providers requires their approved APIs and authorization. Preserve source, unit, time zone, timestamp, and provider values. Define deduplication and source priority before combining overlapping workouts and measurements. Missing source metrics should remain missing.

Custom sleep, recovery, strain, readiness, battery, load, and health score models need explicit definitions and validation before implementation. Brain illustrations are educational and do not estimate measured regional activation.

## Validation

Production build and local HTTP serving passed. DOM interaction checks covered navigation, meal storage and escaping, macro totals, session completion, weekly navigation, plan template generation, race persistence, and brain selection. Browser rendering was not verified: Chromium download was blocked by the environment network policy.
