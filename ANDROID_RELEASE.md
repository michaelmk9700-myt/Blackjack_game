# Blackjack Royale — Android preparation

## Current status
This repository is a browser game with an Android Capacitor project scaffold. **No APK/AAB has been compiled, signed, tested on Android, or published.** Advertising SDK is not integrated yet.

## Build prerequisites
- Node.js 20+ and npm
- Android Studio and Android SDK (API 36+)
- JDK version compatible with the chosen Android Gradle plugin

## Generate Android project
1. `npm install`
2. `mkdir -p www && cp index.html www/index.html` (Windows: copy the file manually)
3. `npm run android:add`
4. `npm run android:sync`
5. `npm run android:open`
6. In Android Studio, configure targetSdkVersion **36 or higher** and build/test a signed Android App Bundle (AAB) for Play Console.

## Release checklist
- Test dealing, double, bust, dealer reveal, blackjack payouts, sound, and save data on physical Android devices
- Test app pause/resume and screen sizes
- Generate final icons, feature graphics, screenshots and store listing
- Add privacy policy and accurate Data safety declarations
- Decide content rating and simulated gambling disclosures; keep virtual coins nonredeemable
- Review Google Play and AdMob simulated gambling and advertising policies before integrating ads
- Create a release keystore securely outside Git; enable Play App Signing
- Configure production app ID, version code/name and sign release bundle
- Test closed track if required by the Play Console account

## Notes
The GitHub Pages website continues to serve `index.html`. The Android package uses a local copy in `www/index.html`; run the copy command again before syncing after web updates. The package ID is provisional and should be confirmed before publication.
