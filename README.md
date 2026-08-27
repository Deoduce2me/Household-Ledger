# Household Ledger

**A simple, private budgeting app for couples — track your income, your
partner's and shared expenses, and see exactly what's left each month.**

Household Ledger is a straightforward monthly budget tracker built for two
people managing money together. It shows three numbers at a glance — money
coming in, money going out, and what's left over — then lets you list every
expense and tag each one as **yours, your partner's, or joint**, with running
totals per person.

### What it does

- **Income, expenses, and money left over** shown at the top at all times.
- **One clear list of expenses**, grouped by whose they are (you / partner /
  joint), each with its own category.
- **Add, edit, or delete** any item in seconds.
- **Optional budget targets** per category, so you can see where you're over or
  under what you meant to spend.
- **Saves automatically** on your device — no account needed.
- **Works offline**, and shows everything in **£ (GBP)**.
- **Back up or move your data** with Export / Import.

Your data stays on your own device and is never uploaded anywhere.

---

## Getting the app onto your phone

Because building an Android APK needs Google's Android tools, the easiest way to
get the finished `.apk` — with **nothing to install on your PC** — is to let
GitHub build it for you for free. Steps below.

### Option A — Build it free on GitHub (recommended, ~10 minutes)

You'll need a free GitHub account. No Android Studio, no downloads.

1. **Create a GitHub account** at https://github.com (free) if you don't have one.
2. Click the **+** at the top right → **New repository**.
   - Name it e.g. `household-ledger`.
   - Leave it **Public** or **Private** (either works).
   - Click **Create repository**.
3. On the new empty repo page, click **“uploading an existing file”**.
4. **Drag the contents of this folder** (all the files and folders you see here —
   `app`, `gradle`, `.github`, `gradlew`, `build.gradle`, etc.) into the upload
   area, so that `build.gradle` and `gradlew` sit at the **top level** of the
   repo. Then click **Commit changes**.
5. Go to the **Actions** tab. A run called **“Build Android APK”** starts
   automatically (3–5 minutes; the dot turns green when done).
6. Click that run → scroll to **Artifacts** → download **`HouseholdLedger-apk`**.
   Unzip it to get **`app-debug.apk`**.

That `app-debug.apk` is your app.

### Put it on your phone

1. Get `app-debug.apk` onto your Android phone (email it to yourself, or open the
   GitHub download link on the phone).
2. Tap the file. Android will ask to allow “install from unknown sources” — that's
   normal for apps not from the Play Store; allow it.
3. Install, and **Household Ledger** appears in your app drawer with its own icon.

Do the same on your partner's phone.

### Option B — Build on your own PC with Android Studio

Install **Android Studio** (free), choose **Open**, pick this folder, wait for it
to sync, then **Build → Build Bundle(s) / APK(s) → Build APK(s)**. The APK lands
in `app/build/outputs/apk/debug/app-debug.apk`.

---

## Good to know

- This is a **debug/test APK** — perfect for installing on your own phones and
  sharing with people to try. It is **not** the Play Store version yet (that
  needs a signed release build and a Play Console account).
- Your data is saved **on each phone** — it does not yet sync between phones.
  That syncing is the next big step if you take this further.
- App name, colour, and icon can all be changed easily — just ask.
