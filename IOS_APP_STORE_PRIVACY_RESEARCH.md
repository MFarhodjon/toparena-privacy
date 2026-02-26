# iOS App Store Privacy Research (TopArena)

Date checked: February 26, 2026

This document summarizes current Apple requirements relevant to privacy policy and privacy compliance for App Store submission.

## Primary Apple Sources

- App Store Review Guidelines (Privacy section 5.1):
  - https://developer.apple.com/app-store/review/guidelines/#privacy
- App privacy details in App Store Connect:
  - https://developer.apple.com/app-store/app-privacy-details/
- User privacy and data use (ATT, privacy manifests, SDK signatures):
  - https://developer.apple.com/app-store/user-privacy-and-data-use/
- App Store Connect Help - manage privacy policy URL:
  - https://developer.apple.com/help/app-store-connect/manage-app-information/manage-your-apps-privacy-policy
- Account deletion requirement details:
  - https://developer.apple.com/support/offering-account-deletion-in-your-app/
- Upcoming required reason API requirement update:
  - https://developer.apple.com/news/upcoming-requirements/

## What Apple Requires (Practical Interpretation)

1. Privacy Policy Availability
- Apps that collect user data must provide a privacy policy.
- Privacy policy must be easily accessible in-app.
- App Store Connect requires a privacy policy URL for iOS and macOS apps.

2. Data Collection and Use Clarity
- Explain what data is collected and why.
- Explain data retention and deletion behavior.
- Explain sharing/disclosure behavior, including legal disclosure scenarios.

3. Third-Party Data Processors
- If third-party providers process user data, they must provide the same or equal protection as required by the app policy.

4. Permission Prompts and Purpose Strings
- Purpose strings for protected resources must be specific and complete.
- Generic text like "needs photo access" is not sufficient.

5. App Privacy Labels in App Store Connect
- Declare all data types collected and tracking behavior.
- Include data collected by third-party SDKs.
- Keep App Privacy metadata consistent with actual behavior and policy text.

6. Account Deletion
- If account creation is supported, the app must also allow account deletion initiation.
- Deactivation-only is not enough.
- If deletion is finished on web, provide a direct link to that exact page.

7. Tracking and ATT
- If tracking users across apps/websites or accessing IDFA for tracking, ATT permission is required before tracking.

8. Privacy Manifests and SDK Signatures
- Apple now requires privacy manifests/signatures for listed SDKs and required reason APIs.
- Verify this in the current "upcoming requirements" page before each release.

## Additions Implemented in This Repo

- [index.html](C:/Users/ffarx/OneDrive/Desktop/Github%20clones/toparena-privacy/index.html)
  - Added deeper App Store aligned sections:
    - Legal bases and consent
    - iOS permission purpose string clarity
    - Tracking and ATT statement
    - Third-party processor obligations
    - Retention and deletion clarity
    - App Store privacy label mapping table
    - Policy availability statement
- [account-deletion.html](C:/Users/ffarx/OneDrive/Desktop/Github%20clones/toparena-privacy/account-deletion.html)
  - Already includes direct deletion initiation guidance and deletion scope/timeline.
- [terms.html](C:/Users/ffarx/OneDrive/Desktop/Github%20clones/toparena-privacy/terms.html)
  - Provides registration-consent text and legal links.

## Still Required in the Mobile App Code (Outside This Repo)

- Add visible registration links to Terms and Privacy.
- Ensure an in-app Delete Account path exists and is easy to find.
- Update Info.plist purpose strings (NSPhotoLibraryUsageDescription and, if applicable, NSPhotoLibraryAddUsageDescription).
- Ensure App Privacy metadata in App Store Connect exactly matches real runtime behavior.
- Validate third-party SDK privacy manifests / required reason APIs before upload.
