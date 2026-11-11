# HuskTech: Coconut Husk Maturity Classifier

HuskTech is an Android app that looks at a photo of a coconut husk and tells you its
maturity stage: **Immature**, **Mature** or **Overmature**. It works fully offline, on the phone.

## Download

👉 **[Download the latest version (HuskTech-v4.apk)](../../releases/latest)**

Open the link on your Android phone, then tap **HuskTech-v4.apk** under *Assets*.

## How to install

1. Download `HuskTech-v4.apk` (about 84 MB).
2. Tap the downloaded file (in Chrome's downloads or the **Files** app).
3. If Android asks, allow **"Install unknown apps"** for Chrome / Files, then go back and tap **Install**.
4. If **Google Play Protect** warns about an unknown app, tap **More details → Install anyway**.
   This appears because the app is not on the Play Store; it is a student thesis project.

Requires Android 5.0 or newer. Camera permission is only asked for when you use Live Camera.

## How to use

- **Live Camera**: point the camera at a husk; the stage updates live. Tap **Capture** to keep a result.
- **Gallery**: pick a photo you already took. **Batch**: analyse many photos at once.
- Keep the husk **in the centre** of the photo and fill most of the frame. Close-ups of the
  inside fibres work best. A plain background is **not** required.

The app can answer in five ways:

| Result | Meaning |
|---|---|
| Immature | Husk not fully developed: pale fibres, high moisture |
| Mature | Ideal stage: fully developed fibres |
| Overmature | Past the ideal stage: dark, dry or degraded fibres |
| Uncertain | A husk was found, but the photo is unclear or the stage is borderline: take another photo |
| Rejected | No coconut husk was recognised in the photo |

The **Strictness** slider makes the app more lenient or more strict about giving an answer.

## Accuracy (tested on photos the model never saw)

| Test | Result |
|---|---|
| Close-up husk photos (169) | 96.4% correct |
| Studio husk photos (69) | 95.7% correct |
| Husks placed on unseen backgrounds (276) | 85.9% correct |
| Non-husk images correctly rejected (1,910) | 98.7% |

Accuracy on outdoor photos with a known stage has not been measured yet.

## Version history

- **v4** (2026-11-11): retrained with labelled close-up photos; much better on close-ups.
- **v3** (2026-11-09): new model with a separate husk check; works on real backgrounds,
  rejects non-husk photos, adds the "Uncertain" result.
