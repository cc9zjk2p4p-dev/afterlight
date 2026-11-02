# AFTERLIGHT — The Ten Realms (v2.5.0 Mobile Stability Update)

An original, self-contained browser arcade game. No build step or dependencies required.

## Features
- Ten progressively themed realms with guardian encounters.
- Moth evolution across five forms, earned through XP.
- Boss health bars and increasingly frequent projectile attacks.
- Power-ups: shield, speed boost, crystal magnet, and blast.
- Local browser save system using `localStorage`.
- Achievements and unlocked-realm atlas.
- Touch-and-drag movement, virtual joystick, on-screen arrow buttons, and WASD/keyboard arrows.
- Responsive layout for phones, tablets, and desktop browsers.

## Run locally
Open `index.html` in a modern browser. For best results, use a local static server or GitHub Pages. No install is needed.

## Publish with GitHub Pages
1. Create a GitHub repository (for example, `afterlight`).
2. Upload `index.html`, `README.md`, and `LICENSE` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch `main`, folder `/ (root)`, then save.
6. Open the published Pages URL after deployment completes.

## Save data
Progress is stored locally in the browser under `afterlight-save-v2`. It does not sync between devices or browsers. Clearing site data can erase the save.

## Controls
- Drag directly on the game canvas.
- Hold and move the virtual joystick.
- Hold an on-screen arrow.
- Use WASD or keyboard arrow keys.
- Pause, save, or restart with the buttons below the controls.

## License
MIT. See `LICENSE`.


## Mobile performance update (v2.2)
- Gameplay rendering is capped at 30 FPS on touch/mobile devices and 45 FPS elsewhere.
- Particle effects are capped to reduce memory and graphics load.
- The animation loop is guarded against duplicate requestAnimationFrame chains.
- Held controls are cleared when the page loses focus or becomes hidden.


## Version 2.3.0
- Added a polished, game-app-inspired visual interface with a stronger game identity, refined HUD cards, controls, panels, and mobile-safe spacing.
- Added a visible version badge in the game header so the deployed build can be checked at a glance.
- Added browser-level protections against pinch zoom, multi-touch page zoom, double-tap zoom, and Ctrl/Command zoom shortcuts.
- Retains the v2.2 mobile performance improvements and touch controls.


## Version 2.4.0 — Mobile game rebuild
- Reworked the main play screen into a fixed-height app layout with no page scrolling during gameplay.
- Added a separate Archive tab for evolution, power-up descriptions, achievements, and the realm atlas.
- Added Archive sorting: realm order, unlocked first, and name A–Z.
- Cached the static starfield/background so it is not redrawn from scratch on every frame.
- Removed synchronous localStorage writes and full archive rendering from ordinary crystal pickups; progress is saved periodically and on manual save or milestones.
- Reduced mobile particle effects and canvas shadow costs, capped active projectiles, and lowered the phone canvas backing resolution while preserving game coordinates.
- Preserved touch joystick, arrow controls, pause, save, restart, and pinch-zoom prevention.


## Version 2.5.0 — iPhone stability and safe-area update
- Reduced mobile gameplay rendering to 24 FPS and lowered the canvas backing resolution to 360×288 while retaining the same game coordinates.
- Disabled expensive canvas glow/shadow effects on touch devices and reduced mobile particle and projectile limits.
- Only records player movement history in the realm that uses the echo mechanic.
- Added iPhone viewport safe-area handling and extra top spacing above the title to keep it clear of the status area/notch.
