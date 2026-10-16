# fileadeX Android 1.0.17 — build 35

- Corrects the black scanner-preview regression reported after build 34. CameraX now uses its compatible TextureView-backed preview within React Native's composited hierarchy instead of a separate SurfaceView.
- Native CameraX subtree layout requests explicitly measure and lay out the preview host. This handles the preview child being inserted after React Native has completed its own layout.
- A preview-start timeout reports a recoverable error rather than remaining silently black if streaming cannot begin.
- Retains the native preview, lightweight YUV detection, fixed guide/manual orientation, green alignment feedback, separate JPEG worker and visible-preview crop safeguards.

Validation: 449 automated mobile tests / 87 suites, TypeScript and targeted lint passed. Both channel APKs are checked for package/version, signature continuity, live API and update-channel configuration, native Maps-key presence, ZIP integrity and SHA-256.

Device verification: reproduced build 34's black preview on the connected CPH2801 while Android reported an active fileadeX rear-camera client. Installed the matching QA build 35 using an in-place update without clearing data. Confirmed visible live preview, successful manual front capture with a nonblank cropped image, reopening for the back side, camera reset and background/resume with a visible preview. No OCR upload or CRM record creation was performed using the test scene. Screenshots are retained privately, not included in public releases. Device frame rate and real-card OCR accuracy were not benchmarked. No backend or iOS App Store change is included.

## SHA-256

- Production: `a2201cada07f7c71b0da1b1342e011b94cfe11c7cc8598d2f2a47ff0ebc86eb2`
- QA: `2b89978c5aa23568a9bdd4adb763ce16ee69fe68c4cfa266f05b1e1780d76664`
