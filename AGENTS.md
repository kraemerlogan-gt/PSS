# Pool Physics Lab

This is a small browser-based pool practice app with no build step. Open `index.html` in a browser to run it.

- `index.html` defines the page structure and table-overlay artwork, including pocket cavities and rims.
- `styles.css` contains the shared interface styling.
- `app.js` contains canvas drawing, game state, input handling, rack setup, and physics.

When editing pocket visuals, keep rendering changes separate from the physics routines in `app.js` (especially `pocketPhysics`, rail-opening checks, and ball collision resolution). Verify visual-only requests do not change gameplay behavior.

Corner pocket wells are full circles, with a three-quarter rim facing the wood and the well continuing into the playfield. Preserve their configured orientation when refining their artwork, and do not alter collision code for visual pocket changes.

Side pockets are visual-only leather insets with full circular wells centered on the inner wood edge; keep their styling consistent with the corner pockets.

Update this `AGENTS.md` whenever preparing a new commit so its project guidance stays current.
