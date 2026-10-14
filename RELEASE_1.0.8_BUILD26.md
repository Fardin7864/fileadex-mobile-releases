# fileadeX Android 1.0.8 — build 26

- Import opens immediately, with access checking inside the drawer.
- Import results use one main action and smaller secondary controls. Skipped rows clearly explain why no new records were added.
- Smart CRM counts use refreshed server totals rather than a cached first-page list.
- Contextual CRM suggestions open a relevant AI Sales Manager conversation.
- CRM email shortcuts open the native fileadeX composer with recipient and record context, plus the active connected From address.
- Icon-based Inbox, Sent, Drafts and Failed folders match web email activity. Incoming Gmail/Outlook mailbox synchronization is not available yet.
- Sending requires an active email connection. Successful record-linked sends create a CRM email activity; post-delivery logging problems show a warning instead of encouraging another send.
- Existing imports, FREE / PRO gates, scanning, profile and CRM corrections remain included.

253 mobile tests and 1,885 backend tests passed, with TypeScript/lint checks passing. Native Android versions, signatures, Maps key presence, channel configuration and APK integrity are checked before activating the manifests. Automated and build checks do not replace live-account and physical-device acceptance testing.

Use production APKs for production installations and QA APKs for the separate QA channel. Android requires installation approval. No iOS/App Store release is included in this Android update.
