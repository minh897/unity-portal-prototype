# Portal Prototype
An example of replicating portal visual effects in Unity

## Overview
This is just a small experimental project that I've done in my free time. The goal is replicating portal visuals with a basic teleportation logic in Unity Engine. The techniques I used to achieve this include: stencil buffer, screenspace texture sampling, oblique projection and local to world space transformation.

## Technical Breakdown
- **Rendering:** Each portal has a camera rendering the scene from its perspective with position and orientation relative to the player's camera. The output is projected onto the portal surface via a Render Texture. 
- **Teleportation logic:** Custom plane-crossing detection for Player within the portal's threshold using dot product checks for accurate direction-based teleportation.
- **Stencil masking:** Stencil buffer is used to hide geometry outside of portal bounds, avoiding rendering artifacts and visual overlap.
- **Oblique Projection:** The portal camera uses a custom oblique matrix to align its near clip plane with the portal surface, preventing visual clipping when close to the portal.

## Assets
[Platformer Kit](https://kenney.nl/assets/platformer-kit) by Kenney

## Resources
This project's sole purpose is for learning how to make portals in Unity. Some of its implementations can be similar to tutorials and articles online. These are the main resources I used for this project:

- [Portal Rendering with Offscreen Render Targets](https://tomhulton.blogspot.com/2015/08/portal-rendering-with-offscreen-render.html) by Tom 
- [Coding Adventure: Portals](https://www.youtube.com/watch?v=cWpFZbjtSQg&t=179s) by Sebastian Lague
- [How were the portals in Portal created?](https://www.youtube.com/watch?v=_SmPR5mvH7w) by DigiDigger 
- [Portal Series](https://github.com/daniel-ilett/shaders-portal) by Daniel Lillett

## Play
[Playable Demo (Unity Play)](https://play.unity.com/en/games/19b4ffbd-eac9-443e-b5ca-2dd2c6b2840c/portal-prototype)
