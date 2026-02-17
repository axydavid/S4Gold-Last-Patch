# The Settlers IV — Unofficial Patch v2.60.0001

A drop-in compatibility and quality-of-life patch for **The Settlers IV GOLD Edition** (GOG / V2.50.1516).  
No manual hex editing, no config headaches — just copy and play.

---

## Features

- **Automatic Resolution Detection** — the game detects your display resolution at startup and patches itself to match. Any resolution supported, works on standard monitors, ultrawides, and the **Steam Deck** (1280×800) out of the box.
- **Full Viewport Rendering** — fixes the viewport so the game renders properly edge-to-edge, including under the left UI panel.
- **Smooth Software Shadow Patch** — replaces the original checkerboard stipple shadows with smooth 50% darkened shadows.
- **Linux / Steam Deck Fixes** — tested and working under Proton/Wine. Includes DPI handling tweaks specific to non-Windows environments.
- **Modern Windows Compatibility** — fixes for Windows 10/11 display scaling, DirectDraw compatibility, and high-DPI displays.
- **FPS Unlocked** — no more 30fps lock.

## Installation

1. Download the latest release.
2. Copy all files into your **Settlers IV root folder** (where `S4.exe` lives).
3. Launch the game. Everything just works.

---

## Screenshots
<img width="1440" height="900" alt="s4pc" src="https://github.com/user-attachments/assets/fff56d0a-8d0e-4d02-94a6-8da9b202e8ff" />
<img width="1140" height="596" alt="sds4" src="https://github.com/user-attachments/assets/f2c08b99-ef19-4706-84c1-a56c03349ecc" />

---

## Configuration

All options are in **`Exe/s4_dev.ini`**. Defaults work for most setups.

```ini
[Resolution]
; Set Width and Height to 0 for auto-detection (recommended). Set explicit values to override auto-detection.
Width = 0
Height = 0

[Patches]
; DPIAware: call SetProcessDPIAware so Windows reports true pixel resolution instead of DPI-scaled values. 
DPIAware = 0
; VersionCheckBypass: skips the multiplayer version number comparison
; File-integrity CRC checks (Gfx, Script, Config) are NOT affected.
VersionCheckBypass = 1

[Debug]
EnableLog = 0
```

---

## Roadmap

- **DX11 Rendering Engine** — complete binary-patch replacement of the GfxEngine.dll rendering backend from DirectDraw to DirectX 11.

---

## Compatibility

| Platform | Status |
|---|---|
| Windows 10/11 | ✅ Working |
| Linux (Proton) | ✅ Working |
| Steam Deck | ✅ Working |
| GOG GOLD V2.50.1516 | ✅ Tested |

---

*This is an unofficial community patch. Not affiliated with Blue Byte or Ubisoft.*
