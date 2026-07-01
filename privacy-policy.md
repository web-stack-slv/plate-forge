# Privacy Policy

**Plate Forge** (package ID: `com.webstack.plateforge`)  
**Effective date:** 26 June 2026  
**Contact:** [turslv18@gmail.com](mailto:turslv18@gmail.com)

This Privacy Policy explains how Plate Forge (“we”, “us”, “the app”) handles information when you use our mobile application on Android and iOS.

## 1. Summary

- **Training data stays on your device.** Workout plans, sessions, goals, and progress are stored locally. We do not operate a user account server for the core app.
- **Analytics and crash reports are optional.** You choose on first launch and can change the choice in Settings. We do not send exercise names, weights, reps, or training notes to analytics.
- **The free version shows ads** served by Google AdMob. Where required by law, Google’s User Messaging Platform (UMP) asks for ad privacy choices separately from analytics.
- **Optional premium subscription** removes ads and unlocks coach–athlete cloud sync, a higher training-account cap, and mentee training reports. Purchases are processed by Google Play or the App Store, not by us directly.

## 2. Information stored on your device

The app stores the following locally on your phone or tablet (ObjectBox database and app files):

- Workout plans, schedules, and completed training sessions
- Custom exercises and exercise preferences
- Training goals, gamification progress, and achievements
- App settings (language, theme, units, rest timers, analytics preference)
- Multiple training profiles (“accounts”) if you create them
- Optional profile photos you choose for a training account (saved in app storage)
- **Coach-tagged training data** on a mentee’s main account when linked to a coach (programs and sessions the coach manages, distinguished from personal programs that stay local-only)

This data is not uploaded to our servers as part of normal offline use. **Personal** programs and sessions on a linked mentee account are not uploaded. Only **coach-tagged** rows may be written to the mentee-owned cloud shard when the athlete is connected to a coach and sync runs. Uninstalling the app or using in-app delete flows removes the corresponding local data.

## 3. Optional online features (premium, coach linking, and promo codes)

When you use premium, coach linking, or promo features, limited data is sent to **Google Firebase** (project `plate-forge`):

- **Firebase Authentication:** Google, Apple (when enabled), email/password, or anonymous sign-in for promo redemption. A stable user ID is used for subscription validation and coach–mentee sync when you sign in.
- **Cloud Functions:** validate subscription purchases (when enabled) and redeem promo codes server-side.
- **Cloud Firestore:**
  - Promo code metadata and subscription records under `users/{uid}/subscription`
  - **Coach–mentee shard** under `users/{menteeUid}/linkedAccounts/{linkId}/shard/current` — JSON snapshot of **coach-tagged** training data only (plans, sessions, schedule state managed by the linked coach). Personal programs on the mentee device are not included.
  - Link metadata (`coachUid`, account IDs, `status`, bootstrap state) under `users/{menteeUid}/linkedAccounts/{linkId}`
  - Invite documents under `invites/{token}` while a coach shares a link
  - **Legacy full-device backups** under `users/{uid}/backups/current` may exist from earlier builds or internal QA; this is **not** a current product feature and is not offered in the app UI for end users.

**Free users** who do not use premium or coach linking do not upload training content to Firestore. Linked **free mentees** may push coach-tagged workouts to their own shard; **coach-side** cloud pull requires an active premium subscription on the coach’s main account.

Promo codes are created manually by the developer for testers or friends; they are not public self-service registration.

### Coach linking and consent

- A mentee must **accept** an invite before any coach-tagged data is shared.
- While linked, the coach may manage coach-tagged programs; the mentee may train and log results on those programs.
- **Revoke** or **disconnect** stops future shard writes. The coach may retain a local copy on their device.
- If the coach’s **premium subscription ends**, cloud links are revoked on the coach’s next app launch (after confirmation); the mentee is notified that the coach link ended. Local training data on both devices remains unless the user deletes it.

## 4. Optional usage analytics and crash reporting

If you **allow analytics**, we use **Google Firebase Analytics** and **Firebase Crashlytics** to understand how the app is used and to fix crashes. Collection is disabled until you opt in (or until you enable the toggle in Settings → Privacy & legal).

**Events we may send (examples):**

- `onboarding_completed` — number of goals selected
- `session_started` — source label and planned set count (numbers only)
- `session_completed` — completed set count and exercise count (numbers only)
- Crash and error diagnostics (stack traces, device/OS metadata)
- Screen navigation in release builds (screen names, not training content)

**We do not send:** exercise names, weights, reps, times, distances, workout notes, or other training content.

If you choose **Continue without analytics**, Firebase Analytics and Crashlytics collection remain off.

Google’s privacy information: [Google Privacy Policy](https://policies.google.com/privacy).

## 5. Advertising (free version)

Plate Forge may show **Google AdMob** advertisements:

- A banner during idle/rest moments in an active workout
- A skippable full-screen ad after you finish a workout (when ads are eligible)

AdMob and its partners may collect device identifiers, ad interaction data, and similar information to deliver and measure ads, subject to your choices and applicable law. In the EEA, UK, and other regions where required, **Google UMP** presents ad privacy options. You can review ad privacy choices from Settings when Google requires it.

Google AdMob information: [AdMob & user data](https://support.google.com/admob/answer/6128543).

## 6. Permissions

- **Camera / photo library** — only if you set a training account avatar from the camera or gallery. Images are stored locally.
- **Internet** — used for ads, optional analytics/crash reporting, in-app purchases, promo redemption, app update checks, and opening legal links. Core workout features work offline.

## 7. Legal bases (EEA / UK / similar regions)

- **Local training data:** processed on your device to provide the service you request; we do not receive it.
- **Analytics and crash reporting:** your **consent** (you can withdraw it in Settings).
- **Advertising:** your **consent** or other lawful basis as presented by Google UMP and applicable law.

## 8. Data retention

- Local training data remains until you delete it in the app, delete a training account, or uninstall the app.
- Analytics and crash data retained by Google are governed by Google’s policies and your consent settings.

## 9. Your rights

Depending on your location, you may have rights to access, correct, delete, or restrict processing of personal data, or to object or withdraw consent.

- **Training data:** manage or delete in the app (e.g. delete plans, accounts, or uninstall).
- **Analytics:** toggle off in Settings → Privacy & legal → Usage analytics.
- **Ads:** use Google’s ad privacy options when offered, or subscribe to premium for an ad-free experience where available.
- **Premium:** manage or cancel subscriptions through Google Play or the App Store account settings.

To exercise rights related to data processed by Google, see Google’s tools and policies. For questions about this app, email [turslv18@gmail.com](mailto:turslv18@gmail.com).

## 10. Children

Plate Forge is not directed at children under 13 (or the minimum age required in your country). We do not knowingly collect personal information from children.

## 11. International transfers

Firebase and AdMob may process data on servers outside your country, including the United States, under Google’s standard contractual and security measures.

## 12. Changes

We may update this policy. The effective date at the top will change. Continued use after an update means you accept the revised policy where permitted by law.

## 13. Contact

Questions about this Privacy Policy: [turslv18@gmail.com](mailto:turslv18@gmail.com)

---

[Terms of Service](terms-of-service.md)
