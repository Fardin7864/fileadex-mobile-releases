# fileadeX Android 1.0.16 — build 34

- Scanner preview now uses CameraX PreviewView in performance mode instead of converting, rotating and uploading full-resolution bitmaps to an ImageView for every visible frame. Camera rendering is no longer paced by card-analysis work or a software frame limiter.
- Card detection reads a small, rotated luminance grid from a lower-resolution YUV stream. Keep-only-latest backpressure and independent analysis throttling avoid a growing frame queue.
- Native preview and analysis share a CameraX viewport. The full-frame FIT_CENTER presentation and fixed manual orientation guide remain; detection still drives alignment/green readiness feedback.
- Capture snapshots the visible native preview only when requested, rejects guides outside the camera content and not-yet-rendered black frames, and saves JPEGs on a separate executor. Camera-generation guards prevent stale sessions updating the guide after leaving/reopening the scanner.
- Includes all corrections from build 33.

Validation: 448 mobile tests / 87 suites, TypeScript, targeted lint and native release compilation passed. Both APKs are verified for package/version, signing-channel continuity, embedded live API/payment/update configuration, native Maps-key presence, ZIP integrity and SHA-256 before manifest publication.

No USB device was connected during this release. Actual preview FPS/latency, physical capture alignment and low-end device performance have not been measured or physically verified. This removes the identified CPU-rendering bottleneck; it does not promise a particular frame rate on every camera or under low lighting. No backend deployment or iOS App Store publication is included.

## SHA-256

- Production: `46aa54e174f268c3f47b3d10bd7c2a1eb7488c9e91b88bf4216b55ee1d0fdb7c`
- QA: `c9821af8ba45a62767566f7b8655a62cffdd6e543adcfce058c855e7e790a4ed`
