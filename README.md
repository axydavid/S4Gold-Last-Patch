# The Settlers IV — Unofficial Patch v2.60.0001

A drop-in compatibility and quality-of-life patch for **The Settlers IV GOLD Edition** (GOG / V2.50.1516).  
No manual hex editing, no config headaches — just copy and play.

---

## Features

- **Automatic Resolution Detection** — the game detects your display resolution at startup and patches itself to match. Any resolution supported, works on standard monitors, ultrawides, and the **Steam Deck** (1280×800) out of the box.
- **Full Viewport Rendering** — fixes the viewport so the game renders properly edge-to-edge, including under the left UI panel.
- **Video & Main Menu Stretching** — intro videos and the main menu automatically scale to fill your screen. No more resolution switching.
- **Smooth Software Shadow Patch** — replaces the original checkerboard stipple shadows with smooth 50% darkened shadows.
- **Linux / Steam Deck Fixes** — tested and working under Proton/Wine. Includes DPI handling tweaks specific to non-Windows environments.
- **Modern Windows Compatibility** — fixes for Windows 10/11 display scaling, DirectDraw compatibility, and high-DPI displays.
- **FPS Unlocked** — no more 30fps lock.

## Installation

1. Download the latest release.
2. Copy all files into your **Settlers IV root folder** (where `S4.exe` lives).
3. Launch the game. Everything just works.

---

## Configuration

All options are in **`Exe/s4_enhancer.ini`**. Defaults work for most setups.

```ini
[Resolution]
; Set to 0 for auto-detection (recommended).
; The DLL detects your display resolution at startup.
; Set explicit values to force a specific resolution.
Width = 0
Height = 0

[Patches]
; ResolutionPatch — patches mode tables + height branch for any resolution.
ResolutionPatch = 1

; ShadowPatch — replaces checkerboard stipple shadows with smooth 50% darkening.
ShadowPatch = 1

; ViewportPatch — removes the left GUI border margin and raises the 640×480
; viewport clamp so the game renders full-width under the leftmost UI elements.
ViewportPatch = 1

; VideoStretch — stretches Bink videos and the main menu to fill the whole
; screen instead of displaying them at 640×480 in the corner.
VideoStretch = 1

; DPIAware — calls SetProcessDPIAware so Windows reports true pixel resolution
; instead of DPI-scaled values. OFF by default — the DPI-scaled resolution
; gives a better size for this 2001 game. Turn ON only if you want native pixels.
DPIAware = 0

[Debug]
; EnableLog — writes detailed patch info to Exe/s4_enhancer.log for troubleshooting.
EnableLog = 1
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
