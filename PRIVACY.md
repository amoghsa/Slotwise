# Slotwise — Privacy Policy

**Effective date:** 2026-06-07
**Last updated:** 2026-06-07

Slotwise (iOS and Android) is built privacy-first: **it has no accounts, builds no
profile of you on any server, and keeps your family's information on your
device.** This policy explains plainly what stays local, the few moments when
information leaves your device (and exactly what is — and is not — sent), and the
permissions the app uses.

## The short version

- **No accounts.** No sign-up, login, username, password, or server-side profile.
- **No tracking.** No analytics, no advertising, no crash/usage telemetry, and no
  third-party tracking SDKs.
- **Your family's data stays on your device.** Names, kids, caregivers, rules,
  activities, locations, and finalized plans are stored only in the app's private
  storage. We never receive them.
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

There are only four situations, all initiated by you:

### 1. Exporting your plan (calendar file)
When you tap **Export**, Slotwise generates a standard calendar file (`.ics`) and
hands it to your operating system's share sheet. **You** then choose where it goes
— Apple Calendar, Google Calendar, email, etc. Once you send that file to another
app or service, *that* service's terms apply to the copy you sent. Slotwise itself
does not transmit the file.

### 2. Finding nearby activities (Discover)
If you use **Discover**, the app requests public activity and event listings from
the Slotwise catalog service. To return relevant results, the app sends the
**search criteria you are filtering by** — which may include a child's **age**,
selected **interest categories**, a **search location and radius** (coordinates
you provided, not your live GPS), date range, and any **search text** you type.

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

### 3. Looking up a place by name (optional)
If you search for a location by name (for example, to set a venue or your home),
the **text you type** is sent to your platform's map service — **Apple Maps
(`MKLocalSearch`) on iOS** or **Google's geocoder on Android** — to look up
matching places and coordinates. Their privacy terms govern that lookup. Slotwise
does **not** access your device's current location or GPS, and requests no
location permission.

### 4. Opening a facility's registration page
From a Discover listing, tapping **Register** opens the facility's own website in
your browser or an in-app web view. That site is operated by the facility, not by
Slotwise, and its own privacy policy and terms apply.

## Permissions

| Permission | Used for | Notes |
|---|---|---|
| **Camera** (iOS & Android) | Snapping a flyer/schedule for on-device text recognition (OCR) | Images are processed **on your device** and never uploaded. |
| **Photos** | Choosing an existing flyer image for OCR | Uses the system **photo picker**; the app is not granted access to your photo library. |
| **Notifications** | Local "registration opens" reminders you set | **Local notifications only** — there is no push server. |

Slotwise does **not** request location/GPS, contacts, microphone, or calendar
write access.

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
*children's* activities, it has no accounts and collects nothing about anyone — adult
or child — on any server. The details you type stay on your device. The only
child-related information that ever leaves the device is the **anonymous filter
values** (such as an age number and interest categories) used to fetch public
Discover listings, as described above; these are not stored against an identity and
do not constitute a child profile.

## Third-party services

When you use the optional features above, these providers may process the related
request under their own privacy policies:

- **Apple Maps** (place search on iOS) — https://www.apple.com/legal/privacy/
- **Google** (geocoding on Android) — https://policies.google.com/privacy
- **Vercel** (catalog API hosting) — https://vercel.com/legal/privacy-policy
- **Turso** (catalog database) — https://turso.tech/privacy-policy
- The **facility/organizer website** you open to register — their own policy

Slotwise has no advertising or analytics SDKs.

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

Questions? Email **amogh.agrawal@boomi.com** or open an issue in this repository.
