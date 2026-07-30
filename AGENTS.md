# Pool Physics Lab

This is a small browser-based pool practice app with no build step. Open `index.html` in a browser to run it.

- `index.html` defines the page structure and table-overlay artwork, including pocket cavities and rims.
- `styles.css` contains the shared interface styling.
- `app.js` contains canvas drawing, game state, input handling, rack setup, and physics.

When editing pocket visuals, keep rendering changes separate from the physics routines in `app.js` (especially `pocketPhysics`, rail-opening checks, and ball collision resolution). Verify visual-only requests do not change gameplay behavior.

Corner pockets are visual three-quarter circles with the missing quarter facing into the playfield. Preserve their configured orientation when refining their artwork, and do not alter collision code for visual pocket changes.

Update this `AGENTS.md` whenever preparing a new commit so its project guidance stays current.
