# fileadeX Android 1.0.14 — build 32

- Membership cancellation and profile billing synchronization support both legacy Stripe subscription-level dates and current subscription-item billing dates. Missing dates are rejected before changing Stripe. Retrying an already accepted end-of-period cancellation does not introduce another renewal.
- Temporary billing refresh failures retain cached details with a clear Retry action. Subscription changes are blocked until billing can be refreshed, rather than treating stale details as verified.
- Lead, Contact and Account creation drawers support selecting, adjusting and previewing profile pictures/logos. Contact and Account editors now support uploads too. Uploads are validated before creating records; failed uploads preserve the drawer and do not create duplicate records. Pictures use the normal saved-record/list-cache flow.
- Successful Gmail and Outlook connections queue private in-app notifications after the integration is saved. Failed connections and OAuth-start requests do not announce success.
- Notifications cover core CRM changes, notes/documents, meetings, route changes, email submission, cancellation requests and completed/failed imports and scans. Unsaved staged photos, background reads, token refreshes and notification read-state changes do not create success notifications.
- The mobile notification feed refreshes while open and on entering the page. Header unread state, read timestamps and relative times understand the server notification envelope.
- Android notification-channel registration and visible provider payloads are prepared for configured push providers. Native Firebase client configuration is absent from the workspace, and phone-level push delivery is not claimed as verified. In-app notifications operate independently.

Validation: 426 mobile tests / 84 suites, TypeScript, targeted lint without errors and whitespace checks passed. Backend changes passed 2,063 tests / 206 suites; the additional upload-limit change passed its focused five-test suite. The API and billing worker were deployed with rollback backups, staged/live source-hash checks and successful production smoke checks.

Both channel APKs are verified for version/package, certificate continuity, embedded live API/payment/update-channel configuration, Maps-key presence, archive integrity and SHA-256 before manifest publication. Public GitHub asset digests/sizes and HTTPS availability are checked separately.

No real membership was cancelled, no real payment was made, and no actual customer email was sent during testing. A connected device was checked read-only and still had v1.0.12/build 30 installed. It was in use, so no app navigation, physical installation/popup or end-to-end Gmail/photo check was performed. This is not an iOS App Store update. Historic activities are not backfilled into notifications.

## SHA-256

- Production: `277da9e95a4845b362cfc02124e2b0325c192b5600bfe95f312392018c79be67`
- QA: `b7e7b3588d4bde16f8918309f4de4a94a241e33412358d16f2fe838d23b67ec5`
