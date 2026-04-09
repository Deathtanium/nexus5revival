# AGENTS.md

Operational guide for contributors and autonomous agents working on the Nexus 5 revival.

## Mission

Make `hammerhead` useful again as a reproducible, testable mobile security platform without sacrificing recoverability.

## Primary Workstreams

1. **Hardware/Firmware Mapping**
   - Document SoC blocks, buses, radios, sensors, boot chain, partitions, and known driver constraints.
   - Keep findings under `docs/hardware-map/`.

2. **Kernel Modernization**
   - Maintain a dedicated `kernel/` workspace with source, configs, patches, and build notes.
   - Target best possible NetHunter compatibility first; pursue newer kernels when feasible.

3. **OS Modernization**
   - Track LineageOS or equivalent newer Android builds under `os/`.
   - Keep flash/install/rollback steps deterministic and documented.

4. **Wireless Capability Path (Nexmon/WPA3)**
   - Preserve existing monitor/injection capabilities.
   - Evaluate WPA3 readiness and identify hardware/firmware blockers with evidence.

5. **Tooling Integration**
   - Maintain NetHunter integration notes under `nethunter/`.
   - Track compatibility notes for `Deathtanium/cSploit` in parallel.

## Change Guidelines

- Prefer small, reversible commits.
- Every risky change must include rollback instructions.
- Record experiments with:
  - device state and build hash
  - exact flashing/install steps
  - expected vs actual behavior
  - logs/artifacts location

## Suggested Next Steps

1. Create `docs/hardware-map/initial-inventory.md`.
2. Import or reference known kernel source baseline for `hammerhead`.
3. Add first reproducible kernel build script in `tooling/`.
4. Add a first-pass flash validation checklist in `docs/flashing/`.
