# fileadeX Android 1.0.9 — build 27

- Faster Android scanner preview pacing, while preserving the fixed card guide, manual orientation, green detection feedback and framed capture.
- Account-scoped plan caching and background refresh. Restricted features open the plan drawer directly without an intermediate checking or unlock page.
- Closing the plan drawer returns to the originating screen. A single root overlay avoids competing native upgrade dialogs and blocked navigation.
- Existing import, email, CRM, profile and FREE / PRO corrections remain included.

257 mobile tests passed, with TypeScript and lint checks passing. Native package/version, signing certificates, update channel configuration, Maps key presence, SHA-256 and ZIP integrity are verified before publishing the update manifests.

The plan drawer was also tested in the iOS simulator. Android camera frame rate and capture alignment still require physical-device acceptance testing; preview timing is a target, not a guaranteed device frame rate.

Use the production APK for production installations and the QA APK for QA installations. Android requires approval to install the update. This release does not update the App Store.
