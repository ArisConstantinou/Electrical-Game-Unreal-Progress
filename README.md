# Electrical Game Unreal — progress screenshots

These are real 1280 × 720 Unreal Engine 5.8 game-runtime captures from 23 September 2026. They show the **current work in progress**, not a finished realistic game. Most images are direct in-engine screenshots. The chisel comparison below crops only the window border from matched game-window captures; no game pixels were changed. Some exterior views use separate QA map copies for the camera and lighting.

The first three screenshots below were captured from branch `codex/electrical-physical-mortar`, commit `6a90ac8`. The original Electrical Game web project remains separate. This repository contains screenshots only, not the Unreal project or a downloadable game.

## 23 September: faster two-course brick wall

Local Unreal source commit `54e2d51` batches the 90 intact rear bricks while preserving their individual chisel cuts: the selected instance becomes a cuttable Blueprint brick when struck. The 90 rear mortar joints remain separate editable actors. The two matched 1280 × 720 game captures below use the same camera and show the wall before and after this rendering change. In a 300-frame static-camera comparison, draw calls fell from 1,511 to 1,244 on average; average frame time was effectively unchanged near the 240 FPS limit.

![Brick wall with fully dynamic rear course before batching](screenshots/batched-masonry-before.png)

![The same brick wall after rear bricks were batched](screenshots/batched-masonry-after.png)

The next unaltered game-window capture shows a small hole after three real chisel clicks. The still image cannot prove which brick layer received the third hit; an Unreal actor/ray test separately verified that the rear instance was replaced and cut.

![Batched wall after three chisel clicks in the game window](screenshots/batched-masonry-three-chisel-clicks.png)

## 23 September: chisel across a two-course brick wall

Local Unreal source commit `84e1c58` replaces the central work wall's solid backing with a second course of hollow bricks and mortar joints. The two images use the same playable map, camera, viewport, and first-person state. Two real left-mouse chisel clicks open a visible hole in the front brick. A separate Geometry Script trace test reached the rear brick after cutting both front-brick faces. The other room walls are still visual brick skins over solid structure.

![Central brick wall before chisel](screenshots/rear-wall-chisel-before.png)

![The same wall after two chisel clicks](screenshots/rear-wall-chisel-after.png)

## 23 September: scanned plaster material

The Unreal project now uses a [Poly Haven Plastered Wall 02](https://polyhaven.com/a/plastered_wall_02) CC0 scan for nine construction-site plaster surfaces, with diffuse, normal, and roughness maps. These two unaltered runtime screenshots are from local Unreal project commit `508078a`. The exterior uses a copy of the playable map with only its camera moved; the wall screenshot comes from the playable map. This is a material improvement on a still-primitive building, not finished architecture.

![Construction building exterior with scanned plaster](screenshots/building-exterior-pbr.png)

![Playable map wall with scanned plaster on both sides](screenshots/wall-main-pbr.png)

## 23 September: masonry courses and mortar head joints

Local Unreal project commit `03e6bf3` adds 12 half bricks at alternating course boundaries and 78 independent vertical mortar joints. The new joints use Blueprint Geometry Script for chisel subtraction and mortar fill; an editor-world damage test verified mesh changes for both actions. The screenshot below is from the playable map in the Unreal game runtime at the same camera as `wall-main-pbr.png`. It shows the closed gaps, but the clay and mortar materials are still visually simple.

![Playable wall with filled masonry courses and vertical mortar joints](screenshots/wall-head-joints.png)

## Mortar station

The visible 5 L water jug and 20 L bucket are separate Blueprint actors. Their finite water transfer and targeted player controls exist, but the pouring animation, refill, complete mortar sequence, sounds, and final materials are unfinished.

![Mortar station with jug and bucket](screenshots/mortar-station.png)

## Building exterior

The current interior/exterior construction test building has an open doorway and the destructible brick wall visible inside. Much of the architecture and its materials remain blockout quality.

![Exterior of the construction test building](screenshots/building-exterior.png)

## Native water

The exterior basin uses Unreal's Water plugin. Its current colour and shoreline are still provisional.

![Exterior Unreal water basin](screenshots/native-water.png)

These still images verify rendered scene content only. They do not prove final visual quality, performance, character animation, weather, audio, or end-to-end interaction.
