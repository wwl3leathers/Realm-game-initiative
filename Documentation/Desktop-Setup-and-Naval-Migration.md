# Desktop Setup and Naval Migration Checklist

This checklist prepares the repository for a Unity project without treating the Talvaren project as a disposable source folder.

## Connect the Desktop

1. Install or verify Git, Git LFS, GitHub Desktop, and the Unity Hub.
2. Run `git lfs install` once for the Windows account.
3. Clone `wwl3leathers/realm-game-initiative` into a new, empty local folder.
4. Confirm that `.gitignore`, `.gitattributes`, and `AGENTS.md` are present before Unity creates files.
5. Read Talvaren's `ProjectSettings/ProjectVersion.txt` and use the matching Unity editor unless Butch approves a different version.
6. Create or place the new Unity project at the cloned repository root.
7. Let Unity generate `Library`, `Temp`, `Logs`, `Obj`, and `UserSettings`; verify that Git ignores them.
8. Before the first project commit, inspect `git status` and confirm that authored `Assets`, `Packages`, `ProjectSettings`, and their required `.meta` files are visible.

## Preserve Before Migrating

- Do not alter the working Talvaren project during the initial audit.
- Verify that the local Talvaren naval prefabs exist and open correctly.
- Record file sizes and dependency paths before copying.
- Preserve every matching `.meta` file so Unity GUID references remain stable.
- Identify third-party or Asset Store dependencies and verify that they may be used locally and in the new project.
- Do not commit licensed third-party source assets to a public repository or otherwise redistribute them contrary to their license.
- Do not copy Talvaren's `Library`, caches, generated screenshots, temporary recordings, builds, or backup folders.
- Take a recoverable local checkpoint of irreplaceable authored content before migration.

## Primary Naval Sources to Verify

- `Assets/Talvaren/World/Ships/Schooner/Prefabs/Talvaren_Schooner.prefab`
- `Assets/Talvaren/World/Ships/Sloop/Prefabs/Talvaren_Sloop.prefab`
- `Assets/Talvaren/Prefabs/Rehearsals/Talvaren_Naval_Capture_Keeper.prefab`
- `Assets/Talvaren/World/Ships/Runtime/`
- `Assets/Talvaren/World/Ships/Editor/`
- `Assets/Talvaren/Tests/EditMode/World/Ships/`
- `Assets/Talvaren/Audio/Ambience/1m-ship.mp3`
- `Assets/Talvaren/Audio/Sound Effects/Talvaren_Cannonball_WoodHull_Impact_v02.wav`
- Any meshes, materials, textures, animations, controllers, audio mixers, scripts, packages, and settings returned by an actual dependency audit of those prefabs

This list identifies audit starting points. It is not permission to copy every dependency blindly.

## Migration Method

1. Produce a dependency inventory for each source prefab.
2. Classify each dependency as:
   - Authored and reusable
   - Third-party and reinstallable
   - Generated and reproducible
   - Talvaren-specific and requiring adaptation
   - Unnecessary for the Realm Game
3. Import the smallest complete dependency set into the new project.
4. Open each imported prefab and resolve missing references before changing behavior.
5. Establish a clean baseline scene that demonstrates:
   - Ship presentation
   - Helm movement
   - Passenger frame carry
   - Cannon operation
   - Projectile collision
   - Boarding
   - Grappling and release
   - Required audio and effects
6. Run focused tests and record the truthful validation boundary.
7. Commit one coherent migration checkpoint only after the baseline is reproducible from a fresh clone.

## Storage Rules

- Prefabs, scenes, scripts, configuration, tests, documentation, and ordinary Unity YAML belong in normal Git.
- Large binary source formats covered by `.gitattributes` belong in Git LFS.
- Do not place all Unity `.asset` files in LFS automatically.
- Inspect terrain, generated meshes, and other frequently changing large assets individually before tracking them.
- Local file reads and uncommitted edits consume no GitHub or LFS storage.
- Avoid pushing intermediate versions of large LFS files; each pushed version consumes additional LFS storage.
- If a required file is unexpectedly large, stop and report its size and purpose before adding it.

## First Checkpoint Acceptance

The first Unity checkpoint is complete only when:

- A fresh clone restores the project without relying on undocumented files.
- Unity opens without missing-script or missing-reference errors caused by the migration.
- The approved baseline scene operates at the stated validation level.
- Generated and machine-local files remain untracked.
- The committed diff contains only intentional project content.
- No new Realm Game mechanics have been inferred from the imported Talvaren systems.
