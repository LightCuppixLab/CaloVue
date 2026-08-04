<!--
BEFORE PUBLICATION:
1. Confirm the Supabase project region and the backup/PITR retention period.
2. Ensure Delete Account also removes CaloVueProgress (Before & after) photos.
3. Confirm whether the Apple Health import UI will ship; remove that paragraph if not.
4. Obtain legal review and publish this policy at a stable public URL.
-->

# Privacy Policy for CaloVue

Last updated: August 4, 2026

This Privacy Policy explains how CaloVue (the “App”) processes and protects personal data. It applies to the iOS version of the App and is intended to provide the information required by the EU General Data Protection Regulation (“GDPR”).

## 1. Data Controller

The data controller is Light Cup Pix Lab, Padova, Italy, the studio that develops CaloVue.

Contact: lightcuppixlab.dev@gmail.com

## 2. What CaloVue Does

CaloVue helps you record meals, estimate foods, portions, calories and macronutrients, review meal history and track body weight. Food recognition and nutrition estimation use Apple Foundation Models on a compatible device. Results are estimates and are not medical advice.

## 3. Data We Process

We process only the data needed to provide and secure the App.

### Account and authentication

CaloVue uses Sign in with Apple. The App does not request your name or email address from Apple. Supabase Auth receives the Apple authentication token and provider identifier needed to create and maintain your account and assigns a CaloVue user ID. If Apple or Supabase includes additional technical authentication information as part of the sign-in process, it is processed only for authentication and account security.

The display name you choose inside CaloVue is stored only on your device and is not requested from Apple or saved in your CaloVue server profile.

### Meal and nutrition records

When an analysis is saved, Supabase receives the structured result generated on your device, including:

- meal and food names;
- meal date and time;
- food and total portion weights;
- estimated calories, protein, carbohydrates and fat;
- estimated score, rating, confidence, warnings and descriptive summary;
- corrections you make to food names or weights and related revision information.

Please avoid entering sensitive personal information in food names or other free-text fields.

### Meal photos and optional notes

The original meal photo, the optional preparation note and the two AI-generation steps remain on your device. They are not uploaded to Supabase or sent by CaloVue to an external AI provider. Before analysis, Apple frameworks may check the image locally for faces and sensitive content.

After a successful analysis, CaloVue may store a reduced meal thumbnail on your device for Home and History. “Before & after” photos are also stored only on your device. If you choose to share a result or progress image, iOS sends it only to the destination you select.

### Body-weight data

Body-weight values and dates entered manually are stored on your device for progress charts and Insights. If an Apple Health import option is available and you explicitly authorize it, CaloVue reads your latest body-mass measurement and stores the imported value locally. CaloVue does not write data to Apple Health, use Health data for advertising or sell it. You can deny or revoke Health access in iOS Settings.

### Usage and security records

For each successfully saved on-device analysis, Supabase stores a minimal record containing your user ID, a random request ID, the operation type, an optional meal ID and a timestamp. This supports daily Free limits, idempotency and service security. It does not contain the photo, note, AI prompt or raw AI response.

Our hosting and authentication providers may also process standard technical logs, such as IP address, request time and error or security metadata, under their own documented retention and security practices.

### Subscription data

If you purchase CaloVue Premium, we process the subscription status and non-financial identifiers needed to unlock features, such as product ID, original transaction identifier, environment and renewal or expiry date. We do not receive or store your payment card or other payment instrument data.

### Preferences stored on the device

Your language, measurement units, notification preferences, display name and other interface settings are stored locally on your device.

## 4. Data We Do Not Use

CaloVue does not use advertising SDKs, third-party analytics SDKs or cross-app tracking. We do not sell personal data. We do not use your photos, meal records, corrections or body-weight data to train advertising systems or external AI models. We do not collect contacts, precise location or advertising identifiers.

## 5. Why We Process Data and Our Legal Bases

Under Article 6 GDPR, we rely on:

- **Performance of a contract (Article 6(1)(b))** to create and manage your account, save and synchronize meal records, apply Free usage limits and provide Premium features.
- **Legitimate interests (Article 6(1)(f))** to protect accounts, prevent abuse, maintain idempotency, diagnose failures and keep the service secure. We use data-minimized records for these purposes.
- **Legal obligations (Article 6(1)(c))** where processing is required by applicable law.
- **Consent (Article 6(1)(a))** for optional permissions and actions where consent is the appropriate basis.

If CaloVue reads body-mass data from Apple Health, we rely on your explicit permission and, where the data qualifies as health data, your explicit consent under Article 9(2)(a) GDPR. You can refuse or withdraw that permission without losing the manual body-weight feature.

The App’s automated analysis produces informational estimates only. It does not make decisions that produce legal effects or similarly significant effects about you.

## 6. Where Data Is Stored and Who Processes It

- **Supabase** provides authentication, database, server functions and related infrastructure for account and structured meal data.
- **Apple** provides Sign in with Apple, on-device system frameworks, Apple Foundation Models and App Store purchase processing.

Meal photos, optional meal notes, local body-weight history and progress photos remain in the App’s local storage. Depending on your iPhone and backup settings, local App data may be included in a device backup managed by Apple.

We may disclose data when required by law or when necessary to establish, exercise or defend legal claims. We do not disclose your data to advertisers or data brokers.

## 7. International Transfers

Supabase and Apple may process limited data in countries outside the European Economic Area. Where GDPR requires safeguards for a transfer, we rely on applicable adequacy decisions, Standard Contractual Clauses or another lawful transfer mechanism provided through the relevant service agreement. You may contact us for further information about applicable safeguards.

## 8. Retention

Structured account, meal, correction, subscription and minimal request records are retained while your CaloVue account remains active, unless a shorter period is required for a specific record or longer retention is required by law.

Local thumbnails, progress photos, body-weight history and preferences remain on your device until you remove them, delete your CaloVue account using the App’s deletion flow, or uninstall the App. Copies contained in a device backup remain subject to your Apple backup settings and Apple’s retention practices.

When active database data is deleted, residual copies may remain temporarily in encrypted provider backups until the applicable backup rotation expires. They are not used for normal product operation and are removed according to the hosting provider’s configured backup schedule.

## 9. Account and Data Deletion

You can choose **Profile → Delete CaloVue Account**. After confirmation, CaloVue deletes your authentication account and the server records linked to it, including profiles, meals, food items, corrections, subscription entitlement records and minimal request records. The App also clears App-managed local data covered by the deletion flow. The action is permanent and cannot be undone.

Deleting your CaloVue account does not delete your Apple Account and does not automatically cancel an App Store subscription. Subscriptions must be managed separately in your App Store account settings.

You may also request deletion by contacting lightcuppixlab.dev@gmail.com.

## 10. Your GDPR Rights

Subject to applicable law, you may request:

- access to your personal data;
- correction of inaccurate data;
- deletion of your data;
- restriction of processing;
- objection to processing based on legitimate interests;
- portability of data you provided;
- withdrawal of consent at any time, without affecting earlier lawful processing.

You may edit supported meal information directly in the App or contact us at lightcuppixlab.dev@gmail.com. We may need to verify that a request relates to your account. You also have the right to lodge a complaint with the Italian Data Protection Authority or the supervisory authority in your country of residence.

## 11. Security

We use encrypted network connections, authenticated server functions, database row-level security and access controls designed to keep each account’s data separate. Photos and AI generation stay on the device to reduce data exposure. No system can guarantee absolute security.

## 12. Children

CaloVue is not intended for children under 16, and we do not knowingly collect personal data from children under 16. If you believe a child has provided data, contact us so that we can review and delete it where appropriate.

## 13. Changes to This Policy

We may update this Privacy Policy when the App, providers or legal requirements change. Material changes will be communicated in the App or by another appropriate method, and the “Last updated” date will be revised.

## 14. Contact

For privacy questions or to exercise your rights, contact:

Light Cup Pix Lab  
Padova, Italy  
lightcuppixlab.dev@gmail.com
