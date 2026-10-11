# AGENTS.md — RuneLite API Reference (Context Only)

## 1. Purpose of This Directory

This directory contains clean Java interface definitions and math utilities extracted directly from the official `runelite-api` repository. It is a **read-only architectural reference** designed to provide AI coding assistants (like GitHub Copilot) with exact method signatures, types, and Javadocs without indexing the full multi-gigabyte RuneLite monorepo.

## 2. Instructions for Coding Agents

- **Read-Only Context:** Do not modify, recompile, or generate code inside this folder.
- **Method Discovery:** When writing features for `RunePipe`, inspect the interfaces in this directory to confirm available getters, return types, and class hierarchies.
- **Key Reference Targets:**
  - `Client.java`: Master session state, tick counts (`getTickCount`), camera parameters (`getCameraYaw`, `getCameraPitch`).
  - `Actor.java` / `Player.java` / `NPC.java`: World positions (`getWorldLocation`), animations (`getAnimation`, `getPoseAnimation`), and click geometries (`getConvexHull`).
  - `Perspective.java`: Pure 3D world-to-2D screen canvas projection math (`localToCanvas`, `getCanvasTilePoly`).
  - `ItemContainer.java` / `InventoryID.java`: Inventory slot arrays and item definitions.
  - `events/GameTick.java`: 600 ms engine tick event contracts.
  