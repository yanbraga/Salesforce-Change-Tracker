# Privacy Policy — Salesforce Change Tracker

**Last updated:** June 2026

Salesforce Change Tracker ("the extension") is a developer tool that lists the
metadata you changed in your own Salesforce org and generates a `package.xml`
or a text report from it.

**The extension does not collect, store, sell, transmit, or share any personal
data or user information with the developer or any third party.** All processing
happens locally, between your browser and your own Salesforce org. There are no
external servers, analytics, tracking, or third‑party APIs of any kind.

## Data the extension accesses

The extension only accesses the following data, and only to provide its core
functionality:

- **Salesforce session cookie (`sid`).** Read from the org tab you have open and
  used as a Bearer token to authenticate requests to **your own org's** REST and
  Tooling API. This value is never stored, logged, cached, or transmitted
  anywhere other than to your own Salesforce org. It is held in memory only for
  the duration of a single request.

- **Your user identity.** The extension calls your org's `chatter/users/me`
  endpoint to obtain your user Id (and your display name and org label, shown in
  the popup). This is used to scope results to the changes **you** made. It is
  not stored or sent anywhere outside your org.

- **Metadata change records.** Using the Tooling API, the Data API and the
  `SetupAuditTrail` object, the extension queries the metadata that was modified
  in the selected period (e.g. Apex classes, flows, fields, validation rules,
  permission sets, reports). These records are fetched directly from your org and
  displayed inside the extension popup. They are never stored, cached, or sent to
  any external server.

- **Your preferences.** The sections you choose to track, the output mode, the
  API version, and the selected date range are saved locally on your device using
  Chrome's `storage` API (`chrome.storage.local`). This data never leaves your
  device.

## Why the extension requests each permission

- **`activeTab` / `scripting`** — to run the metadata queries in the context of
  the Salesforce tab you have open.
- **`cookies`** — to read your org's session cookie so requests can authenticate
  as you.
- **`storage`** — to remember your preferences between sessions, locally.
- **Host permissions** (`*.salesforce.com`, `*.lightning.force.com`,
  `*.salesforce-setup.com`) — to call the REST/Tooling API of the Salesforce org
  you are signed in to.

## Data we do not collect

The extension does not collect or process: browsing history, personally
identifiable information beyond what is described above, location, financial
information, health information, or any data from sites other than your
Salesforce org. Nothing is ever sent to the developer.

## Data retention

The extension keeps no remote data. The only persisted data is your local
preferences, which remain on your device until you change them, clear the
extension's storage, or uninstall the extension.

## Changes to this policy

If this policy changes, the "Last updated" date above will be revised and the
updated policy will be published with the extension.

## Contact

For any questions about this privacy policy, contact:

**yanbraga11@gmail.com**
