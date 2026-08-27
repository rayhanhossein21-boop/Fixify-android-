# Fixify - All Services. One Place.

**Fixify** is a production-grade, global on-demand multi-service Android application built with **Jetpack Compose** and modern Android architecture. Fixify connects clients with verified professionals and specialists across all industries worldwide with guaranteed 8% multi-currency escrow protection, real-time quote generation, interactive scheduling, custom bids, and dispute resolution.

---

## Key Features

- 🛡️ **Dual Account Onboarding & Authentication**:
  - Email/password authentication with remember me, secure password recovery, and input validation.
  - Dedicated sign-up workflows for **Clients / Customers** (post jobs, book appointments, fund escrow) and **Service Providers / Workers** (set hourly rates, select skill presets, publish pro directory profiles).
  - 1-tap demo profiles for rapid testing (`Rayhan Hossein` as Global Client, `Elena Rostova` as Pro Designer, `Marcus Vance` as Master Electrician).
  - Secure session sign-out locking active multi-currency escrow vaults.

- 🌐 **Global Multi-Category & Profession Engine**:
  - Dynamic service catalog across Tech, Trades & Contractors, Automotive, Healthcare, Legal, Creative, and more.
  - Real-time location filters with live currency conversion (USD, EUR, GBP, JPY, CAD, AUD, AED, etc.).

- 💼 **Escrow Vault & Transparent Fee Engine**:
  - Secure 8% platform fee calculation with detailed price breakdown.
  - Escrow milestone deposits, balance tracking, withdrawal mechanisms, and transaction logs.

- 💬 **Proposals, Direct Chat & Dispute Mediation**:
  - Client job posting and worker proposal submissions with custom delivery timelines and cost breakdown.
  - Real-time in-app chat simulation and formal dispute resolution system with 24-48 hr mediation review.

- 🎨 **Adaptive Design & Modern Jetpack Compose UI**:
  - Material 3 dynamic styling, custom metallic shield brand identity, fluid animations, and dark/light adaptive theming.

---

## Tech Stack & Architecture

- **Language**: Kotlin 2.x
- **UI Framework**: Jetpack Compose (Material 3)
- **Architecture**: MVVM (Model-View-ViewModel) + Repository Pattern
- **Async & State**: Kotlin Coroutines & `StateFlow` / `collectAsStateWithLifecycle`
- **Build System**: Gradle (Kotlin DSL - `.gradle.kts`) with Version Catalog (`libs.versions.toml`)
- **Target SDK**: Android 14+ (API 34/35)

---

## Project Directory Structure

```text
Fixify/
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── AndroidManifest.xml
│   │       ├── java/com/example/
│   │       │   ├── data/
│   │       │   │   ├── model/         # UserAccount, JobPosting, Payment, LocationData, Profession, Chat
│   │       │   │   └── repository/    # FixifyRepository (Auth, Escrow, Catalog, Chat)
│   │       │   └── ui/
│   │       │       ├── components/    # Reusable UI widgets, badges, topbars
│   │       │       ├── dialogs/       # Logout, Deposit, Withdraw, Post Job, Dispute dialogs
│   │       │       ├── screens/       # AuthScreen, HomeScreen, ProfileScreen, WalletScreen, etc.
│   │       │       ├── theme/         # Color, Type, Theme definitions
│   │       │       └── viewmodel/     # FixifyViewModel
│   │       └── res/                   # Drawables, mipmaps, strings, layouts
│   └── build.gradle.kts
├── gradle/
│   └── libs.versions.toml
├── .gitignore
├── metadata.json
├── README.md
├── build.gradle.kts
└── settings.gradle.kts
```

---

## Building and Running the App

### Option A: Direct Export from Google AI Studio
1. Open the **Project Settings / Options** menu (three dots or download icon in the top header).
2. Select **"Download as ZIP"** to immediately get the complete project archive.
3. Or select **"Push to GitHub" / "Export to GitHub"** to publish directly to your GitHub repository.

### Option B: Local Android Studio Build
1. Clone or extract the repository:
   ```bash
   git clone <your-github-repo-url>
   cd Fixify
   ```
2. Open the project in **Android Studio (Ladybug / Koala or newer)**.
3. Allow Gradle to sync dependencies automatically.
4. Select a connected device or Android Virtual Device (AVD).
5. Press **Run** (or `Shift + F10`) to build and deploy.

### Option C: Command Line Build
```bash
# Build Debug APK
./gradlew assembleDebug

# The generated APK will be located at:
# app/build/outputs/apk/debug/app-debug.apk
```
