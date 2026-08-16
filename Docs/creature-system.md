# Creature System

## Composition
A creature should normally be assembled from data and reusable systems rather than a species-specific class hierarchy.

### SpeciesDefinition
Defines identity and ordinary parameters for:
- needs: hunger, moisture, temperature, noise tolerance, sleep, social need
- behaviors: wander, graze, flee, follow, nest, sleep, attack, steal, manipulate, climb
- production: milk, fibre, eggs, slime, spores, food, useful waste
- reactions: environment, food, nearby species/population
- lifecycle timings and breeding rules
- ecology emitters/consumers
- strain/variant pools
- presentation references

### Runtime state
Server-owned state includes species id, lifecycle stage, current needs, behavior state, strain, steward/lineage metadata, surplus/protection flags, production state and relevant ecology state.

## Lifecycle
Minimum reusable lifecycle: egg/seed → juvenile → adult → breeding-ready. Species may skip/extend stages later, but the first implementation should not over-generalize.

## Stewardship
Starting lineages carry breeder/steward ownership metadata. Other players may move/feed/care for protected stock but cannot permanently sell/slaughter/eject it. Offspring can be marked surplus. Wild/random stock may be colony-owned.

## Ecology
Prefer environmental channels and generic reactions. Example: Broodhorn emits noise; Hushmallow consumes/reads local noise and cannot maintain sleep above tolerance. No direct Broodhorn-vs-Hushmallow check is needed.

Relationships may be compatible, stressful, symbiotic, predatory, catalytic or catastrophic-but-profitable. Only exceptional interactions warrant bespoke pair logic.

## Initial prototype order
1. Generic placeholder creature
2. Broodhorn + Hushmallow
3. Squelchudder, Frillow, Moss Mop, Mawlop, Slime Sleeve, Woolly Wuffler, Gripwhorl
4. Poddlequill and further roster only after system proof

Do not implement the ~50-concept design pool early.
