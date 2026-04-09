# Kernel Workstream (hammerhead)

This directory is reserved for kernel-focused work needed to support modernized Nexus 5 pentest workflows.

## Objectives

- Identify the latest practical Android kernel baseline for Nexus 5.
- Maintain reproducible defconfig + patch stack.
- Keep compatibility notes for NetHunter-required features/modules.
- Record flashing and rollback procedures for every kernel milestone.

## Suggested Sub-Layout

```text
kernel/
  src/            # checked-out kernel source trees
  config/         # defconfig fragments and known-good configs
  patches/        # patch queue grouped by topic
  build/          # local build outputs (usually gitignored)
  docs/           # kernel-specific debugging and support matrix
```

## First Tasks

1. Document candidate kernel branches and constraints in `kernel/docs/`.
2. Add an initial reproducible build script under `tooling/`.
3. Capture first boot test results (adb/dmesg/serial logs) and known blockers.
