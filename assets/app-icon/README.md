# Rustcalc app icon

The app icon is a stylized "R" monogram derived from the Rustcalc brand identity, set on an emerald green tile.

## Palette

| Colour | Hex | Used for |
|---|---|---|
| Background tile | `#145032` | Deep emerald green field |
| Monogram accent | `#9deac6` | Rustcalc mint brand accent |

## Geometry

A 512 × 512 viewBox, clipped to a rounded square with `rx=112`. Windows and Linux use the full
tile. The macOS icons (`.icns`, `gridcraft-macos-512.png`) sit on Apple's grid: an 824/1024
body with a transparent margin.

## Files

| File | Use |
|---|---|
| `gridcraft.svg` | Canonical artwork; also `hicolor/scalable` |
| `gridcraft-1024.png` | 1024 px render of the full tile |
| `gridcraft-macos-512.png` | Runtime Dock icon on macOS (for `apps/gridcraft` to embed) |
| `gridcraft.icns` | macOS bundle icon (`CFBundleIconFile`) |
| `gridcraft.ico` | Windows exe icon, 16–256 px (embedded by `apps/gridcraft/build.rs`) |
| `hicolor/<size>/apps/ai.storyteller.gridcraft.png` | Linux icon theme, 16–512 px; the 256 px one is also the runtime window icon on Windows and Linux |
| `hicolor/scalable/apps/ai.storyteller.gridcraft.svg` | Linux scalable icon |
| `LICENSE.txt` | MIT OR Apache-2.0 |

The app ID is `ai.storyteller.gridcraft`. It's used for the hicolor icon names, the Wayland app
ID and `packaging/linux/ai.storyteller.gridcraft.desktop`.

## Regenerate

Edit `gridcraft.svg`, then run `packaging/icons.sh`. It needs `resvg`, and `iconutil` for the
`.icns` (macOS only). It packs the `.ico` with `cargo xtask ico`.
