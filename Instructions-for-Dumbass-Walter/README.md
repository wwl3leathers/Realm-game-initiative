# Instructions for Dumbass Walter

This folder is Walter's plain-language operational dashboard.

It answers three questions:

1. What do I need to do next?
2. What must Codex do before it changes anything?
3. What result should exist when the current work is finished?

This is a **fluid working folder**. It must be updated whenever work is added, removed, completed, postponed, or reordered. Do not preserve obsolete checklist items merely because they were once written here.

This folder is not Realm Game design canon and does not approve mechanics. Authoritative design remains in the repository's concept documents. Agent authority and implementation boundaries remain in [AGENTS.md](../AGENTS.md).

## Current To-Do List

### Walter — Connect the Desktop

- [ ] Use the desktop containing the working Talvaren Unity project.
- [ ] Verify that Git is installed.
- [ ] Verify that Git LFS is installed.
- [ ] Run **git lfs install** once for the Windows account.
- [ ] Verify that GitHub Desktop is installed and signed into the correct GitHub account.
- [ ] Verify that Unity Hub can access the Unity editor version recorded in Talvaren's **ProjectSettings/ProjectVersion.txt**.
- [ ] Clone **wwl3leathers/realm-game-initiative** into a new, empty local folder.
- [ ] Confirm that the clone contains **.gitignore**, **.gitattributes**, **AGENTS.md**, and the **Documentation** folder.
- [ ] Open Codex in the new repository.

### Walter — Decisions Still Needed

These decisions cannot be inferred from the Talvaren repository. They may be answered gradually as the audit clarifies the available options.

- [ ] Define what counts as the first finished release, including whether its first public version must already support one-to-five-player online cooperative play with persistent characters.
- [ ] Decide how independent the first release is from Talvaren accounts and future transferable rewards.
- [ ] Establish the financial boundary for hosting, networking services, plugins, and additional assets.
- [ ] Decide whether the initial release is for Walter and invited testers, a wider free public release, or a commercial storefront.
- [ ] Define which ordinary creative and technical decisions Codex may make independently after the foundation is approved.
- [ ] Identify any Talvaren lore, terminology, races, classes, progression principles, visual identity, or naval rules that this separate game may not alter.
- [ ] Choose a public game name when the project is ready for one.

### First Instructions to Codex

Tell Codex to do the following in this order:

- [ ] Read **AGENTS.md** completely.
- [ ] Read **Documentation/Desktop-Setup-and-Naval-Migration.md** completely.
- [ ] Inspect Talvaren's **ProjectSettings/ProjectVersion.txt**.
- [ ] Perform a **read-only** audit of the local Talvaren naval assets.
- [ ] Verify the schooner, sloop, naval capture keeper, runtime ship code, tests, audio, and every required dependency.
- [ ] Perform a broader read-only inventory of existing systems and assets that could be repurposed for the Realm Game.
- [ ] Specifically locate and evaluate Talvaren's water logic, wave system, palm trees, tiki torches, finished dock prefab, island houses and their variations, and Walter's twelve-paint palette.
- [ ] Identify other suitable owned terrain, island, settlement, foliage, prop, lighting, audio, effect, character, animation, interface, and gameplay assets rather than limiting the report to Walter's examples.
- [ ] For every recommended reusable system or asset, state what it does, where it is located, whether it currently works, what it depends upon, and whether it can be migrated cleanly.
- [ ] Record file sizes and identify which files belong in ordinary Git, Git LFS, or neither.
- [ ] Classify assets as fully owned by Walter, project-authored, generated, licensed third-party, replaceable, or uncertain.
- [ ] Identify third-party assets and licensing or redistribution concerns.
- [ ] Confirm that every reusable Unity asset has its matching **.meta** file.
- [ ] Recommend the smallest coherent asset set that provides maximum useful coverage.
- [ ] Report the findings to Walter before copying, importing, deleting, moving, or modifying anything.

### Asset Reuse Direction

- Prefer assets that Walter owns completely whenever possible.
- Reuse the strong systems, prefabs, art, and variations already available rather than recreating satisfactory work.
- The existing water logic, wave system, palm trees, tiki torches, finished dock prefab, island houses and their variations, and twelve-paint palette are explicitly available for evaluation and transfer.
- Do not import a dependency-heavy asset pack merely to obtain one trivial object.
- If a third-party asset pack is worth introducing, obtain meaningful value from that pack and use it as a coherent source rather than mixing one bench from one pack with unrelated pieces from many others.
- If a dependency-heavy pack is not worth using coherently, Codex should create a proper reusable project prefab from inputs Walter owns completely whenever practical.
- A new project-owned prefab must have clean dependencies, matching metadata, clear provenance, and a reusable purpose.
- Using a third-party source inside a project-owned prefab does not erase the source asset's license or provenance. Codex must report that distinction accurately.
- No asset may be migrated merely because it exists. It must support the approved experience and justify its dependency cost.

### After Walter Reviews the Audit

Do not begin this section until Walter explicitly approves the audit and migration scope.

- [ ] Create or place the new Unity project at the cloned repository root.
- [ ] Use Talvaren's recorded Unity version unless Walter approves a different version.
- [ ] Import only the smallest complete set of approved naval assets and dependencies.
- [ ] Preserve working GUIDs and asset references.
- [ ] Resolve missing scripts or references before changing gameplay.
- [ ] Establish one clean baseline scene demonstrating the imported naval foundation.
- [ ] Validate the baseline at the truthful level available; do not describe prototype or EditMode evidence as multiplayer validation.
- [ ] Show Walter the working baseline and report anything still missing.
- [ ] Inspect the Git diff and remove generated or machine-local clutter.
- [ ] Commit and push one coherent migration checkpoint after Walter approves it.

## Current Stopping Point

The next action belongs to Walter: connect the desktop to the repository and start Codex in that local checkout.

Codex must begin with the read-only audit. No naval assets or supporting environment assets are approved for migration until Walter reviews that report.
