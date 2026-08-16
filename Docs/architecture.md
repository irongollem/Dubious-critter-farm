# Architecture Baseline

## Goals
Keep gameplay host-authoritative, data-driven and inspectable while allowing weird creature mechanics without one bespoke codepath per species.

## Proposed module boundaries
Exact assembly names are finalized during Unity bootstrap, but target separations are:
- Core: ids, time, deterministic/session random services, shared utilities
- Networking: session/bootstrap, network messages, authority helpers
- Player: input, movement, interaction, carrying
- Creatures: definitions, runtime state, needs, lifecycle, generic behaviors
- Ecology: emitters, consumers, spatial/environment channels, reactions
- Farming: pens, habitats, construction, resources
- Economy/Rocket: shared currency, inventory, cargo, stock, contracts, tiers
- Objectives: colony/personal objective framework
- Threats: external pressure and creature panic
- UI: player-facing presentation only
- Debug/Tools: inspectors, overlays, tuning and test harnesses

Runtime assemblies should not depend on Editor assemblies. Tests may depend on runtime modules; runtime must not depend on tests. Avoid circular dependencies; shared contracts belong in a lower-level assembly rather than cross-linking features.

## Data-driven content
SpeciesDefinition and related assets describe ordinary needs, production, lifecycle, reactions and behavior composition. A species-specific component is justified only for mechanics that generic systems cannot express cleanly.

## Simulation and presentation
Authoritative simulation state is separate from visual/audio feedback. Client presentation observes replicated state/events. Debug tools may inspect raw values; normal UI should communicate understandable conditions.

## Session state
Treat the match as disposable authoritative state. Long-term progression, when added, is a separate persistence domain and never silently serializes the farm world.
