# fileadeX Android 1.0.6 — build 24

- Profile-photo preview in the Edit Digital Card drawer.
- Selected profile images normalized to cached JPEGs with matching upload MIME types; single-image uploads use native multipart transport.
- Text-only business-profile saves use JSON instead of multipart.
- Interrupted read requests receive bounded retries. Writes are not blindly retried, avoiding duplicate activities and other changes.
- A failed follow-up refresh no longer reports a successful photo upload or business-profile save as failed.
- Card processing shows a web-style progress bar rather than percentage text.
- Retains the fiX launcher icon and fixed, manually rotated scanner guide.

Production and QA use separate signing certificates and update manifests. Install the matching channel; Android requires installation approval.

Validation: 215 tests across 50 suites, TypeScript and lint passed. Signature, package/version, embedded configuration and archive-integrity checks are performed on the release artifacts. Physical-device upload/camera acceptance testing has not been claimed.
