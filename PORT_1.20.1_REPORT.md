# Port 1.20.1 Report

## Target

- Minecraft: `1.20.1`
- Fabric: data-only metadata via `fabric.mod.json`
- Forge: data-only metadata via `META-INF/mods.toml` and `lowcodefml`
- Mod version: `12.00.13`

## Pack Metadata

- Mojang `1.20.1` `version.json` reports data pack version `15`, resource pack version `15`, Java `17`.
- `pack.mcmeta` uses `pack_format` `15` and `supported_formats` `[15, 15]`.
- Forge 47 dependency metadata uses `mandatory=true` syntax for `minecraft`.

## Data-Only Layout

- No `src/main/java` is required or packaged.
- No mixin config is packaged.
- Gradle builds a resource/data jar only.

## Preserved

- Namespace/modid: `echoes_of_the_end__structures_`
- Structure IDs
- Structure sets
- Template pools
- Template names, including `end_warship1`
- Structure NBT files
- JSON worldgen placement

## Verification

- Run `./gradlew build`.
- Verify `/locate structure echoes_of_the_end__structures_:<id>` in a fresh 1.20.1 End world for every structure.
