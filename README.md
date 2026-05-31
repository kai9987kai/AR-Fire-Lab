
# AR Fire Lab

**AR Fire Lab** is an experimental browser-based augmented reality fire engine built with **A-Frame** and **AR.js**. It turns a Hiro marker, custom image marker, `.patt` file, or barcode-style fallback into an interactive AR fire scene with adaptive effects, camera rescue tools, diagnostics, capture options, and mobile-friendly controls.

The project is designed as a single-file creative AR lab: open `index.html`, allow camera access, show a marker, and control a procedural fire system directly in the browser.

---

## Highlights

- Marker-based AR fire scene using AR.js
- Hiro marker support
- Custom image marker upload
- `.patt` marker support
- Smart generated marker mode
- Barcode / matrix fallback mode
- Marker quality scoring with **Marker IQ**
- Multi-scale visual fallback matching
- Scan rescue mode for weak cameras
- Camera switching and focus assist
- Adaptive performance governor
- Guardian mode for stability
- Live FPS, camera, marker, battery, and health diagnostics
- Fire modes including ember, plasma, aurora, quantum, cryoflame, spectral, and voidfire
- FX packs including cinder rain, plasma arcs, core lens, storm forge, and spectral overload
- Weather / atmosphere presets
- Wind, heat, gravity, turbulence, haze, aura, swirl, and particle controls
- Snapshot and short recording support where the browser allows it
- Preset save, load, share, and diagnostic log export
- Mobile-first interface with scrollable controls
- Built-in help and troubleshooting panel
- WebXR-ready structure for future markerless AR placement

---

## Demo Concept

AR Fire Lab is not just a simple AR fire effect. It is a guided AR testing environment for improving marker reliability, camera performance, and visual responsiveness.

The app combines:

1. **AR tracking**
   - Hiro marker
   - Custom `.patt` marker
   - Generated image marker
   - Barcode / matrix fallback

2. **Visual rescue**
   - Marker IQ scoring
   - Multi-scale matching
   - Scan boost
   - Scan rescue
   - Camera health checks

3. **Reactive fire simulation**
   - Procedural particles
   - Heat haze
   - Sparks
   - Wind
   - Burst shockwaves
   - FX packs
   - Weather presets

4. **Live diagnostics**
   - FPS
   - Stability
   - Marker losses
   - Camera state
   - XR support
   - Battery / health indicators
   - Error count
   - Performance governor state

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/kai9987kai/AR-Fire-Lab.git
cd AR-Fire-Lab
````

### 2. Run it locally

Because camera access requires a secure context, run the project from `localhost` or host it over `HTTPS`.

Using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Or open the repository with any local development server.

### 3. Allow camera access

When the browser asks for permission, allow camera access.

For best results, use:

* Chrome or Edge on Android
* Safari or Chrome on iOS
* A rear-facing phone camera
* A well-lit matte printed marker

### 4. Show a marker

Start with the Hiro marker first.

In the app, press:

```text
Open Marker
```

Show the marker to the camera and keep all four corners visible.

---

## Using Custom Markers

AR Fire Lab supports several marker workflows.

### Hiro Marker

The default mode uses the classic Hiro AR marker.

Use this when testing the app for the first time.

### Upload Image / .patt

Press:

```text
Upload Image/.patt
```

You can upload:

* A normal image
* A trained `.patt` file
* A pattern text file

Image uploads can be converted into a local AR.js pattern and printable scan card.

### Marker IQ

When using a custom marker, **Marker IQ** scores the image for:

* Contrast
* Detail
* Tone balance
* Orientation uniqueness

A stronger marker should have bold contrast, clear corners, asymmetric detail, and minimal shiny reflections.

### Make Strong

Use:

```text
Make Strong
```

to generate a stronger high-contrast marker when your uploaded image is not reliable enough.

### Self Test

Use:

```text
Self Test
```

to verify the marker/signature path before relying on it in a live demo.

### Barcode Fallback

Switch marker mode to barcode/matrix mode and use the barcode value control when normal marker pose tracking is unreliable.

---

## Controls

### Main Buttons

| Control              | Purpose                                              |
| -------------------- | ---------------------------------------------------- |
| `Burst`              | Creates an instant fire flare and shockwave          |
| `Pause`              | Pauses the simulation                                |
| `Reset`              | Restores the scene                                   |
| `Calibrate`          | Re-centres and recalibrates behaviour                |
| `Camera`             | Checks or switches camera input                      |
| `Director`           | Automatically shapes heat, wind, and scene behaviour |
| `Weather`            | Cycles environmental presets                         |
| `Script`             | Changes scripted behaviour mode                      |
| `Guardian`           | Keeps the demo stable under stress                   |
| `Wake`               | Attempts to keep the screen awake                    |
| `Focus Marker`       | Requests camera focus assist where supported         |
| `Scan Boost`         | Improves scan tolerance for weak cameras             |
| `Scan Rescue`        | Attempts to recover marker lock                      |
| `Marker`             | Cycles Hiro, Custom, and Barcode modes               |
| `Upload Image/.patt` | Loads a custom marker                                |
| `Barcode Card`       | Opens barcode fallback guidance                      |
| `Heat Map`           | Toggles heat/scan visual feedback                    |
| `FX`                 | Cycles effect packs                                  |
| `Mode`               | Changes flame colour world                           |
| `Audio`              | Toggles audio where supported                        |
| `Record`             | Records a short clip where supported                 |
| `Snapshot`           | Captures an image where browser security allows      |
| `Auto Quality`       | Allows adaptive quality control                      |
| `Optimize`           | Reduces load for better performance                  |
| `Assist`             | Enables extra scanning/camera help                   |
| `Tilt Wind`          | Uses device orientation for wind control             |
| `Reduce Motion`      | Reduces visual motion                                |
| `Contrast`           | Increases UI contrast                                |
| `Save`               | Saves the current preset locally                     |
| `Load`               | Loads the saved preset                               |
| `Share`              | Exports preset JSON                                  |
| `Open Marker`        | Opens the current marker guide                       |
| `Export Log`         | Downloads diagnostic logs                            |
| `Fullscreen`         | Enters fullscreen mode                               |
| `HUD`                | Toggles diagnostics                                  |
| `Help / Ideas`       | Opens built-in help                                  |

---

## Fire Parameters

AR Fire Lab exposes many live controls:

| Slider            | Description                     |
| ----------------- | ------------------------------- |
| `Intensity`       | Overall fire strength           |
| `Wind`            | Horizontal flame drift          |
| `Turbulence`      | Chaotic flame movement          |
| `Scale`           | Scene scale                     |
| `Particle Budget` | Number of particles used        |
| `Haze`            | Heat haze / atmosphere level    |
| `Spark Size`      | Size of spark particles         |
| `Gravity`         | Downward pull                   |
| `Reactivity`      | How strongly the scene responds |
| `Aura`            | Glow and surrounding energy     |
| `Swirl`           | Rotational movement             |
| `Colour Temp`     | Warm/cool colour mix            |
| `FX Depth`        | Strength of extra effect layers |
| `UI Scale`        | Interface size                  |

---

## Effect Packs

The `FX` button cycles through layered visual packs:

* Core
* Cinder Rain
* Plasma Arcs
* Core Lens
* Storm Forge
* Spectral Overload

Use lower `FX Depth` and lower `Particle Budget` on older phones.

---

## Flame Modes

The `Mode` button changes the visual style of the fire.

Available modes include:

* Ember
* Plasma
* Neon
* Smoke
* Ghost
* Aurora
* Bluecore
* Solar
* Inferno
* Quantum
* Bioflare
* Ion
* Molten
* Cryoflame
* Spectral
* Voidfire

---

## Weather Presets

The app includes environmental presets that remix the behaviour of the fire:

* Calm
* Storm
* Zero-G
* Cinematic
* Ion Fog
* Afterburner
* Cryo Drift
* Void Bloom

These presets adjust values such as intensity, wind, turbulence, gravity, reactivity, haze, aura, swirl, and sometimes fire mode.

---

## Capture and Sharing

Depending on browser support, AR Fire Lab can:

* Take a snapshot
* Record a short clip
* Save local presets
* Load local presets
* Export preset JSON
* Export diagnostic logs

Browser security may block canvas capture on some devices or when third-party AR/camera layers are involved.

---

## Troubleshooting

### Camera does not open

Try the following:

* Use `HTTPS` or `localhost`
* Check browser camera permissions
* Reload the page
* Press `Camera`
* Close other apps using the camera

### Marker will not lock

Try the following:

* Use the rear camera
* Print the marker on matte paper
* Avoid shiny screens and glare
* Keep the full black border visible
* Keep the marker flat
* Hold still for 2 seconds
* Move back until the marker fills roughly one third to two thirds of the scanner box
* Press `Scan Rescue`
* Enable `Scan Boost`

### Custom marker does not work

Try the following:

* Use `Marker IQ` to check the image
* Use a high-contrast asymmetric image
* Avoid repeated patterns
* Keep the generated card border visible
* Press `Make Strong`
* Press `Self Test`
* Use the printed image that created the `.patt` file

### Performance is slow

Try the following:

* Press `Optimize`
* Lower `Particle Budget`
* Lower `Haze`
* Lower `FX Depth`
* Turn off heavy FX packs
* Keep `Guardian` and `Auto Quality` enabled

### Screen goes black after switching camera

Reload the page once. The app attempts to preserve the last preset where possible.

---

## Browser Notes

AR Fire Lab depends on browser camera APIs and WebGL support.

Best results usually come from:

* A modern mobile browser
* Good lighting
* Rear camera
* Printed marker
* Stable internet connection for CDN scripts
* HTTPS hosting

Some features are browser-dependent:

| Feature         | Browser dependency              |
| --------------- | ------------------------------- |
| Camera access   | `getUserMedia` support          |
| Recording       | `MediaRecorder` support         |
| Barcode rescue  | `BarcodeDetector` support       |
| Wake lock       | Screen Wake Lock API support    |
| WebXR readiness | WebXR support                   |
| Focus assist    | Camera track capability support |

---

## Project Structure

```text
AR-Fire-Lab/
├── index.html
├── README.md
├── LICENSE
├── SECURITY.md
└── CODE_OF_CONDUCT.md
```

The main experience lives in `index.html`.

---

## Tech Stack

* HTML
* CSS
* JavaScript
* A-Frame
* AR.js
* WebGL
* Browser camera APIs
* Optional browser APIs such as MediaRecorder, BarcodeDetector, Wake Lock, and WebXR detection

---

## Development

This project is intentionally simple to run and modify.

No build step is required.

Edit:

```text
index.html
```

Then refresh the browser.

For local testing, use a static server:

```bash
python -m http.server 8000
```

For deployment, host the repo with any static hosting provider that supports HTTPS.

Good options include:

* GitHub Pages
* Netlify
* Vercel
* Cloudflare Pages
* Any HTTPS static server

---

## Suggested Roadmap

Possible future upgrades:

* True markerless WebXR hit-test placement
* Dedicated mobile calibration wizard
* More custom marker templates
* Saved marker library
* Better offline support
* PWA install mode
* Depth-aware fire placement
* Multi-marker scenes
* Hand gesture controls
* Exportable scene presets
* More audio-reactive fire modes
* Full documentation site
* Automated browser compatibility checks

---

## Safety Note

This is a visual AR experiment. It does not simulate real fire behaviour and should not be used for safety training, firefighting instruction, emergency planning, or real-world hazard modelling.

---

## Contributing

Contributions are welcome.

Ideas that fit the project:

* Better marker tracking
* More stable camera handling
* New flame modes
* New FX packs
* Accessibility improvements
* Mobile UI improvements
* Browser compatibility fixes
* Better documentation

Basic workflow:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test on desktop and mobile
5. Open a pull request

---

## License

This project is released under the MIT License.

See `LICENSE` for details.

---

## Author

Created by [kai9987kai](https://github.com/kai9987kai).

AR Fire Lab is part of an experimental creative coding workflow exploring browser AR, camera tracking, procedural effects, and interactive visual systems.

```
::contentReference[oaicite:1]{index=1}
```

[1]: https://raw.githubusercontent.com/kai9987kai/AR-Fire-Lab/main/README.md "raw.githubusercontent.com"
