# Pool Physics Lab

This is a small browser-based pool practice app with no build step. Open `index.html` in a browser to run it.

- `index.html` defines the page structure and table-overlay artwork, including pocket cavities and rims.
- `styles.css` contains the shared interface styling.
- `app.js` contains canvas drawing, game state, input handling, rack setup, and physics.

When editing pocket visuals, keep rendering changes separate from the physics routines in `app.js` (especially `pocketPhysics`, rail-opening checks, and ball collision resolution). Verify visual-only requests do not change gameplay behavior.

Corner pocket wells and their thick leather rims are full circles, including the portion extending into the playfield. Preserve their configured orientation when refining their artwork, and do not alter collision code for visual pocket changes.

Side pockets are visual-only 46px circular wells centered on the inner wood edge; their 36px leather rims are centered on that same anchor and use `border-radius: 50%`, with no legacy side-pocket backing layers.

Update this `AGENTS.md` whenever preparing a new commit so its project guidance stays current.
