# Roadmap

Milestones are playable proofs, not subsystem percentages.

- **M0 — Project Foundation:** clone, open, test and build reliably; architecture and intent are understandable.
- **M1 — Four Idiots in a Field:** four players join one authoritative session, move and manipulate the same object consistently.
- **M2 — First Creature Loop:** a generic creature spawns, wanders, eats, matures, reproduces and can be handled while remaining server-owned.
- **M3 — The Broodhorn Problem:** Broodhorn noise and Hushmallow sleep create emergent four-player negotiation through generic ecology systems.
- **M4 — Farm Verbs:** shared farm construction, pens, storage, feed, harvest, grooming, habitats and stewardship become playable.
- **M5 — Five-Minute Rocket:** cargo scarcity, shared money, stock, contracts and farm tiers create tempo/opportunity cost.
- **M6 — Alien Husbandry:** multiple radically different species mechanics validate the generic creature architecture.
- **M7 — Ecology & Session Variation:** stable biology plus strains/environment/population creates learnable but non-solved relationships.
- **M8 — One Real Match:** complete ugly 30–60 minute lobby-to-extraction match.
- **M9 — Semi-Cooperative Objectives:** private goals generate funny selfish behavior without griefing.
- **M10 — Predator at the Fence:** escalating external threats pressure the farm without turning it into a shooter.
- **M11 — Looks Like Our Game:** coherent vertical-slice astronaut, creature, environment, UI, audio and VFX direction.
- **M12 — Content Production:** repeatable creature/content pipeline.
- **M13 — Alpha:** repeated external multiplayer tests with sufficient content/stability to assess retention and balance.
- **M14 — Beta / Launch Prep:** onboarding, progression, Steam, accessibility, performance, telemetry, crash handling and packaging.

## Validation gates
- After M1: fix multiplayer iteration before adding systems if unstable.
- After M3: if Broodhorn + Hushmallow does not create negotiation/laughter/frustration/adaptation, stop adding creatures and revisit the core.
- After M5: if rocket cycles lack urgency/scarcity/opportunity cost, stop progression work and fix economy.
- After M8: if the ugly full match is not fun, do not begin serious production art.
- After M9: if personal goals create grief more than funny selfishness, redesign before any saboteur mode.

## GitHub organization note
The current connector can assign existing milestones but cannot create milestones or repository labels. Until those are added manually, issue titles use `[M#][area]` prefixes and issue bodies record intended labels.

### Milestones to create manually
Create GitHub milestones with the exact M0–M14 names above.

### Useful labels to create manually
Areas: `area:foundation`, `area:architecture`, `area:networking`, `area:player`, `area:creature`, `area:ecology`, `area:farming`, `area:economy`, `area:rocket`, `area:objectives`, `area:threats`, `area:ui`, `area:audio`, `area:art`, `area:tools`, `area:testing`.

Types: `type:feature`, `type:bug`, `type:spike`, `type:content`, `type:tech-debt`, `type:docs`.

Priorities/readiness: `priority:p0`, `priority:p1`, `priority:p2`, `ai-ready`, `needs-design`, `needs-playtest`, `blocked`.
