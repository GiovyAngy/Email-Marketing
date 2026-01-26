# Email Campaign Manager

Send beautiful, personalized campaigns in minutes. Just run the app, load your CSV, and hit send.

## Quick Start
- Place `EmailCampaignManager.exe` in any folder and double-click it.
- Your browser opens at `http://localhost:5000` automatically. Allow it through your antivirus if prompted (PyInstaller apps can trigger false positives).

## Import Your Contacts (TemplateCSV.csv)
- Use the bundled `TemplateCSV.csv` as your starting point.
- Required headers (exactly): `Name,Email` separated by commas.
- Example:
  - Name,Email
  - Jane Smith,jane@example.com
  - ,no-name@example.com  (leave Name empty if you do not have it)
- Save as UTF-8.

## Connect Your Email Account
1. Pick your provider: Gmail, Outlook/Hotmail, Yahoo, Office 365, or Custom SMTP.
2. Enter your email and password (or app password).
3. Click **Test Connection**; on success your password is stored securely in the system keychain.
4. Use the dropdown to recall saved accounts or remove them with **Cancel Account**.

## Upload & Attach
- Click **Load CSV** to import your recipients (use your edited TemplateCSV.csv).
- Optional: add shared attachments with **Load Files**; they are sent to every recipient.

## Craft Your Message
- Subject is required.
- Use placeholders `{name}` and `{email}` in the body; they are replaced per row.
- If Name is missing, the **Default Greeting** is used (e.g., "Dear Friend").
- Switch between Text and HTML modes in the editor.

## Send
- Press **🚀 Send Emails**.
- Watch live logs, progress bar, and stats while the campaign runs.

## Security
- Passwords are stored locally in your system keychain (e.g., Windows Credential Manager).
- To remove stored credentials: select the account and click **Cancel Account**.

## Common Fixes
- SMTP connection failed: use an App Password (Gmail requires 2FA + App Password); verify host/port for Custom SMTP.
- CSV rejected: headers must be exactly `Name,Email` with comma separator (no semicolons).
- Windows icon looks old: delete or rename the old `EmailCampaignManager.exe` and copy the new one (Windows may cache icons).

## Support & Contact

Need help, have questions, or just want to say hi? 😊  
Click the badge below to get in touch:

[![Contact](https://img.shields.io/badge/Contact-Get%20in%20touch-blue?style=for-the-badge)](https://giovyangy.github.io/Lebenlauf/index.html#kontakt)


## Included Files
- `EmailCampaignManager.exe` — portable app.
- `TemplateCSV.csv` — ready-to-use contact template.
