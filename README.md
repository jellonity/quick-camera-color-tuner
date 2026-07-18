# Quick Camera Color Tuner (QCCT)

<img width="1280" height="720" alt="app-qcct-cover" src="https://github.com/user-attachments/assets/c482fca3-f7f2-4d5f-8536-f974febdb3b2" />

**Fast multi-camera color matching for Wirecast.**
Pick one camera as a reference, match the others to it, and export the result as a 33-point LUT (`*.cube`) that Wirecast loads instantly.

> Windows & macOS · v1.0.0 · Closed source — this repo hosts releases, documentation, and issue tracking.

## How It Works

QCCT works with **Live Snapshot** still frames captured in Wirecast — no live video feed needed:

1. Take a Live Snapshot of each camera in Wirecast (same lighting as your show).
2. Open the snapshot folder in QCCT (`Ctrl+O`).
3. Pick the **reference** camera (`Page Up/Down`) and the camera to **calibrate** (`Home/End`).
4. Compare in **split view** (`K`) and match using the waveform monitor.
5. Save the LUT (`Ctrl+S`) — Wirecast picks it up immediately from its LUT folder.
6. Reset (`Ctrl+D`) and move on to the next camera.

**Tip:** save LUTs directly into Wirecast's LUT folder (Wirecast → LUTs filter → *Customize* opens it). Optionally, QCCT can save the calibrated frame back to the snapshot folder so you can use it as the reference for the next camera.

## Adjustment Tools

- **Lift / Gamma / Gain (Y·R·G·B)** — the primary engine: shadows, midtones, highlights per channel
- **RGB Curves (Y, R, G, B)** — precision fixes in specific tonal ranges
- **Contrast · Saturation · Hue** — coarse global matching
- **Waveform monitor (8-bit)** — match cameras by the scopes, not just by eye

## Performance

Built to run alongside a live show:

- **Preview resolution** ×1 / ×2 / ×4 / ×8 — lower preview detail, lower system load. **The saved LUT is always full quality.**
- **Rendering engine** — Single-Core CPU, Multi-Core CPU, or GPU. GPU is fastest; Single-Core keeps impact on a loaded streaming PC minimal.
- Need to recalibrate on air? Drop the preview to ×4/×8, fix quietly, `Ctrl+S` — Wirecast reloads the LUT without lagging your streams.

## Keyboard Shortcuts

*Replace `Ctrl` with `⌘` on macOS.*

| Shortcut | Action |
| --- | --- |
| `Ctrl+S` | Save LUT |
| `Ctrl+O` | Open snapshot folder |
| `Ctrl+R` | Reload snapshot folder |
| `Ctrl+D` | Reset all corrections |
| `Ctrl+Shift+S` / `Ctrl+Shift+O` | Save / load correction settings |
| `J` / `K` / `L` | Calibrated / Split view / Reference |
| `Home` / `End` | Next / previous image to calibrate |
| `Page Up` / `Page Down` | Next / previous reference image |

## Beyond Wirecast

QCCT exports standard 33-point `*.cube` files — usable in other streaming and editing apps, and loadable as presets on LUT-capable monitors and cameras.

## Feedback

QCCT is a pre-release — feedback and feature requests genuinely shape what comes next. Open an [issue](../../issues) or write to [jellonity@gmail.com](mailto:jellonity@gmail.com).

**Jellonity** · [Website](https://www.jellonity.com) · [Instagram](https://www.instagram.com/jellonity/) · [Facebook](https://www.facebook.com/jellonity) · [Medium](https://medium.com/@jellonity)

---

*Quick Camera Color Tuner by Jellonity is an independent project and is not affiliated with or endorsed by Telestream, LLC. Wirecast is a trademark of Telestream, LLC.*
