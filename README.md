# SignalRGB Custom Components

Community-made custom component layouts for [SignalRGB](https://signalrgb.com), ready to import through **Component Lab**.

## Components

| File | Brand | Type | LEDs | Status |
|------|-------|------|------|--------|
| [`Thermalright_TL-M12QR.json`](components/Thermalright_TL-M12QR.json) | Thermalright | Fan (120 mm, ARGB 5V 3-pin) | 28 | Testing completed.

### Thermalright TL-M12QR — layout

- **Hub ring:** 12 LEDs (indexes 0–11), clockwise from the top
- **Outer infinity ring:** 16 LEDs (indexes 12–27), clockwise from the top
- **Grid:** 25 × 25, centered at (12, 12)

> The LED order is based on the fan's published specs, not measured from a real unit.
> If effects look rotated, mirrored, or run backwards, reorder `LedMapping` and please open an issue or PR with the fix.

## How to import into SignalRGB

1. Download the `.json` file from the [`components`](components) folder (open the file → **Download raw file**).
2. In SignalRGB, open your controller (e.g. motherboard) → **Components** tab.
3. Click **+** on the ARGB header the fan is plugged into.
4. Click **New Component** to open **Component Lab**.
5. Click **Import** and pick the `.json` file.
6. Click **Save**, then **Use this Component**.

## License

[MIT](LICENSE)
