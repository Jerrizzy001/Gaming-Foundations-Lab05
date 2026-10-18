# Source snapshot notes

- Input: `DPS937_ThirdPerson_LAB05.zip` (8,989,950,247 bytes).
- Original archive SHA-256: `54f9b337dd1e0f40fdefe6e8e3c530aad07630363d6bf8195878ce8c1cef265d`.
- All original ZIP entries passed CRC validation. Paths, case collisions, links, compression ratios and nested archives were reviewed before upload.
- Original file count: 8,581. Prepared project source file count: 8,579, plus README and asset-attribution documents.
- Retained game assets include 8,299 `.uasset` packages, 15 `.umap` maps, and all supplied external actor/object files.
- Omitted `Config/BroadcastDeviceProviderRegistry.json` and `Config/DefaultEditorPerProjectUserSettings.ini`, which hold machine-specific device/editor preferences.
- Cleared the Android File Server credential value in `Config/DefaultEngine.ini`.
- Removed account entitlement, download-location and cache-state fields from 25 Fab metadata files. Public asset descriptions, authors, identifiers and usage flags remain.
- A scan across all prepared files found no remaining match for the original saved server token or the credential patterns checked.
- Six nested asset archives were inspected. Two Unity particle-demo C# scripts were read but never executed; they remain inside their original third-party source package.
- Unreal Engine was not launched. No project scripts were executed, and no runtime, collision, audio or performance results are claimed.

The supplied project descriptor records Unreal Engine 5.8 and 17 enabled plugins. No standalone `Source/`, `Plugins/`, `Binaries/`, `Intermediate/`, `Saved/` or `DerivedDataCache/` directory was present in the archive.
