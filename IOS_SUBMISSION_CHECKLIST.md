# iOS Resubmission Checklist (TopArena)

Complete these steps in your app project before uploading the next build.

## 1) Registration must show Terms and Privacy

- Add two visible links on the registration screen:
  - `https://YOUR-DOMAIN/terms.html`
  - `https://YOUR-DOMAIN/index.html`
- Add consent text under the Sign Up button:
  - `By creating an account, you agree to the Terms of Use and Privacy Policy.`

## 2) Update iOS permission purpose strings

In `Info.plist`, set clear strings:

- `NSPhotoLibraryUsageDescription`
  - `TopArena uses your photo library so you can select a profile photo or team logo that appears in your account and league pages.`
- `NSPhotoLibraryAddUsageDescription` (only if you save images to Photos)
  - `TopArena saves images to your photo library only when you choose to export team or match images.`

## 3) Add in-app account deletion entry point

- Add a menu item in app settings: `Delete Account`.
- This action should initiate deletion directly in app or open:
  - `https://YOUR-DOMAIN/account-deletion.html`
- Do not offer only deactivation.

## 4) Keep App Privacy labels accurate in App Store Connect

- Declare all collected data categories and uses.
- Include data collected by third-party SDKs.
- Verify your declarations match runtime behavior exactly.
- Set privacy policy URL and (optionally) privacy choices URL.

## 5) ATT and tracking compliance

- If tracking across other companies' apps/websites, request ATT permission before tracking.
- If not tracking, keep this consistent in both app behavior and App Privacy labels.

## 6) Privacy manifests and SDK checks

- Verify required reason API declarations are present and valid.
- Verify privacy manifests and signatures for listed third-party SDKs.
- Re-check Apple upcoming requirements before each release.

## 7) App Review note

Use `APP_REVIEW_RESPONSE.md` and include:
- Exact in-app path for Terms and Delete Account.
- Test credentials.
- Any region/role prerequisites.

## 8) Distribution decision (Guideline 3.2)

- If app is public: explain that anyone can sign up.
- If app is restricted to specific organizations: switch to Apple Business Manager / unlisted distribution.
