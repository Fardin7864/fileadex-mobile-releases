# fileadeX Android 1.0.10 — build 28

- CRM Email opens a compose drawer on the current screen, with the selected recipient and record prefilled, instead of navigating away.
- CRM Call saves an initiated activity against the selected lead, contact or account. Returning from the dialer opens call details for outcome, notes, optional duration and recording upload.
- Recordings link to the same activity; returning from the file picker preserves edits.
- Call connection and duration are not detected automatically and must be confirmed by the user. Closing keeps the initiated activity.
- Existing plan, scanner, import, email and CRM fixes remain included.

264 tests / 61 suites passed, with TypeScript and lint passing. Real-device calls and live provider delivery remain acceptance checks. Native version, signing, channel, Maps key presence, APK integrity and uploaded checksums are verified before activating manifests.

The Google unverified-app warning is not resolved by this APK: Google must approve the requested Gmail access scope. No Google approval is claimed. Use the production or QA APK matching your existing installation. Android requires installation approval.
