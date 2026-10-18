# Echoes of Elaria — Gaming Foundations Lab 5

Unreal Engine project snapshot prepared from `DPS937_ThirdPerson_LAB05.zip` for DPS937.

The complete project, including Unreal Blueprint packages, maps, imported models and textures, is distributed through the private [Lab 5 project snapshot release](https://github.com/Jerrizzy001/Gaming-Foundations-Lab05/releases/tag/lab5-project-snapshot). The Git tree contains the project descriptor, configuration, documentation and file manifests. Downloading GitHub's automatically generated source-code ZIP alone will not include the large project bundles.

## Restore the full project

1. Open this repository's **Releases** page while signed into an account that has access.
2. Download every `Lab05-Project-Part-XX-of-YY.zip` file from the Lab 5 snapshot release and `SHA256SUMS.txt`.
3. Verify the bundle SHA-256 checksums (`shasum -a 256 -c SHA256SUMS.txt` on macOS/Linux).
4. Extract all parts into the **same empty directory**. Each ZIP contains a different set of complete files, with project-relative paths; they are not split ZIP fragments.
5. Open `DPS937_ThirdPerson.uproject` in **Unreal Engine 5.8**, the version recorded in `EngineAssociation`. The descriptor enables 17 plugins; the matching engine installation must provide them. No separate `Plugins/` or `Source/` directory is included in the supplied archive.
6. Open `Content/Levels/Region01_VerdantFlats.umap` for the environment containing landscape, shrine, village-gate and quest-NPC actor packages. `Content/Lab5_Lighting_Hamid.umap` is a separate supplied lighting map; `Content/Levels/LV_TestArea.umap` is also included. Keep the `__ExternalActors__` and `__ExternalObjects__` folders with the maps.

The supplied project configuration still selects `/Game/ThirdPerson/Lvl_ThirdPerson` as both the editor startup map and game default map. Open the desired environment or lighting map explicitly. No default-map change has been made during packaging.

## Evidence in the supplied material

- A shrine landmark among pale trees and a ruined palace with a burning throne.
- A village entrance, roadside campsite and winding forest route.
- Yellow-haze and red-orange editor lighting views.
- Environment Light Mixer settings for SunLight, SkyLight, SkyAtmosphere, VolumetricCloud and ExponentialHeightFog.
- Custom assets including `BP_ElariaGameMode`, `BP_GameInstance`, `BP_PlayerCharacter`, `BP_Shrine`, `BP_VillageGate`, `BP_QuestNPC` and treasure/health-pickup Blueprints.

The screenshot record documents visible scene composition and editor settings. Package preparation did not launch the project, execute supplied scripts, test gameplay, or measure performance.

## Files and privacy

`PROJECT-FILES.json` lists every prepared project file, its size, SHA-256 hash and containing release bundle. `SHA256SUMS.txt` verifies the ZIP downloads.

The source archive is preserved locally. It contains 8,581 files (10.02 GB uncompressed), with no top-level build/cache folders. The uploaded project copy retains 8,579 source files and omits two machine-specific editor/device preference files. Credential values are cleared from configuration. Account entitlement identifiers and downloader/cache fields are removed from 25 Fab metadata files while retaining asset descriptions, author information and usage flags. Game packages and required assets retain their original bytes.

## Third-party assets

See `ASSET_CREDITS.md` for the attribution that can be recovered from the supplied metadata. Those entries identify sources; they are not proof of a particular purchase or license tier. Existing notices in project files remain applicable. No blanket open-source license is added for third-party assets.

This repository is private. No instructor access or public redistribution has been configured.
