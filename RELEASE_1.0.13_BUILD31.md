# fileadeX Android 1.0.13 — build 31

- Business Profile website and social links automatically add `https://` when missing. Existing HTTP/HTTPS links are preserved; invalid links remain rejected.
- Compact Remove controls clear profile-photo and company-logo previews. Changes are applied on Save, without changing already-ordered card artwork. Explicitly removed public-profile photos no longer fall back to the login avatar.
- Delivery checks street/city/state/ZIP and the tax quote before advancing, with inline address errors. Provider failures do not silently bypass validation.
- Card-payment confirmation uses a bounded server-confirmation attempt instead of a long blocking polling loop. Pending confirmation continues on the Digital Card screen; pending is not displayed as confirmed payment.
- Ordered-card previews use saved artwork, including job title, company and logo. Multiple accepted cards can be cycled by swiping or an accessible next-card control. Accepted artwork is locked against edits.
- The top system status-bar area uses the primary brand blue across screens and native modals.

Validation: 418 mobile automated tests / 83 suites and TypeScript passed. Relevant lint checks had no errors. Related backend changes passed 2,019 automated tests / 199 suites and production smoke checks. The schema-only payment-confirmation/artwork-lock migration passed database trigger regression tests without modifying customer order/payment rows.

Both APKs are checked for package/version, channel signing certificate, embedded live API/update/payment configuration, native Maps-key presence, ZIP integrity and SHA-256 before update-manifest publication. GitHub asset digests and public download availability are checked separately.

The USB device was disconnected for this release. No physical-device popup/install check, full real-device card checkout, or live purchase was performed. Automated checks do not establish real payment completion or perfect postal deliverability. No iOS App Store update is included.

Use the production or QA APK matching the installed certificate. Android requires installation approval; this is not a silent update. Legacy QA installations that predate the separate QA update channel still require a manual installation of the matching QA APK once.

## SHA-256

- Production: `b882b61d37f136bd99ab53f79d7b5616c0521d25efdf631f1e1e0f87a40dff5c`
- QA: `69e30e7c2041f49045847b5e131346319fabc50a27f69a0a15db7bd11c81dad7`
