# PlayFusion Runtimes

> **Looking for the actual `.kzr` files?** They are stored on the
> **[PlayFusion Runtimes v1.0.0 download page](https://github.com/pixelgriffstudios/PlayFusion-Runtimes/releases/tag/v1.0.0)**,
> not in the Code file list. Open **Assets** on that page to see and download
> all 37 runtimes individually.

Kazeta-compatible runtime images used and tested by PlayFusion. The release page
provides each `.kzr` separately so users of vanilla Kazeta, Kazeta+, or
PlayFusion can download only the systems they need.

## Downloads

**[Open the runtime download list (37 `.kzr` files)](https://github.com/pixelgriffstudios/PlayFusion-Runtimes/releases/tag/v1.0.0)**

Runtime binaries are GitHub Release assets because several exceed GitHub's
100 MB limit for ordinary repository files. Download runtime files from the
[latest release](https://github.com/pixelgriffstudios/PlayFusion-Runtimes/releases/latest).
Verify downloads with `SHA256SUMS.txt`.

The collection contains **37 runtimes** and no ROMs, games, console BIOS files,
decryption keys, memory cards, user profiles, or save data.

## Install on Kazeta+

Kazeta+ 1.41 and newer can keep runtimes on the internal drive. Copy the desired
`.kzr` files to:

```text
/usr/share/kazeta/runtimes/
```

Kazeta+ checks that directory first, then the inserted cart/disc/USB media.

## Use on vanilla Kazeta or removable media

Place the required `.kzr` in the root of the cart, SD card, USB drive, CD, or
DVD beside the game content and `.kzi` file. Set `Runtime=` in the `.kzi` to the
runtime's base name without its version suffix.

Example:

```ini
[Desktop Entry]
Name=Soul Calibur II
Id=soul-calibur-ii
Exec=soul_calibur_ii/soul_calibur_ii.rvz
Icon=soul_calibur_ii/icon.png
Runtime=dolphin
```

This resolves `dolphin-1.0.kzr`. Runtime selection and cart metadata behavior
remain controlled by Kazeta/Kazeta+.

## Important compatibility notes

- The upstream Kazeta and Kazeta+ packages are preserved as downloaded unless
  the catalog explicitly labels a PlayFusion-tuned variant.
- `nintendo64-1.0.kzr` is the PlayFusion 720p internal / 1080p output variant,
  not the original high-internal-resolution Kazeta package.
- New PlayFusion runtimes follow the standard EROFS `.kzr` layout and
  `.kazeta/share/run` entry point. They are intended for current x86-64
  Kazeta/Kazeta+ systems, but not every game is compatible with every emulator.
- Some systems require firmware or keys supplied by the user. See
  [BIOS-GUIDE.md](BIOS-GUIDE.md) and
  [RUNTIME-CATALOG.md](RUNTIME-CATALOG.md). Those files are not included here.
- Windows, Linux, Cemu, Vita3K, xemu, and some emulator packages are larger or
  more demanding than classic-system runtimes.

## Building the PlayFusion-created runtimes

The reproducible runtime builders are maintained with the main
[PlayFusion source](https://github.com/pixelgriffstudios/PlayFusion/tree/main/tools):

- `build-retro-runtime-suite.sh`
- `build-standalone-runtime-suite.sh`

Kazeta runtimes are EROFS images. They can be inspected with `fsck.erofs`,
mounted with Linux loop mounting, and packed with `mkfs.erofs`.

## Credits

- [Kazeta](https://github.com/kazetaos/kazeta), created by Alesh Slovak
- [Kazeta+](https://github.com/the-outcaster/kazeta-plus), maintained by The
  "Overly Complex" Kazeta+ Guy / The Outcaster
- PlayFusion runtime additions and integration by Jason Griffith / PixelGriff
  Studios
- Emulator and compatibility-layer projects listed in the runtime metadata and
  [NOTICE.md](NOTICE.md)

This project is not affiliated with Nintendo, Sony, Microsoft, Sega, Atari,
Commodore, or other platform owners.
