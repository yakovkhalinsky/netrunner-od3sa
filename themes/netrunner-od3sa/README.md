# netrunner-od3sa

**Author:** Yakov Khalinsky

A neon-on-black re-skin of the default **wargames** theme, based on my Omarchy
[netrunner](https://github.com/yakovkhalinsky/omarchy-files/tree/main/theme/netrunner) desktop theme:
accent `#00ff9f`, cyan `#00f0ff`, hot red `#ff2a6e`, magenta `#ff10f0`, on a near-black background.

## Description / inspiration

- Built from **wargames** (theme_version 1.1.3, theme_framework_version 0.8), tested against the copy in
  `hak5/wifipineapplepager-themes` at commit `beb725c`. Layouts and components are unchanged from wargames,
  so every screen and template is the stock one.
- `theme.json` `color_palette` remapped to the netrunner palette:
  - normal text/chrome (`blue`) → cyan `#00f0ff`
  - selected items and titles (`yellow`) → accent green `#00ff9f`
  - errors/alerts (`red`) → `#ff2a6e`
  - secondary/disabled grays → green-tinted neutrals for readability
- Raster assets were recoloured with Pillow by remapping hue bands. For palette PNGs only the palette entries
  change; for RGBA PNGs each pixel changes but alpha is kept. Image sizes and alpha are identical to wargames.
  - light-blue chrome → cyan
  - navy panels → dark green
  - yellow highlights → accent green (warnings stay yellow)
  - reds, oranges and magentas → the netrunner equivalents
- The dashboard background blends a dimmed crop of the netrunner street wallpaper into its dark area.
- The payload log default text uses `#d4f5e0` and its error text uses `#ff2a6e`.

## Known limitations

- **Not yet tested on real hardware.** Everything was validated offline: JSON parses, all references resolve,
  and image sizes match wargames.
- Uses the green/cyan family heavily, so `yellow` (selection) and `green` (enabled/success) are close in hue
  (`#00ff9f` vs `#39ffbf`).
- QR code images (`help_qr`, `license_qr`, `virt_qr`) are intentionally left as in wargames.
- Boot frames, upgrade screens and spinners are recoloured wargames art, not new artwork.
- A different community theme is also named `netrunner` (Doc Voom, Cyberpunk 2077). Installing both into
  the same `themes/` directory will clash, so rename one directory.

## Firmware

Developed for the firmware that ships wargames theme_version **1.1.3** (Pager firmware 1.1.3).

## Install

```
scp -r netrunner/ root@172.16.52.1:/mmc/root/themes/
```
Then select it under **Settings > Display > Theme**.
