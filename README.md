# Nexus Fleet — Logistics & Fleet Tracking

Production-style frontend for managing vehicles, drivers, shipments, live tracking, and operational alerts.

## Stack

- React 19 + TypeScript
- Vite
- Tailwind CSS 4
- React Router
- Lucide icons

Data is mocked in `src/data/mock.ts` behind an async API layer in `src/api/client.ts`, so swapping in a real backend is a drop-in change.

## Scripts

```bash
npm install
npm run dev
npm run build
npm run preview
```

## App map

| Route | Screen |
| --- | --- |
| `/` | Command dashboard |
| `/tracking` | Live map, vehicle telemetry, ETAs |
| `/vehicles` `/vehicles/:id` | Fleet CRUD + maintenance history |
| `/drivers` `/drivers/:id` | Roster, compliance, performance |
| `/shipments` `/shipments/:id` | Tender-to-POD tracking |
| `/alerts` | Delay, fuel, maintenance, driver notices |

## Architecture

```
src/
  api/          mock client ready for HTTP
  components/   layout, forms, map, UI kit
  context/      app state + CRUD
  data/         seed fleet + geo
  pages/        route screens
  types/        domain models
  utils/        formatting + validation
```

## Notes

The tracking map is a self-contained CONUS visualization (no map API key). Vehicle photos live in `public/images/`.
