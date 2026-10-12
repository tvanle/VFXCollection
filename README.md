# VFXCollection

99 ready-to-use particle effect prefabs for Cocos Creator 3.8.7, converted from Unity packages.

## Preview

<!-- TODO: add preview GIFs -->

No preview images or GIFs are in the repo yet. Until they are added, open the project in Cocos Creator and drag any prefab from the `assets/` folders listed below into a scene.

## What is in the box

| Folder | Prefabs | What it holds |
|---|---:|---|
| `assets/effect/` | 25 | General gameplay effects: hits, box open, bubbles, color change and collect, clouds, fire, level up, smoke, star |
| `assets/vfx/GhostArcher/` | 36 | Combat set: arrows (fire, ice, lightning and combinations), fireball, hits, laser, lightning chain, tornado, warp gate, warnings, revival, recovery |
| `assets/vfx/Prefabs/3D/` | 14 | Explosions, impacts, charge, aura, teleport, thunder, shockwave ring, wild smoke |
| `assets/vfx/Prefabs/UI/` | 12 | UI-space effects: confetti variants, fireworks, flare, aura, radial shine, star |
| `assets/vfx/BeatCat/` | 9 | Background particles, road effects, color transition |
| `assets/vfx/coinTrail/`, `assets/vfx/trail/` | 2 | Coin trail, 3D trail |
| `assets/[DEA] Design PA 1/` | 1 | `boxHit` variant with radial spike streaks and smoke that darkens over its lifetime |
| **Total** | **99** | |

Two custom shaders (`.effect`) are included: `assets/effect/waterSpread/RaceWaterSpread.effect` and `assets/vfx/slash/slash.effect`.

### Effect catalogue

**Hits and impacts**
`hit`, `boxHit` (in `effect/hit`, `effect/box` and `[DEA] Design PA 1`), `fightBoom`, `flyLight`; GhostArcher: `hit`, `hitFire`, `hitFireBall1`, `hitFireBall2`, `hitIce`, `hitLightning`; 3D: `ImpactBlue`, `ExplodeBlue`, `ExplodeOrange`, `shockwaveRing`

**Projectiles and beams (GhostArcher)**
`arrow`, `arrowAll`, `arrowFire`, `arrowFireIce`, `arrowIce`, `arrowLightning`, `arrowLightningFire`, `arrowLightningIce`, `fireBall`, `fireBallBig`, `energyBall`, `laser`, `lightningChain`, `jetFires`, `hellFireEff`

**Buffs, spawn and status**
`revival`, `recovery`, `heartEff`, `levelUp`, `groundLight`, `warpGate`, `skill-hilight`, `warningCircle`, `warningLine`, `warningStrip`, `tornado`; 3D: `AuraBoss`, `ChargeEffect`, `ChargeEnemy`, `SuperMode`, `Teleport`, `Thunder`, `Highlight`, `ShineLightTing`, `SphereBlue`

**Pickups, rewards and celebration**
`coinTrail`, `collectPurple`, `collectYellow`, `changeColor`, `changeGreen`, `changeRed`, `changeYellow`, `bubbleG`, `bubbleR`, `bubbleY`, `boxOpen`, `leveUp`, `star01`; UI: `confeti`, `confetti`, `confetti-001`, `confetti-002`, `confetti-2`, `confetti-new`, `vfx_fireworks`, `Flare`, `aura`, `radial shine`, `radial shine-new`, `star`

**Environment, smoke and fire**
`cloud`, `Particle`, `fire01`, `smokeLight01`, `attckSmoke`, `bossAnger`, `commonLight`, `colorBar`, `runSmoke`, `loadingPanel1`, `smoke_wild`, `trail-3D`; BeatCat: `BGParticle1`, `BGParticle2`, `BGParticle6`, `1`, `ColorTransNew`, `PathParent`, `Changkuai`, `Jizhong1`, `Lianji1`

Effects are built from Cocos built-in components (`cc.ParticleSystem` with its modules such as color/size/rotation over lifetime, noise, trail, shape and texture animation). The UI prefabs use `cc.UIMeshRenderer`. Textures (`.png`/`.jpg`), materials (`.mtl`), a few animation clips (`.anim`) and some meshes (`.FBX`) ship next to the prefabs.

## Requirements

- Cocos Creator 3.8.7 (`package.json` declares `creator.version` 3.8.7)

## Usage

This repo is a complete Cocos Creator project (it has `package.json`, `settings/` and `assets/`).

1. Clone the repo and open the folder in Cocos Creator 3.8.7 to browse everything in the Assets panel.
2. To use effects in your own project, copy the folder you need (for example `assets/vfx/Prefabs/UI/`) into your project's `assets/` directory. Copy the `.meta` files too, they are committed in this repo and keep asset references (materials, textures) intact.
3. Drag a `.prefab` into the scene, or instantiate it from code with `instantiate(prefab)`.

Prefabs reference their own textures and materials, so copy whole effect folders rather than single prefab files. This is not distributed as an npm or Cocos Store package.

## Unity to Cocos conversion notes

- The repo description states the effects were converted from Unity packages. The original package names are not recorded in the repo, so no credits are listed here.
- Some folder and file names come from the source (for example `Changkuai`, `Jizhong1`, `Lianji1`, `guangzhu`) and were kept as is.
- `assets/[DEA] Design PA 1/boxHit` is a self-contained clone of `effect/hit/boxHit` with its own texture and material copies, so edits do not touch the original.

## License

License: TBD. No LICENSE file exists in the repo yet. Check the terms of the original Unity packages before using these effects in a commercial project.
