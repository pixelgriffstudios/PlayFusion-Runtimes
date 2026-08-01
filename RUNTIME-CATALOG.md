# Runtime catalog

`Firmware` means the user must supply legally obtained files for the listed
functionality. No firmware, encryption keys, ROMs, games, or save data are
included in this repository.

| Runtime | System or purpose | Origin | Firmware / keys |
|---|---|---|---|
| `amiga-1.0.kzr` | Commodore Amiga / PUAE | PlayFusion | Kickstart ROM recommended or required by game |
| `arcade-fbneo-1.0.kzr` | FinalBurn Neo arcade | PlayFusion | Game-specific BIOS sets may be required |
| `arcade-mame-1.0.kzr` | MAME arcade | PlayFusion | Game-specific BIOS/device sets may be required |
| `atari2600-1.0.kzr` | Atari 2600 / Stella | PlayFusion | None |
| `atari7800-1.0.kzr` | Atari 7800 / ProSystem | PlayFusion | Optional BIOS |
| `atarilynx-1.0.kzr` | Atari Lynx / Handy | PlayFusion | `lynxboot.img` may be required |
| `cemu-1.0.kzr` | Wii U / Cemu | PlayFusion | User keys required for encrypted WUX content |
| `commodore64-1.0.kzr` | Commodore 64 / VICE | PlayFusion | None for common content |
| `dolphin-1.0.kzr` | GameCube and Wii / Dolphin | Kazeta+ | None for common disc images |
| `dosbox-1.0.kzr` | DOS / DOSBox Pure | PlayFusion | None |
| `dreamcast-1.0.kzr` | Dreamcast / Flycast | Kazeta+ | Dreamcast BIOS recommended |
| `gameboy-1.0.kzr` | Game Boy / mGBA | PlayFusion | None |
| `gameboyadvance-1.0.kzr` | Game Boy Advance / mGBA | PlayFusion | Optional GBA BIOS |
| `gameboycolor-1.0.kzr` | Game Boy Color / mGBA | PlayFusion | None |
| `gamegear-1.0.kzr` | Game Gear / Genesis Plus GX | PlayFusion | None |
| `jaguar-1.0.kzr` | Atari Jaguar / Virtual Jaguar | PlayFusion | None for common cartridge images |
| `linux-1.0.kzr` | Native Linux games | Kazeta official | None |
| `linux-1.1.kzr` | Updated Linux/UMU runtime | Kazeta+ | None |
| `mastersystem-1.0.kzr` | Sega Master System / Genesis Plus GX | PlayFusion | Optional BIOS |
| `megadrive-1.1.kzr` | Genesis / Mega Drive / BlastEm | Kazeta official | None |
| `nes-1.0.kzr` | NES / Famicom / Nestopia | Kazeta official | None |
| `nintendo3ds-1.0.kzr` | Nintendo 3DS / Azahar | PlayFusion | System files and keys may be required for encrypted content |
| `nintendo64-1.0.kzr` | Nintendo 64 / Mupen64Plus-Next | PlayFusion tuned | None |
| `nintendods-1.0.kzr` | Nintendo DS / melonDS DS | PlayFusion | DS BIOS/firmware optional or required by mode |
| `pcengine-1.0.kzr` | PC Engine / TurboGrafx-16 and CD | Kazeta+ community | `syscard3.pce` for CD games |
| `playstation-1.01.kzr` | PlayStation / RetroArch core | Kazeta+ community | PS1 BIOS such as `scph5501.bin` |
| `playstation2-1.0.kzr` | PlayStation 2 / PCSX2 | PlayFusion | Legally dumped PS2 BIOS required |
| `playstationvita-1.0.kzr` | PlayStation Vita / Vita3K | PlayFusion | Official Vita firmware and font package required |
| `psp-1.0.kzr` | PSP / PPSSPP | PlayFusion | None for common game images |
| `saturn-1.0.kzr` | Sega Saturn | Kazeta+ community | Saturn BIOS recommended/required by core and game |
| `scummvm-1.0.kzr` | ScummVM adventure games | PlayFusion | None; original game data required |
| `sega32x-1.0.kzr` | Sega 32X / PicoDrive | PlayFusion | None for common content |
| `segacd-1.0.kzr` | Sega CD / Mega-CD | Kazeta+ community | Region BIOS such as `bios_CD_U.bin` |
| `snes-1.0.kzr` | Super NES / Super Famicom / Snes9x | Kazeta official | None |
| `windows-1.0.kzr` | Windows games / UMU + GE-Proton | Kazeta official | None |
| `windows-1.1.kzr` | Updated Windows / UMU + GE-Proton | Kazeta+ | None |
| `xbox-1.0.kzr` | Original Xbox / xemu | PlayFusion | MCPX, compatible flash ROM, and Xbox HDD image required |

## Origin definitions

- **Kazeta official**: byte-identical to the published Kazeta package, except
  where this table says otherwise.
- **Kazeta+**: obtained from the Kazeta+ runtime collection, which documents
  backward compatibility with vanilla Kazeta.
- **Kazeta+ community**: third-party runtime distributed through the Kazeta+
  runtime page.
- **PlayFusion**: created for the PlayFusion runtime suite using the standard
  Kazeta `.kzr` layout.
- **PlayFusion tuned**: an existing runtime rebuilt with PlayFusion-tested
  settings.
