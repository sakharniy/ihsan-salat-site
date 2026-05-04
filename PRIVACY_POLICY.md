# Privacy Policy — Ihsan Salat

**Effective date:** 2026-05-04
**Last updated:** 2026-05-04
**Developer contact:** matikmay@gmail.com

This Privacy Policy describes how the **Ihsan Salat** mobile application (the "App") handles your information.

## TL;DR

- The App is **offline-first**. All your data — settings, prayer counter, selected city — stays on your device in local storage (Hive). Nothing is sent to a server we operate, because we do not operate one.
- We **do not** collect, store, or transmit personal data ourselves. There are no accounts, no analytics, no telemetry.
- Two third-party SDKs run inside the App and have their own data practices:
  - **Google AdMob** serves ads and may use device identifiers and ad-related data per Google's policy.
  - **Google Mobile Ads SDK** initialisation contacts Google's servers.

## Information used by the App

### Location (optional, on-device only)

If you grant location permission, the App reads your approximate or precise coordinates **once during onboarding** to find the nearest city in our 30-city catalogue and again only if you tap "Detect my city" in the city picker. Coordinates are **not stored** — only the chosen city ID (e.g. `tashkent`) is saved locally.

You can revoke location permission in your OS settings at any time. The App will still work — you can pick a city manually.

### Notifications (local, on-device only)

The App schedules local notifications for the five daily prayer times based on your selected city. Scheduling happens entirely on your device using the OS notification system. **No notification content is sent over the network.**

On Android 12+ we request the `SCHEDULE_EXACT_ALARM` permission to deliver notifications at exact times. If denied, notifications still arrive but with up to 15 minutes of delay (Android system limitation).

### Local storage

The following is stored on your device using Hive (encrypted at rest by the OS sandbox):

- Selected language, calculation method, madhab, time format, theme, city
- Tasbih (prayer beads) counter values
- Onboarding completion flag

This data **never leaves your device** and is deleted when you uninstall the App.

## Third-party services

### Google AdMob

The App displays banner ads on the Prayer Times and Readings screens, and a full-screen interstitial ad approximately every 8 in-app navigations. Ads are served by **Google AdMob**.

AdMob may collect data including but not limited to:
- Device identifiers (Advertising ID on Android, IDFA on iOS if granted)
- IP address
- Coarse location derived from IP
- App usage events relevant to ad delivery

This data is collected and processed by Google under the [Google Privacy Policy](https://policies.google.com/privacy) and the [Google AdMob & AdSense Policy](https://support.google.com/admob/answer/7686480). We have no access to it.

You can opt out of personalised advertising:
- **iOS:** Settings → Privacy & Security → Tracking → toggle off "Allow Apps to Request to Track" and revoke for Ihsan Salat.
- **Android:** Settings → Google → Ads → "Opt out of Ads Personalisation" or reset Advertising ID.

We do **not** integrate the App with any other ad networks, analytics SDK, crash-reporting SDK, or social login.

## Data we do NOT collect

- We do not have user accounts.
- We do not collect names, emails, phone numbers, or addresses.
- We do not track you across other apps.
- We do not sell or share data with brokers.
- We do not transmit your prayer history, location, or settings anywhere.

## Children's privacy

The App is not directed at children under 13 (or the equivalent age in your jurisdiction). We do not knowingly collect data from children. If you are a parent and believe your child has provided personal data through the App's third-party ad SDK, contact us — we will instruct Google AdMob to flag the device.

## Permissions summary

| Permission | Why it's requested | Required? |
|---|---|---|
| `ACCESS_COARSE_LOCATION` / `ACCESS_FINE_LOCATION` (Android), Location (iOS) | Detect nearest city for prayer times | Optional |
| `POST_NOTIFICATIONS` (Android 13+), Notifications (iOS) | Daily prayer reminders | Optional but app is much less useful without it |
| `SCHEDULE_EXACT_ALARM` (Android 12+) | Deliver reminders at the exact prayer time | Optional; falls back to inexact alarms with ~15 min delay |
| `RECEIVE_BOOT_COMPLETED` (Android) | Restore scheduled reminders after device reboot | Required for reliability |

## Changes to this policy

We may update this Privacy Policy as the App evolves (e.g. when adding paid subscriptions or new third-party services). Changes take effect when posted at this URL with a new "Last updated" date. Material changes will be flagged in-app on next launch.

## Contact

Questions, complaints, or data requests:

- Email: **matikmay@gmail.com**
- Subject line: *"Ihsan Salat — privacy"*

---

*Russian version: see [PRIVACY_POLICY_RU.md](PRIVACY_POLICY_RU.md).*
