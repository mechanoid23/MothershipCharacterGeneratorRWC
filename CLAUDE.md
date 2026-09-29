# CLAUDE.md — MothershipCharacterGeneratorRWC

Module ID: `mothership-character-creator-rwc`
Manifest: `https://raw.githubusercontent.com/mechanoid23/MothershipCharacterGeneratorRWC/master/module.json`

## Standalone design

This module intentionally duplicates all macros from `MothershipCharacterGenerator` (MCG) so it runs without MCG as a dependency. When adding new macros to MCG, add the same macro here too. The Choose Skills macro in this module searches RWC compendium first, then PSG.

## Pack format

LevelDB binary format — same workflow as MCG. Use `fvtt package unpack/pack` with `--compendiumType Macro` (or Journal/RollTable as appropriate).

## Releasing updates

Same process as MCG. Always use a tagged release and name the zip `mothership-character-creator-rwc.zip` to match the download URL.

## Dependencies

- `fvtt_mosh_1e_rwc` — required; provides RWC classes, psionic abilities, skills, and rolltables
- `fvtt_mosh_1e_psg` — required; provides PSG base classes and shared items
