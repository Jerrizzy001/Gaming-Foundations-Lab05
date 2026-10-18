# Lab 5 verification and remaining captures

Based on the supplied *Tutorial - Lab#5.pdf*, GAM537 Game Development Fundamentals, Lab #5: Open-World Design and Interactive Systems. Activity instructions are on pages 3–21; deliverables and GDD requirements are on pages 22–23. This checklist does not claim that the tests have run.

## Established by the source files

- The descriptor targets Unreal Engine 5.8.
- `Content/Levels/Region01_VerdantFlats.umap` has landscape, shrine, gate, quest-NPC and day-night-controller actor packages. Keep its external actor/object folders intact.
- `Content/ThirdPerson/Blueprints/BP_DayNightCycle.uasset` exists. Its serialized symbols include `SunLight`, `DaySpeed`, `ReceiveTick`, `GetWorldDeltaSeconds`, `Multiply_DoubleDouble`, `MakeRotator` and `K2_AddActorLocalRotation`.
- A controller instance in the main region references a Directional Light. This supports the intended architecture but does not prove valid graph wiring, successful compilation or runtime rotation.
- ExponentialHeightFog, SkyLight, SkyAtmosphere, VolumetricCloud and PostProcessVolume actor packages are present.
- `BP_Fire` includes Niagara and audio components referencing `NS_Fire_Big`, `SFX_FireBig_L` and `SA_FireBig`. The main region has direct fire and fire-trap instances.
- The source default/startup map is still `Lvl_ThirdPerson`. Open `Region01_VerdantFlats` explicitly for the Lab 5 world. The separate `Lab5_Lighting_Hamid` map does not have a day-night-controller reference in its scanned external actor packages.

## Checks to perform in Unreal

1. Open the main region, compile BP_DayNightCycle and inspect the complete graph. Confirm an editable Directional Light reference, DaySpeed default 5.0, valid SunLight assignment, Tick execution, elapsed-time multiplication and rotation through the Pitch input of Make Rotator. Verify the sun actually rotates during Play.
2. Confirm SunLight: Atmosphere Sun Light enabled, intensity 10 Lux, source angle 2.0 and an appropriate initial rotation. Confirm SkyLight: Movable, Real Time Capture and intensity 1.0.
3. Check the tutorial fog setup: density 0.03, height falloff 0.2, max opacity 0.8; Volumetric Fog enabled, scattering distribution 0.7, white albedo and extinction scale 1.5. The supplied screenshots instead show fog density 0.02.
4. Check warm lighting and Sky Atmosphere: Rayleigh scattering scale 1.5 and Mie scattering scale 2.0. The supplied screenshots show SunLight intensity 3.480051 and Rayleigh 1.0. Mie absorption is not the same property as Mie scattering scale.
5. Verify the PostProcessVolume is unbound and check Min/Max EV100 0/0, bloom 0.5, vignette 0.3, ambient occlusion 1.0 and global saturation 1.1.
6. Listen to environmental audio in Play. Confirm Auto Activate, attenuation radius 3000 and appropriate balance. Inspect the actual Niagara system assignment, effect scale 1.5 and visible movement near a landmark.
7. Inspect the focal-point light: intensity 5000, gold/blue colour and attenuation radius 1500. Walk to several locations and check landmark visibility, the paths and contrasting light cues.
8. Run separate DaySpeed trials at 1, 5, 15 and 30. Record three real observations covering shadow direction/length, sky colour, fog or brightness; explain the selected speed. No trial results have been supplied.

## Captures still needed

- A clean overview establishing the entire region. Existing broad editor views do not establish its full extent.
- A Play-mode F9 Hero Shot with the focal landmark, fog, lighting and effects visible.
- Distinct morning, midday and sunset/night gameplay screenshots from the running cycle.
- A readable screenshot of the BP_DayNightCycle graph.

The existing 11 images already support the shrine, ruined-palace storytelling, static fog appearance, forest route, village approach and several editor lighting settings. Do not relabel the red/yellow editor studies as a verified day-night sequence.

## Documentation and package

The GDD must contain Section 5 (region, landmarks and environmental storytelling), Section 6 (day-night system and Blueprint architecture), and Section 11 (visual style, lighting style and audio design), supported by the required captures. The current document records static evidence and remaining verification honestly.

After the checks and any necessary corrections, restore all six release bundles into one project directory and create the final project ZIP with the required maps, Blueprints and assets. GitHub's generated source-code ZIP alone does not contain the large content bundles. Do not treat packaging or this checklist as evidence of runtime correctness. No coursework has been submitted.
