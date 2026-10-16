# fileadeX Android 1.0.15 — build 33

- Empty Leads, Contacts and Accounts lists show the supplied illustration and a compact Add action opening the corresponding creation drawer in place. Searches that match no existing records retain search/filter guidance.
- Integrations use the supplied Gmail, Outlook, Google Calendar and Apple Calendar artwork with consistent sizing.
- Agenda & Calendar checks saved provider connections, requests external calendar events, refreshes on returning to the page, and shows a five-event recent list. A connected but empty calendar offers Add events in the existing meeting drawer instead of another Connect prompt. Request failures show retry guidance rather than a false empty state. External events do not expose local appointment status changes.
- The setup celebration is saved before display rather than on dismissal. It triggers only on an observed incomplete-to-complete transition, not when opening an already-completed account. Existing seen markers are respected; account switches and repeated status changes cannot replay it on the installation.

Validation: 447 automated mobile tests / 87 suites, TypeScript and targeted lint. Both signed channel APKs are checked for package/version, certificate continuity, embedded production API and matching update channel, native Maps-key presence, archive integrity and SHA-256 before manifest publication.

No backend changes or App Store publication are required for this Android release. The user's live Google Calendar connection, physical update popup and complete device journeys have not been retested for this build. No live payments or customer communications were performed.

## SHA-256

- Production: `2aef6152c9d34ca0bdcf97f43fa8ade1f787ffadc37d7b345c6c1b2b6fbb613c`
- QA: `9401a55e70de8fc38adbbe72c1b1b329b146e94cc9a792e212a851dadd5478a5`
