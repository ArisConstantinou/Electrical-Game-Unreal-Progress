# Electrical Game Unreal — progress screenshots

These are unaltered 1280 × 720 screenshots captured from the Unreal Engine 5.8 game runtime on 23 September 2026. They show the **current work in progress**, not a finished realistic game. The capture used copies of the `ConstructionSite` map with only the camera position changed; the playable map was not modified for these images.

The first three screenshots below were captured from branch `codex/electrical-physical-mortar`, commit `6a90ac8`. The original Electrical Game web project remains separate. This repository contains screenshots only, not the Unreal project or a downloadable game.

## 23 September: scanned plaster material

The Unreal project now uses a [Poly Haven Plastered Wall 02](https://polyhaven.com/a/plastered_wall_02) CC0 scan for nine construction-site plaster surfaces, with diffuse, normal, and roughness maps. These two unaltered runtime screenshots are from local Unreal project commit `508078a`. The exterior uses a copy of the playable map with only its camera moved; the wall screenshot comes from the playable map. This is a material improvement on a still-primitive building, not finished architecture.

![Construction building exterior with scanned plaster](screenshots/building-exterior-pbr.png)

![Playable map wall with scanned plaster on both sides](screenshots/wall-main-pbr.png)

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
