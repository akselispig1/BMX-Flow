# BMX Flow — Endless Pump Rider

A tiny mobile-browser BMX game. Side-on 2D, one button + phone tilt. Auto-ride
left-to-right over an endless wavy dirt trail; pump through the dips, release at
the lip to launch, flip in the air, and land clean.

**Single self-contained file** — `index.html`, vanilla JS + Canvas, no
libraries and no build step. Just open the file or host it on GitHub Pages.

## Play

- **Hold** anywhere — pump to build speed (stronger through compressions/dips).
- **Release** on the upslope/lip of a jump to launch. Steeper lip = bigger pop.
- **Tilt** the phone back / forward (DeviceOrientation `beta`) to rotate in the
  air. No motion sensor (e.g. desktop)? **Drag up/down** on screen instead.
- Land within ~25° of the slope = clean; complete full 360° rotations for trick
  points. Land off-angle = crash.

On iOS the "Tap to Start" screen triggers the motion-permission prompt.

## Tuning

Every feel constant — gravity, base speed, pump acceleration, jump force,
air-rotation speed, landing tolerance, terrain hump size/spacing, colours — is
in the `CONFIG` object at the very top of the `<script>` in `index.html`.

## Structure

Terrain generation, physics/update, input, and rendering are kept in separate
clearly-labelled sections so level types and multiplayer can be layered on
later without rework.
