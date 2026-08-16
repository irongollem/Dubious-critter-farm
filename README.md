# Dubious Critter Farm

A 4–5 player session-based semi-cooperative alien farming game.

Four astronauts share one cramped off-world farm. They raise bizarre alien livestock, negotiate scarce space and resources, fulfill colony contracts, survive ecological pressure, and ship goods off-world. Every player also has private incentives that pull them in different directions, but **the colony must succeed first**.

> First proof target: four astronauts, one ugly field, Broodhorns and Hushmallows. If somebody eventually yells “WHO PUT THE BROODHORNS HERE?”, the prototype is doing its job.

## Design targets

- 4 players initially; comfortably support 4–5.
- 30–60 minute sessions, targeting ~45 minutes.
- MOBA-like progression cadence: meaningful changes every 60–90 seconds.
- Shared farm; no private self-sufficient plots.
- Host-authoritative multiplayer from day one.
- Familiar husbandry expressed through alien biology rather than Earth-animal reskins.
- Emergent social/ecological chaos over scripted comedy.
- Personal goals matter only if the colony succeeds.

## Technology

- Unity 6
- C#
- Netcode for GameObjects
- Unity Multiplayer Services / Lobby / Relay where appropriate
- PC first; Steam later
- Fixed session world; no persistent farm save

The exact Unity editor version and render pipeline are deliberately tracked as the first bootstrap decision rather than guessed in this empty repository.

## Current status

**Pre-production / M0 — Project Foundation.** Production assets and broad content work are intentionally deferred until the multiplayer/ecology proof is fun.
