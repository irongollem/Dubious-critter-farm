# Content Pipeline

Do not spend production-art effort before the core multiplayer/ecology loop survives playtesting.

## Creature pipeline
Concept sheet → selected design → orthographic turnaround → optional AI 3D draft (Meshy/Tripo or similar) → Blender cleanup/retopo/art direction → custom/generic rig as appropriate → reusable + species-specific animation → Unity prefab and SpeciesDefinition.

Weird anatomy is expected; assume auto-rigging will often fail. Prefer robust generic rigs per body family over forcing humanoid assumptions.

## Astronauts
Build one strong humanoid rig with modular suits, helmets, backpacks, hats and color/customization variants. Reuse humanoid animation heavily.

## Environment
Prefer a modular, hand-built kit: fences, gates, troughs, pipes, rocket pad, workshop pieces, terrain, alien weeds and habitat pieces. Slight repetition is desirable because the farm should read as improvised, functional and shippable rather than as a unique concept render per prop.

## Version control
Large source binaries such as `.blend`, `.fbx`, layered source art and large lossless audio belong in Git LFS. Do not blanket-LFS every ordinary small PNG/JPG asset.

## Definition of ready-for-production
No serious creature/environment production pass before M8 proves a complete ugly match is fun. M11 is where the project intentionally begins looking like the final game.