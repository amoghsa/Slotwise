# Slotwise — Privacy Policy

**Effective date:** 2026-06-07
**Last updated:** 2026-06-09

Slotwise (iOS and Android) is built privacy-first: **it has no accounts, builds no
profile of you on any server, and keeps your family's information on your
device.** This policy explains plainly what stays local, the few moments when
information leaves your device (and exactly what is — and is not — sent), and the
permissions the app uses.

## The short version

- **No accounts.** No sign-up, login, username, password, or server-side profile.
- **No advertising.** No ad SDKs and no selling of data, ever.
- **Anonymous usage analytics, which you can turn off.** Slotwise uses **Google
  Firebase Analytics** to understand how the app is used (which screens are
  visited, which features are tapped, and how long is spent) so we can improve it.
  These events are **anonymous and contain no names, schedules, or other personal
  details**. You can switch this off any time in **Settings → Privacy → Share
  anonymous usage data**.
- **Your family's data stays on your device.** Names, kids, caregivers, rules,
  activities, locations, and finalized plans are stored only in the app's private
  storage. They are **never** sent to us or included in analytics.
- **Location, only if you allow it.** Discover can use your device's location to
  show activities near you. It asks for the system location permission first; if
  you decline, Discover falls back to a home address you set or a city you type.
  Your location is used only to fetch nearby results — it is never stored or shared.
- **A few optional features make network requests** — finding nearby activities
  (Discover), looking up a place by name, and opening a facility's registration
  page. Each is described below, including exactly what is sent. None of them send
  your names, your plans, or any account identifier (there is no account).

## What the app stores (on your device only)

Everything you enter is stored locally in the app's private storage:

- Household name, time zone, and optional home label and coordinates
- Kids' names, colors, optional emoji, birth year, and interests
- Caregivers/drivers and their availability windows
- Seasons and their date ranges
- Family rules (limits, cut-off times, no-activity days, gaps)
- Activities, their candidate time slots, locations/coordinates, prep/travel times,
  and the assigned driver
- Which slot you chose for each activity, and any alternate plans
- Activities you saved from Discover and any registration reminders you set

This data stays in the app's sandbox. We — the developer — never see it.

## When information leaves your device

There are only five situations, all initiated by you:

### 1. Exporting your plan (calendar file)
When you tap **Export**, Slotwise generates a standard calendar file (`.ics`) and
hands it to your operating system's share sheet. **You** then choose where it goes
— Apple Calendar, Google Calendar, email, etc. Once you send that file to another
app or service, *that* service's terms apply to the copy you sent. Slotwise itself
does not transmit the file.

### 2. Finding nearby activities (Discover)
If you use **Discover**, the app requests public activity and event listings from
the Slotwise catalog service. To return relevant results, the app sends the
**search criteria you are filtering by** — which may include a child's or adult's
**age**, selected **interest categories**, a **city or postal/ZIP code you type**,
a **search location and radius** (from your device location if you allow it — see
§3 — otherwise a home address you set), date range, and any **search text** you type.

- These are sent as **anonymous query parameters**. There is no account, login, or
  identifier attached, and we do not build or keep a profile linked to you.
- Your **names, household details, rules, plans, and on-device data are never
  sent.** Discover only sends the filter values needed to fetch matching listings.
- Like any web request, our hosting provider (**Vercel**) and database (**Turso**)
  process the request and may retain standard, short-lived operational/security
  logs (such as IP address, timestamp, and the requested URL). These are not used
  to identify you or build a profile.
- The catalog itself is **read-only public content**. You cannot register, pay, or
  create an account through it.

### 3. Using your location for nearby results (optional)
Discover can use your device's **location** to show activities near you. The app
requests the system **"while using the app" location permission** first; you can
allow or decline:

- **If you allow it**, your current coordinates are used **only** to build the same
  anonymous geo search described in §2 (a latitude/longitude + radius). The location
  is used in the moment to fetch nearby listings and is **not stored on a server,
  not retained, and not shared**. There is no background or continuous tracking —
  Discover takes a single fix when you open it.
- **If you decline**, Discover falls back to a home address you set (or a city /
  postal code you type), or shows all areas. You can change the permission any time
  in your device Settings.

Separately, when you **search for a place by name** (e.g. to set a venue or your
home), the **text you type** is sent to your platform's map service — **Apple Maps
(`MKLocalSearch`) on iOS** or **Google's geocoder on Android** — to look up matching
places and coordinates, under their privacy terms.

### 4. Opening a facility's registration page
From a Discover listing, tapping **Register** opens the facility's own website in
your browser or an in-app web view. That site is operated by the facility, not by
Slotwise, and its own privacy policy and terms apply.

### 5. Emailing us about missing activities (optional)
If Discover has nothing for your area, you can tap **"Tell us what's missing"**.
This opens **your own email app** with a pre-filled draft to `slotwise@amoghsa.com`
containing the city/postal code and filters you were searching — you review and
send it yourself, and you can edit or delete anything first. The app does not send
email on its own, and the draft includes no names or on-device family data.

## Usage analytics (Google Firebase Analytics)

To understand how the app is used and where to improve it, Slotwise sends
**anonymous usage events** to **Google Firebase Analytics**. Aside from the optional
location use above (a single fix used in the moment for nearby results, never
retained — §3), this is the only ongoing data collection in the app, and you can
**turn it off** in **Settings → Privacy → Share anonymous usage data**.

- **What is sent:** event names and non-identifying attributes — for example, a
  screen name ("Discover"), a feature tag ("discover_filter_changed"), enum/category
  values (e.g. an interest category like "swimming", a reminder offset like "1d"),
  counts, and how long a screen was on-screen (dwell time). Firebase also collects
  standard mobile analytics signals such as a random app-instance identifier, device
  model, OS version, app version, and coarse region inferred from IP.
- **What is never sent:** your or your kids'/caregivers' **names**, your household
  label, your activities, your schedule/plans, exact locations, or any free-text you
  type. Analytics carries **no personal content** — only the anonymous categories
  above.
- **Processor:** Google processes this data as described in its privacy policy and
  the Firebase/Google Analytics for Firebase terms. We use it only in aggregate to
  improve Slotwise; we do not sell it or use it for advertising.
- **Your control:** the in-app toggle stops new events immediately. Analytics is
  independent of the app's core features — turning it off does not affect anything.

## Permissions

| Permission | Used for | Notes |
|---|---|---|
| **Camera** (iOS & Android) | Snapping a flyer/schedule for on-device text recognition (OCR) | Images are processed **on your device** and never uploaded. |
| **Photos** | Choosing an existing flyer image for OCR | Uses the system **photo picker**; the app is not granted access to your photo library. |
| **Notifications** | Local reminders you set: "registration opens" alerts and "before it starts" reminders for activities and watched events | **Local notifications only**, scheduled on-device from the device clock — there is no push server and no device token. |
| **Run at startup** (Android) | Re-arming your local event reminders after a reboot (Android clears scheduled alarms on restart) | No network; only re-schedules reminders you already set. |
| **Location** (iOS & Android) | Showing activities **near you** in Discover (optional; "while using the app") | A single location fix is used to fetch nearby results; **not stored or shared**. Decline and use a typed city / home address instead. |

Slotwise does **not** request contacts, microphone, or calendar write access, and
location is **optional** (used only for nearby Discover results, never tracked).

## On-device text recognition (OCR)

The optional "import from a photo" feature uses **Apple Vision (iOS)** and
**Google ML Kit (Android)** to read text from an image **entirely on your device**.
The image and the recognized text are not uploaded anywhere; nothing is committed
to your plan until you review and confirm it.

## Device backups

Like most apps, Slotwise's on-device data may be included in **your own device
backup** if you have backups enabled — **iCloud Backup on iOS** or **Google
backup on Android**. That backup belongs to you and is managed by Apple/Google
under their terms; **we never receive it**. You can disable or exclude app data in
your device's backup settings.

## Children's privacy

Slotwise is intended for use by **adults (parents and caregivers)**, not by
children, and is **not directed to children**. Although the app helps you plan
*children's* activities, it has no accounts and builds no profile of anyone — adult
or child — on any server. The details you type stay on your device. The only
child-related information that ever leaves the device is the **anonymous filter
values** (such as an age number and interest categories) used to fetch public
Discover listings, as described above; these are not stored against an identity and
do not constitute a child profile. The usage analytics described above measure how
the *app* is used (screens, taps, timings) and **do not include children's names or
any child profile**.

## Third-party services

When you use the optional features above, these providers may process the related
request under their own privacy policies:

- **Google Firebase Analytics** (anonymous usage analytics; can be turned off in
  Settings) — https://firebase.google.com/support/privacy and
  https://policies.google.com/privacy
- **Apple Maps** (place search on iOS) — https://www.apple.com/legal/privacy/
- **Google** (geocoding on Android) — https://policies.google.com/privacy
- **Vercel** (catalog API hosting) — https://vercel.com/legal/privacy-policy
- **Turso** (catalog database) — https://turso.tech/privacy-policy
- The **facility/organizer website** you open to register — their own policy

Slotwise has **no advertising SDKs**. Its only analytics is the anonymous Firebase
Analytics described above, which you can disable in Settings.

## Your choices and rights

Because your data lives on your device, you are in direct control of it: edit or
delete anything in the app, reset the app, or uninstall it (see
[DATA-DELETION.md](./DATA-DELETION.md)). Depending on where you live, you may have
rights under laws such as Canada's **PIPEDA** / **BC PIPA**, the EU/UK **GDPR**, or
California's **CCPA/CPRA**. Since we hold no account or profile about you, most such
requests are satisfied by managing the data on your own device; for anything else,
contact us below.

## Changes to this policy

If a future version adds any feature that sends or stores additional data off the
device, we will update this policy and clearly disclose it in the app **before**
that feature is enabled. We will not silently add tracking.

## Contact

Questions? Email **slotwise@amoghsa.com** or open an issue in this repository.
