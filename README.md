# KhanPan

Food, grocery and kitchen management in one place: compare the **real payable cost** (item + delivery, per-unit price, surplus waste), plan meals from what you have, keep a kitchen inventory, build shopping lists, and track a grocery budget.

> **All prices are invented demo data** (`data/sample-data.json`). No retailer integrations exist yet.

## Project layout (4 segments)
| Folder | What it is |
|---|---|
| `backend/` | Zero-dependency Node server, cost engine (`costEngine.js`), tests |
| `frontend/` | Mobile-first web app (HTML/CSS/JS, no build step) |
| `data/` | Demo catalogue: sellers, products, offers, recipes |
| `docs/` | Feature status and integration guide |

## Run
Requires Node 18+. No `npm install` needed.
```
npm start        # http://localhost:3000
npm test         # 11 tests: cost engine + API
```
Set `PORT` to change the port.

## Deploy
Any Node host (Render, Railway, Fly.io, a VPS): build command none, start command `npm start`.
The server reads `PORT` from the environment.

## What works vs. what doesn't
See `docs/FEATURE_STATUS.md`.
