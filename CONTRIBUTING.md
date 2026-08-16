# Contributing

## Setup
1. Clone the repository.
2. Open it with the Unity editor version pinned in `ProjectSettings/ProjectVersion.txt` once M0 bootstrap lands.
3. Use the package versions committed in `Packages/manifest.json` and `Packages/packages-lock.json`.
4. Run EditMode and PlayMode tests before opening a PR.
5. Verify a PC development build for changes touching runtime code, scenes, networking, or build configuration.

## Branches and PRs
- Keep changes scoped to one issue where practical.
- Reference the issue in the PR description.
- Prefer small, reviewable commits.
- Do not commit generated Library/, Temp/, Logs/, obj/, or local IDE state.
- Large production binaries covered by `.gitattributes` belong in Git LFS.

## Architecture rules
- Multiplayer from day one; do not build gameplay that assumes single-player authority.
- Host/server owns authoritative world state. Clients submit requests/intents.
- Creature definitions are data-driven. Do not create one hardcoded class per species unless behavior is genuinely bespoke.
- Prefer generic ecological channels and reactions over pair-specific species checks.
- Simulation values must be inspectable in debug tooling.
- Player-facing UI should communicate symptoms and causes without exposing raw simulation math by default.
- Session world state is disposable. Persistent progression is unlocks/cosmetics/knowledge, not a persistent farm.

## Issue readiness
An issue may be marked `ai-ready` only when product/design decisions are resolved, dependencies are understood, and acceptance criteria are concrete enough that an implementation agent does not need to invent game design.
