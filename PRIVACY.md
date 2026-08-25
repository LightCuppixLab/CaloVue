# Privacy Policy for CaloVue

Last updated: August 25, 2026

This Privacy Policy explains how CaloVue (the “App”) processes and protects personal data. It applies to the iOS version of the App and is intended to provide the information required by the EU General Data Protection Regulation (“GDPR”).

## 1. Data Controller

The data controller is Light Cup Pix Lab, Padova, Italy, the studio that develops CaloVue.

Contact: lightcuppixlab.dev@gmail.com

## 2. What CaloVue Does

CaloVue helps you record meals, estimate foods, portions, calories and macronutrients, review meal history and track body weight. Results are estimates and are not medical advice.

CaloVue offers three ways to record a meal, and they do not process data in the same way:

- **Photo analysis** and **written description** send your input to an external AI provider for analysis, as described in Section 3.
- **Nutrition label reading** runs entirely on your device using Apple Foundation Models. Nothing about that analysis is sent to an external AI provider.

Section 3 explains exactly what leaves your device in each case.

## 3. Data We Process

We process only the data needed to provide and secure the App.

### Account and authentication

CaloVue uses Sign in with Apple. The App does not request your name or email address from Apple. Supabase Auth receives the Apple authentication token and provider identifier needed to create and maintain your account and assigns a CaloVue user ID. If Apple or Supabase includes additional technical authentication information as part of the sign-in process, it is processed only for authentication and account security.

The display name you choose inside CaloVue is stored only on your device and is not requested from Apple or saved in your CaloVue server profile.

### Meal and nutrition records

When an analysis is saved, Supabase receives the structured result, including:

- meal and food names;
- meal date and time;
- food and total portion weights;
- estimated calories, protein, carbohydrates and fat;
- estimated score, rating, confidence, warnings and descriptive summary;
- corrections you make to food names or weights and related revision information.

Please avoid entering sensitive personal information in food names or other free-text fields.

### Meal photos, descriptions and AI analysis

**Checks performed on your device first.** Before a meal photo is used for analysis, Apple frameworks examine it locally on your device: Vision checks for faces, Apple’s Sensitive Content Analysis checks for sensitive imagery where that policy is active, and an on-device Apple model checks that the image actually shows food. A photo rejected by any of these checks is never transmitted anywhere and never reaches an AI provider.

**Photo analysis.** If the photo passes those checks and you start the analysis, the photo is transmitted over an encrypted connection to our authenticated server function, which forwards it to our AI provider, Anthropic, to produce the nutritional estimate. The photo is held only in memory for the duration of that request. CaloVue does not save the meal photo in its database or in remote file storage, and does not keep a server-side copy after the request completes.

**Written description.** In the text mode, the short description you type — currently limited to 120 characters — together with the portion weight is transmitted the same way, through our authenticated server function to Anthropic. No photo is involved.

**Re-analysis.** When you ask CaloVue to recalculate a meal you already saved, only the stored food names and weights for that meal are sent. No photo is sent.

**Nutrition label reading.** In this mode the photo of the printed nutrition table, the reading of it and the AI step all remain on your device, using Apple Foundation Models. Nothing is sent to Anthropic.

**About the AI provider.** Anthropic acts as a processor on our behalf under its commercial terms. Under those terms, inputs and outputs sent through the API are not used to train Anthropic’s models. Anthropic may retain the content of a request for a limited period for security and abuse-monitoring purposes, under its own documented retention practices, after which it is deleted. We do not send your CaloVue account identifier, email address or name to Anthropic.

**What stays on your device.** After a successful analysis, CaloVue may store a reduced meal thumbnail on your device for Home and History. “Before & after” progress photos are also stored only on your device. If you choose to share a result or progress image, iOS sends it only to the destination you select.

Please do not photograph people, documents or other sensitive subjects for analysis, and avoid including personal information in the written description.

### Body-weight data

Body-weight values and dates entered manually are stored on your device for progress charts and Insights. If you explicitly authorize it, CaloVue reads your latest body-mass measurement from Apple Health and stores the imported value locally. CaloVue does not write data to Apple Health, use Health data for advertising or sell it. You can deny or revoke Health access in iOS Settings.

### Usage and security records

For each saved analysis, Supabase stores a minimal record containing your user ID, a random request ID, the operation type, an optional meal ID and a timestamp. This supports idempotency and service security. It does not contain the photo, description, AI prompt or raw AI response.

Separately, each request forwarded to the AI provider is recorded in a restricted server-side ledger containing your user ID, a random request ID, the operation type, its status and timestamps. This ledger enforces the daily allowance described below and lets us refund an attempt that failed for technical reasons. It does not contain the photo, description, AI prompt or raw AI response.

These records support the current usage model: nutrition label reading is free and unlimited because it runs on your device, while photo analysis, written description and re-analysis require a Premium subscription and share a limit of six attempts per UTC day. A photo rejected by the on-device checks does not consume that allowance.

Our hosting, authentication and AI providers may also process standard technical logs, such as IP address, request time and error or security metadata, under their own documented retention and security practices.

### Subscription data

If you purchase CaloVue Premium, we process the subscription status and non-financial identifiers needed to unlock features, such as product ID, original transaction identifier, environment and renewal or expiry date. We do not receive or store your payment card or other payment instrument data.

### Preferences stored on the device

Your language, measurement units, notification preferences, display name and other interface settings are stored locally on your device.

## 4. Data We Do Not Use

CaloVue does not use advertising SDKs, third-party analytics SDKs or cross-app tracking. We do not sell personal data. We do not use your photos, meal records, corrections or body-weight data to train AI models, our own or anyone else’s, and our AI provider’s terms prohibit using the content of our requests to train its models. We do not collect contacts, precise location or advertising identifiers.

## 5. Why We Process Data and Our Legal Bases

Under Article 6 GDPR, we rely on:

- **Performance of a contract (Article 6(1)(b))** to create and manage your account, analyze the meal photos and descriptions you submit, save and synchronize meal records, apply usage limits and provide Premium features.
- **Legitimate interests (Article 6(1)(f))** to protect accounts, prevent abuse, maintain idempotency, diagnose failures and keep the service secure. We use data-minimized records for these purposes.
- **Legal obligations (Article 6(1)(c))** where processing is required by applicable law.
- **Consent (Article 6(1)(a))** for optional permissions and actions where consent is the appropriate basis.

If CaloVue reads body-mass data from Apple Health, we rely on your explicit permission and, where the data qualifies as health data, your explicit consent under Article 9(2)(a) GDPR. You can refuse or withdraw that permission without losing the manual body-weight feature.

The App’s automated analysis produces informational estimates only. It does not make decisions that produce legal effects or similarly significant effects about you.

## 6. Where Data Is Stored and Who Processes It

- **Supabase** provides authentication, database, server functions and related infrastructure for account and structured meal data.
- **Anthropic** provides the AI models that analyze meal photos and written descriptions, as described in Section 3. It receives the photo or description transiently for the duration of the request and does not receive your account identifier, email address or name.
- **Apple** provides Sign in with Apple, on-device system frameworks, Apple Foundation Models used for the on-device checks and the nutrition label reading, and App Store purchase processing.

Meal thumbnails, local body-weight history, progress photos and preferences remain in the App’s local storage. Depending on your iPhone and backup settings, local App data may be included in a device backup managed by Apple.

We may disclose data when required by law or when necessary to establish, exercise or defend legal claims. We do not disclose your data to advertisers or data brokers.

## 7. International Transfers

Supabase, Anthropic and Apple may process limited data in countries outside the European Economic Area, including the United States. Where GDPR requires safeguards for a transfer, we rely on applicable adequacy decisions, Standard Contractual Clauses or another lawful transfer mechanism provided through the relevant service agreement. You may contact us for further information about applicable safeguards.

## 8. Retention

Structured account, meal, correction, subscription and minimal request records are retained while your CaloVue account remains active, unless a shorter period is required for a specific record or longer retention is required by law.

Meal photos and written descriptions sent for analysis are not retained by CaloVue after the request completes. Our AI provider may retain the content of a request for a limited period for security and abuse-monitoring purposes under its own documented practices, after which it is deleted.

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

We use encrypted network connections, authenticated server functions, database row-level security and access controls designed to keep each account’s data separate. Meal photos and descriptions sent for analysis travel over encrypted connections through our authenticated server function, are processed transiently and are not stored by CaloVue. On-device checks run before any photo is transmitted, and the nutrition label mode keeps its analysis entirely on your device. No system can guarantee absolute security.

## 12. Children

CaloVue is not intended for children under 16, and we do not knowingly collect personal data from children under 16. If you believe a child has provided data, contact us so that we can review and delete it where appropriate.

## 13. Changes to This Policy

We may update this Privacy Policy when the App, providers or legal requirements change. Material changes will be communicated in the App or by another appropriate method, and the “Last updated” date will be revised.

## 14. Contact

For privacy questions or to exercise your rights, contact:

Light Cup Pix Lab  
Padova, Italy  
lightcuppixlab.dev@gmail.com
