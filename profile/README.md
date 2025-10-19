# Telegram CRM Panel — End‑User Guide

This guide explains how to use the Telegram CRM Panel from a regular user’s perspective. Admin-only pages are explicitly out of scope.

## Audience & Prerequisites
- You have access to the web app URL provided by your team.
- A backend API must be running (your workspace will typically have this prepared by your team).
- You either have a user account or can self-register (if enabled by your organization).

## Quick Start
1) Open the app URL in your browser.
2) Sign up (Register) or Sign in.
3) You will land on the Dashboard. Use the sidebar to navigate: Contacts, Sequences, Broadcasting, Templates, Jobs, Accounts, Billing, Analytics, Integrations, Settings, Help.

## Navigation & UI Basics
- Header: global search, notifications, theme toggle (light/dark), and user menu.
- Sidebar: main modules. Active page is highlighted.
- Global Search: quickly jump to contacts, jobs, or views. Keyboard shortcuts may be available (commonly Ctrl/Cmd+K).
- Responsive: works on desktop, tablet, and mobile. Sidebar can collapse on small screens.

## Authentication
- Register: provide required fields on the Register page and submit. If email verification is enforced by your organization, follow the instructions you receive.
- Login: use your credentials on the Login page. On success, you will be redirected to the Dashboard.

## Dashboard (Home)
The dashboard provides a quick overview of your activity and system status. You will typically find:
- Summary cards (e.g., total contacts, active campaigns, recent jobs)
- Recent activity feed and high-level charts
- Shortcuts to common actions (e.g., “Go to Contacts”)

## Contacts
Manage your Telegram contacts and their journey through your funnel.

Views
- Pipeline: contacts are grouped in columns by stage. Drag-and-drop to move a contact to the next stage.
- List: a compact table/list for quick scanning and bulk operations.
- Archived: contacts you have archived; you can restore when needed.

Search & Filters
- Use the search box to find contacts by name, username, or other attributes.
- Filters help narrow down by stage or recency.

Importing Contacts
- Open the Import action (e.g., “Import from Telegram”).
- Choose the source account (one of your connected Telegram accounts).
- Choose a time window (e.g., import last N days of dialogs/messages).
- Start the import and follow the progress bar (processed dialogs/messages, any errors).
- Note: Import may require an active subscription/plan. If features are locked, the UI will show a notice with upgrade guidance.

Contact Profile & Notes
- Open a contact to view details and add notes.
- Edit notes inline and save. You can cancel edits to discard changes.

Archive / Restore
- Use archive to remove a contact from active workflows without deleting historical data.
- Restore from Archive when needed.

## Contact Detail (Chat)
Open a contact to chat in real time and view the full message history.
- Realtime chat: messages appear as they arrive; send replies instantly.
- Message types: plain text; attachments may be available if enabled by your plan and backend.
- Quick actions: jump to profile, stages, or related tasks.

## Sequences (Campaigns)
Automate multi-step outreach to your audience.

Create & Manage
1) Click “Create Sequence”, name your campaign, and select the sending account(s) if required.
2) Upload targets (CSV) or select an existing target set.
3) Add or select a template/spintax for message personalization.
4) Start the sequence. You can pause/resume as needed.

Statuses & Metrics
- Each sequence shows status (e.g., Draft, Running, Paused, Completed) along with counts and progress.
- Open a sequence to view recent sends, errors, and timing.

Spintax Sets
- Define reusable spintax keys for randomized text variants (e.g., {hello|hi|hey}).
- Add a key and pipe-separated options; save the set.
- Reference these in your templates to improve deliverability and reduce repetition.

## Broadcasting (Bulk Send)
Send one-off broadcasts to a target segment.
1) Choose a target (list, imported segment, or selection).
2) Pick a template or compose a message.
3) Optionally schedule the send; otherwise send immediately.
4) Track progress and outcomes on the Jobs page.

## Templates
Create and manage message templates used by Sequences and Broadcasting.
- Rich editor: compose text and optionally use variables or spintax.
- Best practices: keep messages short, personalized, and compliant with platform rules.
- Versioning: if you need variations, duplicate and adjust.

## Jobs
Monitor background jobs such as sends, imports, and sequence runs.
- Statuses: Queued, Running, Succeeded, Failed.
- Drill down to see logs and error details.
- Retry failed jobs if the action permits.

## Accounts (Telegram)
Connect and verify Telegram accounts used for messaging.

Add & Verify
1) Add an account with the phone number in international format.
2) Request a verification code; enter the received code.
3) If two‑factor authentication (2FA) is enabled, enter your password to complete verification.
4) If the code expires, request a new one (respecting cooldown timers shown by the UI).

Proxy (Optional)
- Test a proxy for a given account to improve reliability based on your region/policies.
- Review test results (latency/connectivity) before enabling.

Enable/Disable
- Temporarily disable an account from being used in sends if needed; re‑enable when ready.

## Billing
Manage your subscription plan and limits.
- View available plans and current usage (e.g., max accounts, feature access).
- Upgrade/downgrade as your needs change.
- Renewal details and billing history (if exposed by your organization).

## Analytics
View key performance indicators such as sends, replies, and conversion trends.
- Adjust date ranges and filters to focus on specific periods.
- Use charts to identify what’s working and where to iterate.

## Integrations
Discover available integrations and follow the on‑screen steps to connect them.
- Typical flow: open an integration card, read the description, click Connect/Configure, follow OAuth or API key steps.

## Settings
Personalize your experience.
- Profile: update your display name and relevant preferences.
- Preferences: toggle light/dark theme, adjust notification preferences.
- Security: sign out from all devices (if available) and update password.

## Help
Find answers and support.
- FAQ section for common questions.
- Links to documentation or support channels provided by your team.

## Tips & Troubleshooting
- Feature Locked: If you see a lock banner, you may need an active subscription or a higher plan.
- Import is slow: Keep the browser tab open; large imports can take time depending on your Telegram data size.
- Message delivery issues: Verify the sending account is active and not rate‑limited; consider adjusting send cadence and using spintax.
- Two‑factor issues: Ensure you have your 2FA password; request a new verification code if the previous one expired.
- Proxy problems: Re‑test your proxy and check connectivity from your network location.

---
This guide covers the end‑user journey in the Telegram CRM Panel. For architecture and admin operations, see the corresponding documents in the main `DOCS` folder.


