# Delete your Plate Forge account and data

**Plate Forge** (package ID: `com.webstack.plateforge`)  
**Effective date:** 30 June 2026  
**Contact:** [turslv18@gmail.com](mailto:turslv18@gmail.com)

This page explains how to delete your data in **Plate Forge**. Core workout features work offline; optional online features (sign-in, premium cloud backup, coach linking, promo codes) store limited data in **Google Firebase** (project `plate-forge`).

## 1. Delete data on your device (no account required)

You can remove local training data without signing in or contacting us:

1. Open **Plate Forge** → **Settings**.
2. Delete individual workout plans, sessions, or training accounts you no longer need.
3. To remove **all** local app data: uninstall the app from your device.

This removes workout plans, sessions, goals, settings, and profile photos stored only on your phone or tablet.

## 2. Delete your online account (Firebase)

Use this if you signed in with **Google** or **email**, redeemed a **promo code**, used **premium cloud backup**, or used **coach–client linking**.

### Steps

1. (Optional) Open **Settings** → **Account** → **Sign out**.
2. Email [turslv18@gmail.com](mailto:turslv18@gmail.com) from the address linked to your account (if any).
3. Use subject line: **Plate Forge account deletion request**.
4. Include the **email address** you used to sign in, or state that you used **Google Sign-In** with that email.

We will process verified requests within **30 days**.

### What we delete

- Your **Firebase Authentication** account (Google or email sign-in, or anonymous ID if linked to your request)
- **Cloud backup** data in Firestore (`users/{uid}/backups`)
- **Subscription and promo** records in Firestore (`users/{uid}/subscription`)
- **Coach–client link** metadata associated with your account, where applicable

### What we do not delete through this request

- **Google Play** or **App Store** purchase and billing records — manage or cancel subscriptions in your store account (**Google Play** → **Payments & subscriptions**).
- **Analytics and crash** data already collected by **Google Firebase** or **AdMob** — turn off future collection in **Settings** → **Privacy & legal** → **Usage analytics**, and see [Google’s privacy tools](https://policies.google.com/privacy).

## 3. Delete some data without deleting your account

You can remove or limit data without closing your Firebase account:

| Data | How to remove or limit it |
|------|---------------------------|
| Local workouts and plans | Delete in the app or uninstall |
| Usage analytics | **Settings** → **Privacy & legal** → turn off **Usage analytics** |
| Ads personalization | Use Google’s ad privacy options when offered in the app or device settings |
| Premium subscription | Cancel in **Google Play** or **App Store**; premium features stop when the subscription ends |
| Cloud backup only | Email us to delete Firestore backups while keeping sign-in (same contact as above) |

## 4. Coach–client linking

If you are linked as a **coach** or **client**:

- **Client (mentee):** revoke the coach in **Settings** → **Account** before or as part of your deletion request.
- **Coach:** disconnect linked clients from **Settings** → **Training accounts**, then request account deletion if needed.

Local copies on each device remain until deleted in the app or the app is uninstalled.

## 5. Questions

For help with deletion or privacy: [turslv18@gmail.com](mailto:turslv18@gmail.com)

See also: [Privacy Policy](privacy-policy.md) · [Terms of Service](terms-of-service.md)
