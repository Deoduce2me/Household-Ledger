# Household Ledger

**A simple, private budgeting app for families and friends who share money —
track income, split expenses between up to 4 people, and see what's left.**

Household Ledger is a straightforward monthly budget tracker for people who
share money — families, friends, housemates or partners. It opens with a short
welcome page, then shows three numbers at a glance (money in, money out, and
what's left) and lets you list every expense and tag who it belongs to.

### What it does

- **Income, expenses, and money left over** shown at the top at all times.
- **Up to 4 people, plus Joint** — choose how many people share the budget and
  name each one; every expense is tagged to a person or to shared "Joint".
- **One clear list of expenses**, grouped by person with running totals.
- **Add, edit, or delete** any item in seconds.
- **Three currencies** — switch between **£ GBP**, **₦ NGN**, and **$ USD** and
  everything reformats instantly.
- **Optional budget targets** per category, to see where you're over or under.
- **Saves automatically** on the device — no account needed.
- **Works offline**, and starts as a clean, empty slate.

Your data stays on the device and is never uploaded anywhere.

---

## Getting the app onto your phone

Because building an Android APK needs Google's Android tools, the easiest way to
get the finished `.apk` — with **nothing to install on your PC** — is to let
GitHub build it for you for free.

### Build it free on GitHub (~10 minutes)

1. **Create a free GitHub account** at https://github.com if you don't have one.
2. Click **+** (top right) → **New repository**, name it e.g. `household-ledger`,
   and click **Create repository**. (Set it **Private** if you'd rather the key
   below isn't public — see *Signing* section.)
3. On the empty repo page, click **“uploading an existing file”**.
4. **Drag the contents of this folder** (all files and folders — `app`, `gradle`,
   `.github`, `gradlew`, `build.gradle`, etc.) into the upload area, so that
   `build.gradle` and `gradlew` sit at the **top level** of the repo. Commit.
5. Go to the **Actions** tab — the **“Build Android APK”** run starts on its own
   (3–5 min; the dot turns green when done).
6. Open the run → **Artifacts** → download **`HouseholdLedger-apk`**, unzip it to
   get **`app-debug.apk`**. That's your app.

### Put it on your phone

Get `app-debug.apk` onto the phone (email it to yourself, or open the GitHub
download there), tap it, allow "install from unknown sources" when asked, and
**Household Ledger** installs with its own icon.

---

## Updating the app later

When the app changes, you don't rebuild from scratch — you just update the files
and GitHub rebuilds:

- **Small change (just the app screen):** replace `app/src/main/assets/index.html`
  in the repo (navigate into that folder → **Add file → Upload files** → drag the
  new `index.html`), then commit.
- **Bigger change (build settings, new files):** re-upload the whole folder's
  contents to overwrite everything.

Either way, committing triggers a fresh build in the **Actions** tab; download the
new APK when it's green.

---

## Signing

This project includes a **fixed test signing key** (`app/keystore.jks`, wired up
in `app/build.gradle`). Because every build is signed with the same key, each new
APK installs as a **proper update over the previous one** — no uninstalling.

- **One-time step:** the very first time you install a build made with this key,
  if you already had an older Household Ledger installed (signed with a different
  key), Android will refuse it with "App not installed". **Uninstall the old app
  once**, then install this one. After that, all future updates install over the
  top.
- **This is a TEST key**, committed for convenience — fine for sideloading and
  sharing with people to try. If your repo is **public**, anyone can download it,
  so set the repo to **Private** if that matters to you.
- **For the real Play Store**, you'll use a **separate, secret release key** that
  is kept out of the repo. That's a later step when you're ready to publish.

---

## Good to know

- This is a **debug/test APK** — great for your phones and for handing to people
  to try. The Play Store version is a later step (a signed release build + a Play
  Console account).
- Data is saved **on each phone** and doesn't sync between phones yet. Syncing is
  the next major feature if you take this further.
- App name, colours, icon, wording, currencies and number of people can all be
  changed — just ask.
