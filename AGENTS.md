# Pool Physics Lab

This is a small browser-based pool practice app with no build step. Open `index.html` in a browser to run it.

- `index.html` defines the page structure and table-overlay artwork, including pocket cavities and rims.
- `styles.css` contains the shared interface styling.
- `app.js` contains canvas drawing, game state, input handling, rack setup, and physics.

Cue controls use the sliders and Take Shot button directly; there are no quick-shot preset buttons.

Sight diamonds use three evenly spaced marks on each short rail and seven evenly spaced marks on each long rail.

When editing pocket visuals, keep rendering changes separate from the physics routines in `app.js` (especially `pocketPhysics`, rail-opening checks, and ball collision resolution). Verify visual-only requests do not change gameplay behavior.

Corner pocket wells and their thick leather rims are full circles, including the portion extending into the playfield. Preserve their configured orientation when refining their artwork, and do not alter collision code for visual pocket changes.

Side pockets are visual-only 46px circular wells centered on the inner wood edge; render the 4px leather rim as an inset layer on the same well element so it shares the exact diameter and offset, with no legacy side-pocket backing layers.

Inner rails are 30px felt-toned cushions with diagonal mouths: side jaws match their 46px pockets and slope outward toward the side pockets, while 60px corner jaws slope away from each corner pocket. Keep the 60px corner jaw length and its steep slope. Corner wells are centered on the rail corner, so inset the corner-side rail vertices by the 23px rim radius—not the diameter—so the opening clears the well without overextending; do not widen the side-pocket mouths or the playing-surface end of the corner jaws. Corner rail collision uses the matching narrow diagonal boundary, motion toward both sides of the target corner, and a sufficiently diagonal approach, preventing shallow-angle clipping through a jaw; do not alter other pocket physics when changing rails.

Teams are open through the break and any shot that pockets both groups. On a later shot that pockets only solids or only stripes, assign that group to the shooter and the other group to the opponent; use these assignments for first-contact fouls and 8-ball eligibility. An 8-ball contact is a scratch only when it is the cue ball's first object-ball contact.

Update this `AGENTS.md` whenever preparing a new commit so its project guidance stays current.
