# Delete your Plate Forge data

**Plate Forge** (package ID: `com.webstack.plateforge`)  
**Effective date:** 14 July 2026  
**Contact:** [turslv18@gmail.com](mailto:turslv18@gmail.com)

Plate Forge does **not** offer sign-in accounts. Training profiles and workouts stay on your device. Optional online data is limited to anonymous premium or promo validation in **Google Firebase** (project `plate-forge`).

## 1. Delete data on your device (no contact required)

1. Open **Plate Forge** → **Settings**.
2. Delete individual workout plans, sessions, or training profiles you no longer need.
3. To remove **all** local app data: uninstall the app from your device.

This removes workout plans, sessions, goals, settings, and profile photos stored only on your phone or tablet.

## 2. Delete online data in the app (premium or promo)

If you used **premium** or redeemed a **promo code**, you can delete the small online record linked to this install:

1. Open **Settings** → **Privacy & legal**.
2. Tap **Delete online data**.
3. Read the confirmation and confirm.

This removes anonymous premium/promo records from Firebase for the current install. It does **not** delete workouts on your device and does **not** cancel Google Play or App Store billing.

If you reinstalled the app or no longer have the same anonymous session, use the email option below.

## 3. Email fallback (reinstall or help)

Email [turslv18@gmail.com](mailto:turslv18@gmail.com) if in-app deletion is not available.

1. Subject line: **Plate Forge data deletion request**
2. Include one of:
   - Google Play or App Store purchase email (premium)
   - Promo code you redeemed (if known)
   - Approximate date of purchase or redemption

We will process verified requests within **30 days**.

### What we delete on request

- **Firebase Authentication** anonymous ID (when identifiable)
- **Subscription mirror** in Firestore (`users/{uid}/subscription`)
- **Promo redemption reference** for that anonymous ID

We do **not** store workout content, emails, or names on our servers.

### What we do not delete through this request

- **Google Play** or **App Store** purchase and billing records — cancel in your store account.
- **Analytics and crash** data held by **Google Firebase** or **AdMob** — turn off future collection in **Settings** → **Privacy & legal** → **Usage analytics**.

## 4. Delete or limit data without a full request

| Data | How to remove or limit it |
|------|---------------------------|
| Local workouts and plans | Delete in the app or uninstall |
| Online premium/promo mirror | **Settings** → **Privacy & legal** → **Delete online data** |
| Usage analytics | **Settings** → **Privacy & legal** → turn off **Usage analytics** |
| Ads personalization | Google ad privacy options in Settings or device settings |
| Premium subscription | Cancel in **Google Play** or **App Store** |

## 5. Questions

[turslv18@gmail.com](mailto:turslv18@gmail.com)

See also: [Privacy Policy](privacy-policy.md) · [Terms of Service](terms-of-service.md)
