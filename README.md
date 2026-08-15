# action-adventure-game-inspired-by-swordigo

A 2D action-adventure game inspired by Swordigo and DKCR — rigged 3D characters rendered as black silhouettes against colored, hand-drawn backdrops.


## About

The game hasn't any name for now.
[Game Name] is a solo-developed 2D action-adventure game. You play as a lone hero marked by a single red hood — crossing four distinct zones plus a final confrontation in a classic hero's journey, fighting enemies with a parry/dodge combat system, upgrading gear at a merchant with a personality (like RE4 and RE8's), and facing down a final boss whose animation deliberately breaks the game's fluid motion.

This project is being built solo, from scratch, in Unity — including learning 3D character animation from zero. Animation is the core technical challenge of this project; every other pipeline decision (Synty base mesh, hand-painted backgrounds, silhouette rendering) has been made specifically to free up time for it.


## Art Direction
Silhouette rendering: rigged 3D humanoid models (Synty Studios assets) rendered as black silhouettes, set against colored, gradient backdrops hand-drawned by me with my graphic tablet, one per zone — full value-contrast keeps gameplay and the hero readable.

Hero accent: a single red hood (a nod to Little Red Riding Hood) — the only colored element on the hero silhouette. It does double duty: gameplay readability (accent color against enemies/background) and character identity (distinctive head silhouette shape), at near-zero animation cost since it's part of the head volume with no extra bones or cloth sim.

Tone: the silhouette style is a purely visual/technical choice — it does not set the narrative tone. "Game Name" is beautiful, lighthearted, and inviting, closer to Swordigo and Donkey Kong Country Returns vibrant silhouette levels than to Limbo/Inside's bleak atmosphere.

Animation philosophy: since the character has no internal detail, readability comes from strong, clear key poses rather than smooth interpolation. Animation is deliberately keyframed at low fps rather than mocap-style fluidity — idle/walk/run around 24fps, attacks/dodge/parry around 12fps ("on 2s," punchier key poses), building toward the final boss's intentional jitter (down to ~8fps or lower). That jitter — implemented as a single global frame-rate parameter, possibly with one isolated element (weapon/cape) lagging behind, and potentially progressive through the fight — becomes a real narrative beat rather than just a visual option.
References: For the frames, I was inspired by Spider Man Across The Spider-verse. Spider-Punk for exemple is composed of a lot of frames in one and only character. Bad Apple!! for expressive movement in pure silhouette, and Donkey Kong Country Returns' silhouette levels (Sunset Shore, Foggy Fumes, Smokey Peak) as proof that fully-colored, high-contrast backdrops stay readable behind pure black silhouettes.


## World

Four zones leading into a final confrontation:

Desert Canyon → "Normal Zone (Grass field, plain)" → Jungle → Crystal Cave → Boss zone

Each zone (plus the final boss zone) has its own hand-painted backdrop — 5 in total. A merchant hub sits somewhere along the route (tentatively between the jungle and the crystal cave). An intermediate boss caps the end of the normal zone, ahead of the final boss.

## Gameplay
Movement: run, jump (coyote time ~0.1–0.15s + jump buffering), attack (input buffered), dodge (dash with i-frames), and parry.
Combat: frontal/melee attacks are parryable, area/zone effects are dodge-only. Enemies (up to 4 types — jumper, ranged, tank, optional flyer) use scripted patterns rather than heavy AI, keeping behavior readable.
Bosses: an intermediate boss at the end of Zone normale, and a final boss whose defining feature is the jitter/frame-drop effect described above.
Progression: XP-based leveling, 3–4 weapons, 1–2 spells, and a merchant NPC with real personality (RE4/RE8-style) whose dialogue evolves across zones — selling potions, armor, and trinkets.
Two balance profiles: a full-featured PC build (dodge + parry, higher risk/reward) and a planned Mobile Lite version (dodge/parry removed, simplified moveset, separate stat multiplier profile) — Mobile Lite comes after the PC game is finished.


## Scope (V1)
4 zones + 1 final boss zone
4 enemy types, 2 bosses (intermediate + final)
5 hand-painted backdrops (one per zone, plus a dedicated one for the final boss)
3–4 weapons, 1–2 spells
2-3 hour playtime
Free vertical slice demo targeted for Steam Next Fest, then Early Access
Tech Stack


Engine: Unity (Student Plan — Pro Editor, Learn Premium, Odin Inspector)
Key packages: Animation Rigging, IK, Cinemachine
Base character assets: Synty Studios — Prototype Pack (hero and light enemies) and Knights Pack (tank enemy), commercially licensed. Since final rendering is a pure black silhouette, base topology/texture detail matters far less than a clean, pre-rigged mesh — remaining work is adaptation/calibration (Animation Rigging, IK, silhouette shader), not building a rig from scratch. Time saved here goes straight into animation.
Language: C#
Primary dev machine: Desktop PC (RTX 4060 Ti 16GB, Ryzen 5 5600X, 32GB RAM)


## Roadmap
Now → mid-Sept 2026: Learning Unity/C# fundamentals (Unity Essentials → Roll-a-Ball → Create with Code) before touching the actual project.
Mid-Sept 2026: Start of actual Emberhood development — first 2–3 months focused on technical prototyping (rig, silhouette shader, movement feel).
~May 2027: Free vertical slice demo targeting Steam Next Fest — polished Canyon → Zone normale transition, full movement/combat system, 1–2 enemy types, hero silhouette readable in motion.
~Jan 2028: Early Access launch, followed by full launch.
Mobile Lite (iOS/Android) planned after the PC release.
Status

Pre-production — currently learning Unity and C# fundamentals ahead of full-time development starting mid-September 2026. Animation is treated as the top-priority risk area and will be prototyped first (a single full combat loop: walk, attack, parry, dodge) before further planning commits around it.

License

All rights reserved. This code is publicly visible for portfolio purposes but is not licensed for reuse or redistribution.
