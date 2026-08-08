# action-adventure-game-inspired-by-swordigo

A 2D action-adventure game inspired by *Swordigo*, *Limbo*, and *Inside* — rigged 3D characters rendered as black silhouettes against colored, hand-drawn backdrops.

## About

The game hasn't any name for now.
[Game Name] is a solo-developed 2D action-adventure game. You play as a lone hero crossing three distinct environments in a classic hero journey, fighting enemies with a parry/dodge combat system, upgrading gear at a merchant with a personality (like RE4 and RE8's), and facing down a final boss whose animation deliberately breaks the game's fluid motion.

This project is being built solo, from scratch, in Unity — including learning 3D character animation from zero. **Animation is the core technical challenge of this project**, every other pipeline decision (base mesh, backgrounds, rendering) has been made specifically to free up time for it.

## Art Direction

- **Silhouette rendering**: rigged 3D humanoid models rendered as pure black silhouettes, set against colored, gradient backdrops (hand-painted by me with my graphic tablet, one per zone) — full value-contrast keeps the gameplay and the front readable
- **Hero accent**: a single colored element (neckerchief/bandana) on the hero silhouette, so the player character always reads instantly against enemies and background — same principle as DK's red cap in Donkey Kong Country Returns silhouette levels
- **Fluid animation is the most important** — it's the visual identity of the whole game, which makes the final boss's intentionally jittery, frame-dropped animation land as a real narrative beat rather than just an option in the game
- References: *Bad Apple!!* (Everyone knows Bad Apple, no ?) for expressive movement in pure silhouette, and the silhouette levels of *Donkey Kong Country Returns* for proof that fully-colored, high-contrast backdrops can stay readable behind pure black silhouettes

## Gameplay

- **Movement**: run, jump (with coyote time & jump buffering making the game funnier and more enjoyable), attack, dodge and parry
- **Combat**: melee/frontal attacks are parryable, area attacks are dodge-only — enemies use scripted patterns, no heavy AI, keeping enemy behavior readable rather than needlessly complex
- **Progression**: XP-based leveling, multiple weapons, a merchant NPC with personality selling potions, armor, and trinkets. I'd really love to make something like RE4 and RE8, there is something mysterious behind these merchants, who are they ?
- **Two balance profiles**: a full-featured PC build (dodge + parry, higher risk/reward) and a planned Mobile Lite version (simplified moveset, rebalanced stats via a separate profile multiplier) — for later, the game needs to be finished on PC first

## Scope (V1)

- 3 environments, 4 enemy types, 2 bosses
- 5 hand-painted backdrops (one per zone, plus a dedicated one for the final boss)
- 3–4 weapons, 1–2 spells
- ~1.5–2.5 hour playtime
- I target a vertical slice demo

## Tech Stack

- **Engine**: Unity
- **Key packages**: Animation Rigging, IK
- **Base character mesh**: Synty Studios (POLYGON) asset, modified — since final rendering is a pure black silhouette, base topology/texture detail matters far less than a clean rig; time saved here goes straight into animation
- **Language**: C#

## Status

Early development — currently in the technical prototyping phase (character rig, silhouette shader, core movement feel). Animation is being treated as the top-priority risk area and will be prototyped first (a single full combat loop: walk, attack, parry, dodge) before committing further planning around it.

## License

All rights reserved. This code is publicly visible for portfolio purposes but is not licensed for reuse or redistribution.
