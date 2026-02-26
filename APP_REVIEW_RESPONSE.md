# App Review Response Template (TopArena)

Use this reply in App Store Connect and replace bracketed placeholders.

## Guideline 2.1 - App Completeness (Terms not visible)

We fixed the issue where Terms could not be viewed during registration.

- In-app registration now links to Terms of Use and Privacy Policy.
- Terms URL: [https://YOUR-DOMAIN/terms.html]
- Privacy URL: [https://YOUR-DOMAIN/index.html]

Testing completed on clean installs and update installs on iOS devices, including iPhone 17 Pro Max (iOS 26.3).

## Guideline 5.1.1 - Purpose String Clarity

We updated the photo library purpose string to clearly explain use and include a concrete example.

Current `NSPhotoLibraryUsageDescription`:
"TopArena uses your photo library so you can select a profile photo or team logo that appears in your account and league pages."

If applicable, current `NSPhotoLibraryAddUsageDescription`:
"TopArena saves images to your photo library only when you choose to export team or match images."

## Guideline 5.1.1(v) - Account Deletion

TopArena now supports account deletion initiation and provides a direct deletion path.

- In-app location: Profile > Settings > Delete Account
- Direct deletion page: [https://YOUR-DOMAIN/account-deletion.html]
- If a user cannot access the account, support is available to recover account access and then complete in-app deletion.

## Guideline 3.2 - Business Model / Distribution

TopArena is intended for a general public audience.

1. Is your app restricted to one company or organization?
No.

2. Is your app designed for a limited group of organizations?
No. Any user can register and use available features.

3. What features are intended for the general public?
Public users can create accounts, create/join teams, join leagues, and view matches and related content without organizational affiliation.

4. How do users obtain an account?
Users self-register in-app using email signup.

5. Is there paid content, and who pays?
[Describe your current monetization clearly. Example: "No paid content" or "Users pay for optional subscription features via in-app purchase."]

If your app is actually private to specific organizations, replace this section and select the correct distribution channel (Apple Business Manager, unlisted, etc.).
