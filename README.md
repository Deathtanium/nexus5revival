# Nexus 5 Revival (hammerhead)

Reviving the Google Nexus 5 (`hammerhead`) as a modern mobile pentest platform.

## Core Goals

- Map out Nexus 5 hardware and firmware surfaces as completely as possible.
- Build and install the newest Android kernel that can fully support Kali NetHunter use cases (dedicated `kernel/` folder).
- Build and install a newer Android OS version (likely LineageOS-based).
- Preserve and, where possible, update Nexmon-related functionality.
- Investigate compatibility with newer Wi-Fi security tech such as WPA3.
- Keep practical instructions for iterative development, flashing, testing, and NetHunter install paths.
- Coordinate in parallel with the cSploit revival effort at `Deathtanium/cSploit`.

## Proposed Repository Layout

This structure keeps risky/low-level work isolated and reproducible:

```text
README.md               # project charter + high-level roadmap
AGENTS.md               # contributor workflow for humans/agents
kernel/                 # kernel source, configs, patch queue, build notes
os/                     # ROM/Lineage build scripts and device trees
nexmon/                 # firmware/driver patches and experiment logs
nethunter/              # NetHunter integration and module notes
docs/
  hardware-map/         # chipset, buses, radios, sensors, boot chain notes
  flashing/             # safe install/rollback procedures
  experiments/          # dated lab logs and findings
tooling/                # scripts for build/flash/validation
```

## Initial Milestones

1. Build a complete hardware + firmware map for `hammerhead`.
2. Establish a reproducible baseline build/flash workflow.
3. Bring up kernel + ROM updates, then layer NetHunter support.
4. Re-test Nexmon and document capability gaps (including WPA3 feasibility).
5. Keep install and rollback instructions current after each major change.

## Notes

- This repo focuses on the device/platform revival effort.
- The app-side offensive tooling revival for cSploit should continue in parallel at `Deathtanium/cSploit`, with shared compatibility notes tracked here under `docs/`.
