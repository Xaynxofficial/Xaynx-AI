> Official Live Page: https://xaynxai.com/google-privacy-policy

Google Data SecurityApplication: xaynx(Xaynx AI Teknoloji A.Ş.)

# Google API & Workspace User Data Privacy Policy

Effective Date: November 16, 2026•Last Updated: November 16, 2026•Doc ID: XAYNX-GOOGLE-PRIV-2026/V2•Adherence to Google Limited Use Requirements
Google API Services User Data Policy (Limited Use Disclosure)"Xaynx AI's (application name: **xaynx**) use and transfer of information received from Google APIs to any other app will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements. Xaynx AI does NOT use data obtained from Google Workspace APIs to develop, improve, or train generalized or foundation AI/ML models."

## 1. Scope & Application Identity

This policy governs how the application "xaynx" (also referred to as "Xaynx AI"), developed by Xaynx AI Teknoloji A.Ş., accesses, collects, uses, protects, retains, and deletes user data obtained via Google OAuth 2.0 authorization and Google Workspace APIs (specifically the Gmail API).

Our application only accesses Google user data upon explicit user consent and opt-in action. Authentication is completely voluntary and users can revoke access at any time.

## 2. Requested Google OAuth Scopes & Specific Uses

Xaynx AI strictly adheres to the Principle of Data Minimization and requests only the minimum required scopes necessary to deliver user-initiated features:

| OAuth Scope | Data Accessed | Functional Purpose |
| --- | --- | --- |
| https://www.googleapis.com/auth/gmail.readonly | Email headers, subjects, sender info, message snippets | To display inbox messages, search emails, and provide instant email summaries requested by the user. |
| https://www.googleapis.com/auth/gmail.send | User-drafted email content | To transmit emails drafted and explicitly confirmed by the user via the Send action. No automated or unsolicited sending. |
| https://www.googleapis.com/auth/gmail.compose | Email drafts | To create and save email drafts for user review and manual sending. |
| https://www.googleapis.com/auth/gmail.modify | Email labels and read/unread status | To mark messages as read or manage labels upon direct user action. |
| https://www.googleapis.com/auth/calendar.events | Calendar events, meeting times, and attendees | To create, view, or update calendar events and meetings initiated by the user. |
| https://www.googleapis.com/auth/calendar.readonly | Upcoming calendar events and schedule | To view daily schedules and upcoming appointments to provide schedule assistance. |
| https://www.googleapis.com/auth/drive.readonly | Selected Drive documents, PDFs, and text files | To read and summarize user-selected documents and perform AI document analysis. |
| https://www.googleapis.com/auth/drive.file | Files created or opened by Xaynx AI | To save documents, reports, and files created by the user directly to their Google Drive. |
| userinfo.email, userinfo.profile & openid | Email address, display name, avatar, unique user ID | To authenticate session identity, verify user account, and display profile information. |

## 3. Data Storage, Retention & Security

**Zero Persistent Server Storage:** Xaynx AI does NOT permanently store Gmail email bodies, attachments, or personal message contents on centralized backend database servers. Emails are fetched on-demand directly from Google APIs over encrypted TLS 1.3 connections, processed ephemerally in the client browser's local session memory, and completely discarded upon session termination or sign-out.

**OAuth Tokens:** Google OAuth access tokens are stored in local browser storage to maintain your active session, and when multi-device sync is enabled, are stored encrypted in your isolated account session record. They are immediately expunged when you log out or disconnect the integration.

4. Strict AI Model Training ProhibitionUnder no circumstances is data obtained from Google Workspace or Gmail APIs used to train, develop, fine-tune, or improve generalized, non-personalized, or foundational artificial intelligence / machine learning models. We do not use Google user data for training public AI systems.

## 4. No Data Sharing, Sale, or Advertising

- **No Advertising:** Google user data is never transferred to advertisers, ad networks, or used for behavioral advertising or retargeting.
- **No Data Sale:** Google user data is never sold, leased, or traded to data brokers or any commercial third parties.
- **Human Review Limitations:** Our employees do not read or inspect user email content unless explicitly requested by the user for a technical support ticket or required by binding statutory laws.

## 5. User Access Revocation & Data Deletion

Users have full autonomy to revoke Xaynx AI's access to their Google account at any time using either of the following methods:

**Method 1: Inside Xaynx AI Settings**Navigate to Settings > Connectors and click 'Disconnect' on the Gmail card. This immediately purges all local tokens and session data.

**Method 2: Google Account Security**Directly visit [Google Permissions Page](https://myaccount.google.com/permissions) and remove access for \"xaynx\" with a single click.

## 6. Privacy Officer Contact Information

For inquiries regarding our Google API User Data commitments, privacy requests, or data deletion inquiries:

Xaynx AI Teknoloji A.Ş.

Email: [contact@xaynx.co m](mailto:contact@xaynx.co m)

General Privacy Policy: [https://xaynxai.com/privacy](/privacy)
