# Dorn's Giant Jump

Jump to dodge a pseudogiant's ground slam for **S.T.A.L.K.E.R. G.A.M.M.A.** — if you're airborne the instant the slam lands, you take no damage.

## What this mod does

- Hooks the engine's pseudogiant stomp callback and cancels the hit outright for the player while they're jumping or falling
- Only cancels the actual "in the air" window — if you're still recovering from a landing when the slam hits, you take the hit as normal
- Doesn't touch the pseudogiant's damage to anything else (NPCs, physics objects) — only the player's own dodge timing changes

## Why

Vanilla pseudogiant slams hit every nearby object within range regardless of height, so jumping never helped. This makes the timing-based dodge that players expect from a "ground slam" attack actually work.

## Installation

1. Download the latest release from [GAMMA-Giant-Jump](https://github.com/JoshuaCarter/GAMMA-Giant-Jump/releases)
2. Install via MO2 like normal

## Files

- `gamedata/scripts/dorn_giant_jump_main.script` — stomp callback hook + airborne check
- `gamedata/scripts/dorn_giant_jump_mcm.script` — MCM menu (enable toggle, debug log)
