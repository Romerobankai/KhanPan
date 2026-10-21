# Feature status

## Working (on demo data)
- Ingredient search and category filter
- Seller comparison by total payable cost, unit price, delivery thresholds, pack rounding
- Waste-risk flag: perishables in oversized packs are not recommended
- Basket optimiser: single store vs. split, counting delivery fees and minimum orders
- Meal suggestions from kitchen inventory (expiring items first), servings scaling, cost of missing items
- Shopping list (edit, tick off, remove), kitchen inventory with expiry and low-stock flags
- Budget, manual purchase log, planned vs. spent
- Dark mode, keyboard focus, empty/error states

## Stored in the browser only (localStorage)
List, kitchen, budget and spend. Moving to accounts needs a database and auth (Phase 2).

## Not built yet
- User accounts, saved preferences, multi-device sync (Phase 2)
- Weekly meal planner calendar, reminders/notifications (Phase 2)
- Real prices, stock, checkout (Phase 3): needs retailer APIs, affiliate programs or merchant agreements
- Barcode/receipt scanning, household sharing, other languages (Phase 4)

## Adding a real retailer
Write an adapter that returns `{seller, product, price, packQty, updatedAt}` offers plus a seller record
(`delivery`, `freeDeliveryAbove`, `minOrder`). Keep API keys in server environment variables, never in `frontend/`.
Match retailer products to catalogue IDs by brand, pack size and unit before comparing. Show source and
timestamp on every price, and show stale data as stale.
