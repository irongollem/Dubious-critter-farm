# Networking

## Principle
Multiplayer is foundational, not an integration phase. The prototype is host-authoritative from its first gameplay systems.

## Authority
Host/server owns authoritative:
- player session membership and spawn state
- creatures, needs, lifecycle, breeding and strain state
- world/interactable state
- inventory and carrying validation
- farm construction/state
- shared currency and sales
- rocket schedule, cargo, stock and contracts
- personal/colony objective truth
- session random seed and consequential random outcomes
- major physics ownership decisions

Clients submit action requests/intents. Clients may predict or interpolate presentation where appropriate, but prediction must not become game-state authority.

## Prototype connection flow
Use Netcode for GameObjects. Local/direct transport is acceptable for earliest testing; Unity Multiplayer Services Lobby/Relay should be introduced when the basic authoritative session works and remote testing requires it.

## Session assumptions
- Fixed-session game; all players normally join near the beginning.
- Target 4, support 5 comfortably.
- Persistent world save is explicitly out of scope.
- Rejoin may begin as crude prototype support, but disconnects must not corrupt ownership/world state.

## Testing
Every authoritative feature should be exercised as host and client. Debug HUD should expose local client id, host/client role, relevant network object ids and authority/ownership state. Provide a repeatable multi-instance workflow and latency/packet-loss test instructions before M1 is considered done.
