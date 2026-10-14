# SignalRGB Custom Components

Community-made custom component layouts for [SignalRGB](https://signalrgb.com), ready to import through **Component Lab**.

## Components

| File | Brand | Type | LEDs | Status |
|------|-------|------|------|--------|
| [`Thermalright_TL-M12QR_x3_Kit.json`](components/Thermalright_TL-M12QR_x3_Kit.json) | Thermalright | Fan kit (3 × 120 mm, ARGB 5V 3-pin, daisy-chained) | 30 | Tested on real hardware |

### Thermalright TL-M12QR x3 Kit: layout

- **30 LEDs per kit**: 3 fans × 10 LEDs, chained in series on one ARGB cable.
- **Fan 1:** LEDs 1–10 · **Fan 2:** LEDs 11–20 · **Fan 3:** LEDs 21–30
- Each fan is a ring of 10 LEDs, clockwise from the top. The fans are stacked vertically (13 × 39 grid).
- **Two kits on one header** (through a splitter) mirror each other, so use **one** kit component per header.

> **How the count was measured:** with the old 28-LED component, the last LEDs at the corner of the last fan in each kit stayed stuck on an old color. Adding test LEDs on the same header showed 29 still left one LED stuck and 30 lit every LED.
>
> The order of the 10 LEDs inside each fan is an estimate. If effects look rotated, mirrored or run the wrong way, open an issue or a PR with the fix.

### Replaces `Thermalright_TL-M12QR.json` (28 LEDs)

The old single-fan component (28 LEDs: 12 hub + 16 ring) was based on published specs and left 2 LEDs uncontrolled on every kit. If you used it, remove it from the header and add the kit component instead.

## How to import into SignalRGB

1. Download the `.json` file from the [`components`](components) folder (open the file → **Download raw file**).
2. In SignalRGB, open your controller (e.g. motherboard) → **Components** tab.
3. Click **+** on the ARGB header the fans are plugged into.
4. Click **New Component** to open **Component Lab**.
5. Click **Import** and pick the `.json` file.
6. Click **Use this Component**.
7. Remove any old TL-M12QR component from that header, so the header has exactly 30 LEDs.

## Troubleshooting

| Problem | Fix |
|---|---|
| One corner stays a different color | The header has fewer LEDs than the fans. Use the 30-LED kit component and remove the old 28-LED one. |
| The effect looks rotated or upside down | Rotate or flip the component in **Layouts**. |

## License

[MIT](LICENSE)
