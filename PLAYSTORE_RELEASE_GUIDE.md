# Google Play Store Fresh App Release Guide

This guide walks you through the steps to publish the **Kumarpur Land** app for the first time as a fresh release on the Google Play Store.

---

## Step 1: Pre-Release App Configuration

Before building the production bundle, ensure the app's metadata and settings are correct.

1. **Verify Package Name**:
   - Locate the `namespace` and `applicationId` in [android/app/build.gradle.kts](file:///c:/Users/Python/OneDrive/Desktop/magical-hubble/android/app/build.gradle.kts) (lines 18 and 38).
   - Ensure it is set to the correct production ID: `"com.adhikshita.kumarpurland"`.

2. **Check Version Info**:
   - For a fresh release, the initial version is typically:
     - `versionCode = 1`
     - `versionName = "1.0"`
   - Open [android/app/build.gradle.kts](file:///c:/Users/Python/OneDrive/Desktop/magical-hubble/android/app/build.gradle.kts) and adjust these values if necessary in the `defaultConfig` block:
     ```kotlin
     defaultConfig {
         applicationId = "com.adhikshita.kumarpurland"
         minSdk = 24
         targetSdk = 36
         versionCode = 1
         versionName = "1.0"
     }
     ```

3. **Verify Signing Credentials**:
   - The production signing keys are configured inside [android/local.properties](file:///c:/Users/Python/OneDrive/Desktop/magical-hubble/android/local.properties).
   - Ensure the following properties are correct (this file is excluded from Git for security):
     ```properties
     release.keystore.file=release.jks
     release.keystore.password=AdhikshitaLand2026!
     release.key.alias=releaseKey
     release.key.password=AdhikshitaLand2026!
     ```
   - Ensure the keystore file [release.jks](file:///c:/Users/Python/OneDrive/Desktop/magical-hubble/android/app/release.jks) is located in the `android/app` directory.

---

## Step 2: Build the Signed Production Bundle (AAB)

Android App Bundles (`.aab`) are the required format for all new apps uploaded to the Google Play Store.

1. Open PowerShell or a terminal window inside the `android` directory:
   ```powershell
   cd android
   ```
2. Run the Gradle clean and bundle task:
   ```powershell
   ./gradlew clean bundleRelease
   ```
3. Once the build finishes successfully, your signed production app bundle will be located at:
   - `android/app/build/outputs/bundle/release/app-release.aab`
4. Copy or move this file to your desktop or workspace root for easy upload.

---

## Step 3: Set Up a Google Play Developer Account

If you do not have one, you need a developer account to publish apps.

1. Go to the [Google Play Console Sign-up page](https://play.google.com/console/signup).
2. Sign in with your Google account.
3. Choose your account type (Personal or Organization).
4. Pay the **$25 USD one-time developer registration fee**.
5. Complete your identity verification (requires ID/documentation).

---

## Step 4: Create Your App in the Play Console

1. Open the [Google Play Console](https://play.google.com/console).
2. Click the **Create app** button in the top right.
3. Fill in the initial app details:
   - **App name**: Adhikshita Kumarpur Land (or your preferred name)
   - **Default language**: English (United States)
   - **App or game**: App
   - **Free or paid**: Free
4. Agree to the Developer Program Policies and US Export Laws, then click **Create app**.

---

## Step 5: Complete the Mandatory Dashboard Tasks

Google requires all fresh apps to complete a series of self-declaration tasks before they can be released. Navigate to the **Dashboard** and complete:

1. **Set privacy policy**: Provide the public URL of your website's privacy policy.
2. **App access**: Declare if parts of your app are restricted (e.g., login screens). Choose "All functionality is available without special access" unless you have login gates.
3. **Ads**: Declare if your app contains ads (select "No").
4. **Content rating**: Click "Start questionnaire", fill in your contact email, select your app category (Utility/Productivity), and answer the questions to receive an age-rating certificate.
5. **Target audience**: Select age groups (e.g., 18 and over) and declare if children will be attracted to the app (select "No").
6. **News apps**: Declare if your app is a news app (select "No").
7. **COVID-19 contact tracing/status**: Declare if your app is a status app (select "My app is not a publicly available COVID-19 contact tracing or status app").
8. **Data safety**: Complete the questionnaire declaring how you handle user data (e.g., whether you collect contact information or device IDs).
9. **Government apps**: Declare if your app is developed on behalf of a government entity (select "No").

---

## Step 6: Set Up Your Store Listing

Your store listing is what users see on the Google Play Store. Go to **Grow** > **Store presence** > **Main store listing**:

1. **App details**:
   - **Short description** (up to 80 characters): *e.g., Browse and book premium industrial plots in Kumarpur, West Bengal.*
   - **Full description** (up to 4000 characters): Describe the project connectivity, road sizes, available plot tiers, and features.
2. **Graphics**:
   - **App icon**: Upload a `512 x 512` pixel PNG or JPEG (max 1MB).
   - **Feature graphic**: Upload a `1024 x 500` pixel PNG or JPEG (max 1MB).
   - **Phone screenshots**: Upload at least two screenshots (9:16 or 16:9 aspect ratio, between 320px and 3840px).
   - **Tablet screenshots**: Optional but recommended if targeting tablets.

---

## Step 7: Create and Roll Out the Release

Once the store listing is set up, you can release your app.

1. In the left-hand menu, navigate to **Release** > **Production**.
2. Click **Create new release** at the top right.
3. **Play App Signing**:
   - For fresh apps, click **Choose signing key** (Google recommends using Google Play App Signing key. It will automatically enroll you).
4. **App bundles**:
   - Upload the `.aab` file you built in **Step 2** (`app-release.aab`).
5. **Release details**:
   - Verify the release name (automatically populated based on your `versionName`, e.g., `1.0`).
   - Enter **Release notes** (e.g., `Initial release of Adhikshita Kumarpur Land industrial plot viewer and booking application.`).
6. Click **Next** at the bottom to run automated pre-launch validation tests.
7. Click **Save** and then click **Start rollout to Production** (or submit for review).
8. Google will review the application (for new apps, the initial review can take between **3 to 7 days**). Once approved, it will go live on the store automatically.

---

## 🔑 Crucial Warnings

> [!CAUTION]
> **Keystore Security**: Keep the keystore file [release.jks](file:///c:/Users/Python/OneDrive/Desktop/magical-hubble/android/app/release.jks) secure. Make a copy of it and store it in a safe place. If lost, you will not be able to publish updates.
