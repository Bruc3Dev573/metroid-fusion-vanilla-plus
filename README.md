# Metroid Fusion Vanilla+

English | [Italiano](README.it.md)

A collection of palette changes and small quality-of-life improvements for the European version of Metroid Fusion. It changes the colors and cuts down waiting time without changing movement, combat or progression.

European adaptation and testing by [Bruc3Dev573](https://github.com/Bruc3Dev573). The game's original five languages, including Italian, are unchanged.

## Download

The v1.0.0 patch and its checksum are on the [Releases](https://github.com/Bruc3Dev573/metroid-fusion-vanilla-plus/releases) page.

## Changes

- Revised environment and character palettes, including Samus's suits.
- Faster navigation dialogue text.
- Faster door transitions, with the correction for odd vertical distances.
- Faster elevators.
- Press Start to skip the introduction on a new file. Without Start, the introduction plays normally.

Better Suits Colours, Adam dialogue skip, single-wall jumping, infinite bomb jumping and unlocked doors are not included. This is not the full Redux patch. The palette changes reflect the recolor author's choices, not an official color restoration.

## Screenshots

Captured from the patched ROM in BizHawk at 240 x 160 pixels.

| Introduction in Italian | Navigation dialogue |
|:---:|:---:|
| ![Introduction in Italian](docs/screenshots/intro-italian.png) | ![Navigation dialogue in Italian](docs/screenshots/navigation-italian.png) |
| **Samus and the station** | **Habitation terminal** |
| ![Samus and the station colors](docs/screenshots/gameplay.png) | ![Samus beside the Habitation terminal](docs/screenshots/habitation.png) |

## Required ROM

Use a clean copy of `Metroid Fusion (Europe) (En,Fr,De,Es,It)`. The USA and Japanese releases are not compatible.

| Property | Value |
|---|---|
| Game code | `AMTP` |
| Revision | `0` |
| Size | `8388608` bytes |
| CRC32 | `974e46ab` |
| SHA-1 | `cc46d54b70c1ee38c856ee6e58ec712136763389` |
| SHA-256 | `a024ef6fa8ff19444bc6c31a714eb6cab44464b39227fcd434e409fca1cd8198` |

## Installation

1. Keep a backup of the original ROM and check its hash. The IPS format does not check the base ROM for you.
2. Apply [`metroid-fusion-vanilla-plus-eu-v1.0.0.ips`](patches/metroid-fusion-vanilla-plus-eu-v1.0.0.ips) with [Lunar IPS](https://fusoya.eludevisibility.org/lips/) or another IPS patcher. Save the result to a new file.
3. Compare the patched ROM's SHA-256 with the value below.
4. Start the game and select your language.

Apply this one IPS to the clean ROM, with no other patches installed. The resulting ROM remains 8 MiB.

| File | SHA-256 |
|---|---|
| IPS patch | `03f15ebaf6939ad58c4c977113866d29b0a751a400685f1c0064d8365dc0f728` |
| Patched ROM | `fd211f006f81ef2ce3ea09de94831a4a1b33b2e87702618fa6c18b1eedf11312` |

These values and the patched ROM's SHA-1 are also listed in [`release.json`](release.json).

## Testing

Rebuilding the patch and applying it to the clean ROM produce the same result. Checks covered fast text, doors and elevators, including the odd distances that caused problems in the original faster-door modification.

BizHawk checks covered the full introduction, Start skips at two different points, two door crossings and an elevator route. In the compared cases, the save after the introduction was identical to the unmodified game's save. The Habitation terminal was observed in a prepared test scene, with no disappearance during its inactive animation cycle.

A full playthrough has not been completed. The patch has not been tested on a physical GBA or MiSTer, and the checks do not cover every room or story event.

## Credits

- **Piggy Chan!**: [Color Palette Improvement](https://www.romhacking.net/hacks/8122/), covering environments, characters and suits.
- **ShadowOne333**: the [European port of Color Palette Improvement](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/ColorImprovement/color_improvement_eur.asm), used as the palette source.
- **SpineShark**: [Fast Text](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L114-L126).
- **Jumzhu**: [Faster Door Transitions](https://metroidconstruction.com/resource.php?id=414).
- **somerando/caauyjdp**: the [odd-distance correction for Faster Door Transitions](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_door_transitions.asm).
- **interdpth**: [Faster Elevators](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_elevators.asm), preserved in the Redux source with ShadowOne333's port.
- **ShadowOne333 and yohann**: the original modification and research behind [Start-to-skip introduction](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L4-L6), used as a reference. The European version uses a dedicated implementation.
- **[Bruc3Dev573](https://github.com/Bruc3Dev573)**: European integration, EU intro-skip code, build tools, testing and patch packaging.
- **Nintendo**: original game, artwork and text.

The links point to each patch's page or its specific source code. For Fast Text and Faster Elevators, the available reference is the individual modification's source rather than a separate Romhacking.net listing. The Redux sources used are from commit `e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a`.

## License and attribution

Original documentation and integration notes are © 2026 Bruc3Dev573 and licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). When reusing them, credit the author, link to [this project](https://github.com/Bruc3Dev573/metroid-fusion-vanilla-plus) and the license, and indicate any changes.

The hacks retain their original credits and terms. The [original Redux README](docs/Metroid-Fusion-Redux-README.txt), [GPLv3](docs/Metroid-Fusion-Redux-LICENSE.txt) and [`NOTICE`](NOTICE) are included. The documentation license does not cover the game or the artwork in screenshots.

This is an unofficial fan project, provided without warranty. A legitimate copy of the game is required. No ROMs, saves or emulators are included.
