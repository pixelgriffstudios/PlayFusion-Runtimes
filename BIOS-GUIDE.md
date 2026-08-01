# BIOS and firmware guide

Some runtimes emulate hardware whose firmware is not freely redistributable.
Dump these files from hardware or software you legally own. This repository
does not provide BIOS downloads, firmware dumps, console keys, NAND images,
or copyrighted system files.

## Easiest installation on PlayFusion

1. Put the recognized files anywhere on a FAT32, exFAT, or Linux-readable USB
   drive or SD card.
2. Insert the media.
3. Open **Extras > BIOS Files**.
4. Choose **Scan/Install from media**.
5. Review the list for `PRESENT`, `OPTIONAL`, or `MISSING` status.

PlayFusion validates recognizable filenames and common expected sizes, then
copies them into the correct subfolder under `/var/kazeta/firmware/`.

## Manual installation on Kazeta or Kazeta+

PlayFusion-created RetroArch runtimes look for shared firmware in:

```text
/var/kazeta/firmware/retroarch/
```

Other PlayFusion runtimes use the system-specific locations in the table below.
On Kazeta/Kazeta+, create the folders and copy files through SSH/SFTP or from
mounted removable media. Example:

```bash
sudo mkdir -p /var/kazeta/firmware/ps1
sudo cp /path/to/scph5501.bin /var/kazeta/firmware/ps1/scph5501.bin
sudo chmod 0644 /var/kazeta/firmware/ps1/scph5501.bin
```

Stock Kazeta runtime packages can also expect firmware inside the individual
cart's `bios/` directory or the runtime's RetroArch `system` directory. Consult
the embedded `runtime-info.txt` and the upstream runtime page when using an
untuned upstream package.

## Recognized files

| System | Destination | Files | Status |
|---|---|---|---|
| PlayStation 1 | `firmware/ps1/` | `scph5501.bin` (512 KiB) | Required by the included PS1 setup |
| PlayStation 2 | `firmware/ps2/` | A legally dumped 4 MiB `scph#####.bin` | Required |
| Sega CD / Mega-CD | `firmware/segacd/` | `bios_CD_U.bin`, `bios_CD_E.bin`, and/or `bios_CD_J.bin` (128 KiB each) | Required for the matching region |
| Sega Saturn | `firmware/saturn/` | `sega_101.bin` or `mpr-17933.bin` (512 KiB) | Required/recommended |
| PC Engine CD | `firmware/pcengine/` | `syscard3.pce` (256 KiB) | Required for CD games |
| Atari Lynx | `firmware/retroarch/` | `lynxboot.img` (512 bytes) | Required by the Handy core configuration |
| Nintendo DS | `firmware/retroarch/` | `bios7.bin` (16 KiB), `bios9.bin` (4 KiB), `firmware.bin` | Optional for most DS games |
| Nintendo DSi | `firmware/retroarch/` | `dsi_bios7.bin`, `dsi_bios9.bin`, `dsi_firmware.bin`, `dsi_nand.bin` | Required for DSi mode |
| Game Boy | `firmware/retroarch/` | `gb_bios.bin` | Optional |
| Game Boy Color | `firmware/retroarch/` | `gbc_bios.bin` | Optional |
| Game Boy Advance | `firmware/retroarch/` | `gba_bios.bin` (16 KiB) | Optional |
| Super Game Boy | `firmware/retroarch/` | `sgb_bios.bin` | Optional |
| Atari 7800 | `firmware/retroarch/` | `7800 BIOS (U).rom` (4 KiB) | Optional |
| Commodore Amiga | `firmware/retroarch/` | Legally dumped `kick*.rom`, `kick*.bin`, or `kick*.a500` | Optional; improves compatibility |
| Nintendo 3DS | `firmware/retroarch/` | `aes_keys.txt` | Needed for encrypted content |
| Dreamcast | `firmware/dreamcast/` | `dc_boot.bin` (2 MiB), optionally `dc_flash.bin` | Optional; HLE can boot many games |
| Wii U | `firmware/wiiu/` | `keys.txt` containing legally obtained Cemu keys | Needed for encrypted WUX content |
| Original Xbox | `firmware/xbox/` | `mcpx_1.0.bin`, `Complex_4627.bin` or `Complex_4627v1.03.bin`, and `xbox_hdd.qcow2` | All three required by xemu |
| PlayStation Vita | `firmware/vita/` | Official Sony firmware package (`PSVUPDAT.PUP` or `PSP2UPDAT.PUP`) and font package | Required; install through Vita3K |

## Systems that normally need no external BIOS

NES, SNES, Nintendo 64, Atari 2600, common Game Boy content, common PSP
images, DOSBox Pure, ScummVM, Linux, Windows/Proton, and most GameCube/Wii disc
images normally boot without a separate console BIOS. Arcade titles may still
require game-specific BIOS/device ROM sets distributed with a legally obtained
MAME or FinalBurn Neo set.

## Verify before troubleshooting a game

- Filenames are case-sensitive on Linux; use the capitalization shown above.
- A correctly named file with the wrong byte size is usually the wrong dump.
- Region-specific disc systems may need the BIOS matching the game's region.
- Firmware alone does not guarantee emulator compatibility.
- Never rename an unrelated BIOS merely to satisfy a filename check.
