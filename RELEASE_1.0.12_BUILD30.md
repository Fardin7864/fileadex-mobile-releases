# fileadeX Android 1.0.12 — build 30

- Leads, Contacts and Accounts lists display saved profile pictures or logos, with initials when no usable photo is available.
- Subscription & Billing has a cleaner layout and a Current plan badge on the active plan card. Existing PRO subscriptions open on their saved billing interval, and past-due subscriptions offer billing management instead of duplicate checkout.
- The live backend correction allows FREE accounts to upgrade to PRO without being incorrectly blocked by their FREE subscription record. Existing paid-subscription protections remain in place.
- Guided sales journey step 2 recognizes saved Business Profile details rather than requiring separate AI business-context answers.
- fiX has an input microphone for voice-to-text drafting, without the old Chat/Voice toggle or New chat button. Dictation does not automatically send messages.

Validation: 393 mobile automated tests across 79 suites passed, along with TypeScript and targeted lint (no errors). Both release builds passed native package/version, signing certificate, embedded API/update-channel/payment configuration, Maps-key presence, archive integrity and SHA-256 checks. Related live backend corrections passed 1,993 automated tests and readiness checks. Automated checks do not establish live paid checkout, provider approval, or every physical-device user journey.

The matching QA release APK was installed over the connected Android device's existing build without clearing app data. Build 30 launched in the foreground with no AndroidRuntime/ReactNativeJS errors in the launch log check. This is an install/launch check, not full user-journey acceptance testing.

Use the production or QA APK matching your installed signing channel. Android requires installation approval; the update is not silent. This release does not publish an iOS App Store update.

## SHA-256

- Production: `e24698bed05bd920df3facef62eabbe43b5f3da0cd48b3c84a2d13578a132b3e`
- QA: `0bea506820402379dd072d2abfea95cb543b5b2cd4eedabdf13276c3bcff4591`
