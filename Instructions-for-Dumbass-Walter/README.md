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

### First Instructions to Codex

Tell Codex to do the following in this order:

- [ ] Read **AGENTS.md** completely.
- [ ] Read **Documentation/Desktop-Setup-and-Naval-Migration.md** completely.
- [ ] Inspect Talvaren's **ProjectSettings/ProjectVersion.txt**.
- [ ] Perform a **read-only** audit of the local Talvaren naval assets.
- [ ] Verify the schooner, sloop, naval capture keeper, runtime ship code, tests, audio, and every required dependency.
- [ ] Record file sizes and identify which files belong in ordinary Git, Git LFS, or neither.
- [ ] Identify third-party assets and licensing or redistribution concerns.
- [ ] Confirm that every reusable Unity asset has its matching **.meta** file.
- [ ] Report the findings to Walter before copying, importing, deleting, moving, or modifying anything.

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

Codex must begin with the read-only audit. No naval assets are approved for migration until Walter reviews that report.
