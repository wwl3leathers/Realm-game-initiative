# Comprehensive Reusable-Asset Audit

## Purpose

Identify the smallest coherent set of existing Talvaren systems and assets that can accelerate the first Realm Game without damaging Talvaren, importing unnecessary dependencies, duplicating working content, or creating licensing uncertainty.

This is a **read-only audit**. It does not authorize copying, moving, renaming, deleting, importing, reimporting, upgrading, converting, fixing, or modifying any file.

## Required Output

Create one report named **Reusable-Asset-Audit.md**. Do not scatter findings across multiple temporary documents.

For every candidate, record:

| Field | Required information |
| --- | --- |
| Candidate | Human-readable asset or system name |
| Exact location | Full project-relative path |
| Type | Prefab, scene, script system, model, material, texture, audio, animation, package, tool, or other |
| Purpose | What it currently does |
| Current evidence | Where and how it is presently used |
| Working status | Working, partial, prototype, unverified, obsolete, or broken |
| Ownership | Walter-owned, project-authored, generated, licensed third-party, uncertain, or mixed |
| License evidence | Package/source and any verified reuse or redistribution boundary |
| Dependencies | Direct required packages, scripts, assets, shaders, materials, scenes, and settings |
| File size | Candidate size and meaningful dependency total |
| Metadata | Whether every Unity asset has its matching .meta file |
| Portability | Clean, adaptable, expensive, blocked, or uncertain |
| Realm Game value | Specific use it could provide |
| Recommendation | Reuse, adapt, recreate, reinstall, exclude, or investigate |
| Reason | Concise justification |

Do not call an asset reusable merely because it exists.

## Audit Order

Complete the phases in order. Do not repeatedly rescan an earlier phase unless new evidence identifies a missing dependency.

### Phase 1 — Project Identity and Package Baseline

Inspect only:

- **ProjectSettings/ProjectVersion.txt**
- **Packages/manifest.json**
- **Packages/packages-lock.json**
- Render-pipeline settings and pipeline assets
- Input-system configuration
- Build-target settings
- Scripting backend and API compatibility settings
- Relevant quality and physics settings
- Repository .gitignore and .gitattributes
- Any existing asset registries, architecture documents, provenance records, or license inventories

Report:

- Exact Unity editor version
- Render pipeline and required packages
- Input system
- Existing networking packages, if any
- Existing water, terrain, vegetation, navigation, save, addressable, and multiplayer packages
- Obvious version or package conflicts a new project would face

Stop after recording the baseline. Do not upgrade or install anything.

### Phase 2 — Known High-Value Candidates

Locate and evaluate these known candidates first:

#### Naval foundation

- Talvaren schooner prefab
- Talvaren sloop prefab
- Naval capture keeper prefab
- Helm and sailing controls
- Ship transport and passenger-frame logic
- Crew cannon stations
- Cannon projectile pooling and collision
- Captain Broadside
- Grappling, alignment, rope, release, and Cut Free support
- Boarding and landing areas
- Ladders and cabin interactions
- Naval hull hitboxes and health presentation
- Ship naming and appearance systems
- Sailing and cannon audio
- Naval visual effects
- Relevant ship tests and rehearsal tools

#### Environment foundation

- Water logic
- Wave system
- Ocean materials, shaders, and surface assets
- Buoyancy or wave-following integrations
- Finished dock prefab
- Lighthouses, including variations, interiors, light behavior, materials, and supporting effects
- Palm trees
- Tiki torches
- Island houses and every existing variation
- Walter's twelve-paint palette
- Existing beaches, shorelines, cliffs, rocks, reefs, islands, caves, docks, piers, bridges, ruins, and coastal settlement pieces
- Existing sky, fog, weather, lighting, day/night, and ambience suitable for a tropical or seafaring region

For each known candidate, identify its complete direct dependency chain once. Do not repeatedly open the same source merely to reconfirm unchanged numbers.

### Phase 3 — Structured Asset Search

Search each category below. Record only candidates that plausibly support the first seafaring Realm Game.

#### World construction

- Terrain authoring tools
- Heightmap import/export tools
- Terrain layers and paint palettes
- Island or coastline meshes
- Sand, soil, grass, stone, cliff, and underwater materials
- Rocks, boulders, cliff modules, reefs, coral, and seabed pieces
- Waterfalls, rivers, pools, and shoreline effects
- Roads, paths, bridges, stairs, ramps, and boardwalks
- World-boundary, horizon, distant-island, and background assets
- Occlusion, LOD, culling, scene-streaming, and addressable-world support

#### Vegetation

- Palm trees and variations
- Tropical or coastal trees
- Shrubs, grasses, reeds, vines, flowers, crops, and ground cover
- Fallen logs, stumps, driftwood, seaweed, and beach debris
- Vegetation shaders, wind presentation, terrain-detail prototypes, and placement tools

#### Settlements and architecture

- Island houses and variations
- Lighthouses and lighthouse variations
- Lighthouse interiors, stairs, doors, windows, lamps, beams, rotating-light behavior, fog interaction, materials, and nighttime presentation
- Docks, piers, jetties, moorings, ladders, gangways, and harbor structures
- Inns, taverns, shops, warehouses, shipyards, forts, towers, huts, tents, and ruins
- Doors, windows, roofs, walls, floors, stairs, fences, signs, banners, and modular building pieces
- Interior kits and furniture
- Lighting fixtures, including tiki torches, lanterns, braziers, candles, and campfires

#### Props and interactables

- Barrels, crates, sacks, rope, nets, chains, anchors, pulleys, tools, carts, cargo, and market goods
- Maps, charts, books, bottles, tableware, instruments, treasure containers, and navigation equipment
- Weapons and maritime equipment
- Harvestable, lootable, destructible, movable, usable, or storage-capable props
- Existing interaction prompts and reusable interaction foundations

#### Ships and maritime presentation

- Additional boats, rafts, canoes, wrecks, sails, masts, rigging, figureheads, flags, and ship modules
- Ship customization materials and palettes
- Wake, splash, foam, projectile-impact, fire, smoke, damage, and sinking presentation
- Underwater and overboard presentation
- Harbor traffic or ambient vessel assets

#### Characters and creatures

- Existing playable-character foundation
- UMA or other character-generation systems
- Pirate, sailor, guard, merchant, villager, bandit, undead, Arachni, creature, boss, and wildlife candidates
- Clothing, armor, hairstyles, accessories, weapons, and color variations
- Existing character prefabs suitable for reuse without dragging unnecessary frameworks
- Swimming, climbing, boarding, cannon, helm, combat, idle, work, social, and death animations
- Existing animation controllers, retargeting systems, and animation-sorting tools

#### Combat and encounter support

- Character combat foundation
- Health, damage, defeat, targeting, aggro, spawning, encounter, boss, and loot systems
- Ranged attacks, projectiles, spells, area effects, damage-over-time, and healing
- Enemy navigation on moving ships
- Encounter randomization or composition tools
- Existing test enemies and combat rehearsal scenes
- VFX and audio that can be reused coherently

#### Player progression and persistence

- Character creation
- Attributes, classes, abilities, skill progression, inventory, equipment, currency, crafting, vendors, loot, and rewards
- Save/load systems
- Account or authenticated-entry foundations
- Persistence services and data formats
- Existing systems that are too Talvaren-specific to migrate safely
- Any foundation that could preserve future Talvaren reward recognition without coupling the Realm Game prematurely

#### Multiplayer and online foundations

- Networking packages
- Player spawning and ownership
- Host, client, lobby, matchmaking, relay, dedicated-server, authentication, and session systems
- Networked movement, combat, inventory, ships, passengers, projectiles, AI, and scene transitions
- Existing multiplayer tests and truthful validation evidence
- Missing owners or integrations that prevent production multiplayer

This phase is an inventory only. Do not select a multiplayer architecture without Walter's decision.

#### Interface and accessibility

- Menus, HUD, prompts, hotbars, health presentation, inventory, maps, settings, pause, loading, failure, and results screens
- Input rebinding
- Controller support
- Text scaling, subtitles, color distinction, audio controls, motion controls, and other accessibility support
- Existing fonts, icons, cursors, frames, and style assets
- UI frameworks whose dependency cost exceeds their likely value

#### Audio and music

- Ocean, sailing, harbor, island, weather, wildlife, tavern, combat, cannon, impact, fire, footstep, and interface audio
- Music appropriate for exploration, danger, combat, settlements, and discovery
- Audio mixers, spatial-audio configuration, loops, transitions, and volume categories
- Source ownership and licensing for every recommended recording

#### Tools, tests, and build support

- Reusable editor tools
- Prefab validators
- Dependency and missing-reference scanners
- Test infrastructure
- Performance and memory tools
- Build scripts
- Version display, diagnostics, logging, crash reporting, and update support
- Existing tools that are obsolete, destructive, or too Talvaren-specific

### Phase 4 — Dependency and Ownership Review

For every candidate recommended from Phase 3:

1. Determine its direct dependencies.
2. Identify which dependencies pull further packages or frameworks.
3. Calculate the practical migration set rather than reporting only the top-level file.
4. Identify whether one trivial asset would require a disproportionate dependency chain.
5. Determine whether a complete pack could provide enough coherent value to justify that chain.
6. Prefer Walter-owned or project-authored replacements when a pack is not worth introducing.
7. Preserve provenance. A project-created prefab assembled from third-party content does not convert the underlying content into wholly owned work.
8. Mark uncertain ownership or licensing as **blocked pending Walter**, not approved.

Do not inspect personal credentials, receipts, emails, or account data. Ask Walter only when the source or license cannot be established from project-local evidence.

### Phase 5 — Recommendation

End the report with exactly these groups:

1. **Reuse Immediately** — proven, clean, high-value candidates
2. **Reuse After Adaptation** — valuable candidates with bounded work
3. **Reinstall from Owned Source** — licensed packages that should not be copied blindly
4. **Recreate as Project-Owned Prefabs** — simple needs better served by clean owned construction
5. **Exclude** — unsuitable, redundant, obsolete, too expensive, or unjustified candidates
6. **Blocked Questions for Walter** — only decisions or ownership facts Codex cannot determine independently

For each group, provide the estimated ordinary-Git size, Git-LFS size, major packages, and significant risks.

## Search Boundaries

- Do not modify Talvaren.
- Do not allow Unity to upgrade the project.
- Do not install packages.
- Do not reimport the entire project merely to perform the inventory.
- Do not copy assets into the Realm Game repository.
- Do not rename, move, delete, repair, or resave assets.
- Do not inspect unrelated personal folders.
- Do not open the same file repeatedly when one recorded result is sufficient.
- Do not chase exact numerical matches beyond what the audit requires.
- Do not create thumbnails, screenshots, recordings, or generated evidence unless a visual ambiguity cannot be resolved from existing material.
- Do not commit the audit until Walter reviews it.
- Stop and report if the working Talvaren project appears damaged, mid-import, version-mismatched, or dependent upon unavailable mounted storage.

## Completion Condition

The audit is complete when:

- Every required category has been checked once.
- Every known high-value candidate has a recorded disposition.
- Recommended assets have dependency, ownership, metadata, size, and portability information.
- The report identifies the smallest coherent reusable foundation.
- Unknowns have been reduced to questions only Walter can answer.
- Nothing in Talvaren or the Realm Game repository has been modified.
