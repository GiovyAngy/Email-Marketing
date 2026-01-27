# Email Campaign Manager v1.4

Send beautiful, personalized campaigns in minutes. Manage campaigns, schedule sends, run A/B tests, and use powerful templates - all in one professional tool!

## 🆕 What's New in v1.4

### 🎨 Template Engine (v1.4)
- **Advanced variables** with Jinja2 syntax: `{{first_name}}`, `{{company}}`, `{{email}}`
- **Conditional content**: `{% if country == "IT" %}Ciao{% else %}Hello{% endif %}`
- **Template library** to save and reuse your best templates
- **Real-time preview** with actual data from your CSV
- **Validation** for missing variables and syntax errors
- **Categorize templates** (promo, newsletter, cold outreach, etc.)

### 🧪 A/B Testing (v1.3)
- **Split recipients** with custom ratio (50/50 or any percentage)
- **Test variations** with different subjects and content
- **Side-by-side preview** to compare variants A and B
- **Separate tracking** for variant A and B sends
- **Local statistics** without requiring cloud services

### ⏰ Scheduling & Throttling (v1.2)
- **Schedule campaigns** for future delivery with date/time picker
- **Timezone support** (UTC, CET, EST, PST, JST, AEST)
- **Rate limiting** with customizable emails per minute (0-60)
- **Pause/Resume** campaigns during sending
- **Auto-resume** after crashes with state persistence

### 📊 Campaign Manager (v1.1)
- **Organize campaigns** with names, tags, and notes
- **Track progress** with status (Draft, Scheduled, Sent)
- **View statistics** including sent count and errors
- **Search & filter** campaigns in real-time
- **Duplicate campaigns** to reuse successful templates
- **Professional UI** with tab navigation

[See full version history](Version.md)

## Quick Start
- Place `EmailCampaignManager.exe` in any folder and double-click it.
- Your browser opens at `http://localhost:5000` automatically. Allow it through your antivirus if prompted (PyInstaller apps can trigger false positives).

## 📊 Using Campaign Manager (NEW!)

### Create a Campaign
1. Click the **Campaigns** tab
2. Click **➕ New Campaign**
3. Compose your email in the **Compose** tab
4. Click **⚙️ Settings** to set name, tags, and notes
5. Click **💾 Save** to save your progress

### Manage Campaigns
- **Search**: Type in the search box to find campaigns
- **Filter**: Click Draft/Scheduled/Sent to filter by status
- **Edit**: Click on a campaign card to open and edit it
- **Actions**: Click **⋮** for Duplicate or Delete options

### Send a Campaign
1. Select or create a campaign
2. Load your CSV file with recipients
3. Configure SMTP settings
4. Click **🚀 Send Emails**
5. Statistics update automatically!

## 🎨 Using Templates (NEW in v1.4!)

### Create a Template
1. Click the **Templates** tab
2. Click **➕ New Template**
3. Enter template name and description
4. Write your email using variables and conditions:
   - Variables: `{{first_name}}`, `{{company}}`, `{{email}}`
   - Conditions: `{% if country == "IT" %}Ciao{% else %}Hello{% endif %}`
5. Select a category (promo, newsletter, cold, follow-up)
6. Click **💾 Save Template**

### Use a Template
1. In the **Compose** tab, click **📄 Load Template**
2. Select a template from the library
3. The subject and body are automatically filled
4. Variables will be replaced with real data from your CSV

### Template Syntax
- **Variables**: Use any column from your CSV with `{{column_name}}`
  - Example: `Hello {{first_name}}, welcome to {{company}}!`
- **Conditions**: Show/hide content based on data
  - Example: `{% if company %}at {{company}}{% endif %}`
- **Preview**: Click the preview button to see how it renders with sample data

## 🧪 Running A/B Tests (NEW in v1.3!)

### Set Up an A/B Test
1. Create or edit a campaign
2. Click **⚙️ Settings**
3. Enable **A/B Test Mode**
4. Set your split ratio (default 50/50)
5. Go to **Compose** tab
6. Enter **Variant A** subject and body
7. Enter **Variant B** subject and body
8. Click **👁️ Preview** to compare side-by-side

### Send A/B Test
1. Load your CSV with recipients
2. Configure SMTP settings
3. Click **🚀 Send A/B Test**
4. Recipients are automatically split (e.g., 50% get A, 50% get B)
5. View separate statistics for each variant

## ⏰ Scheduling Campaigns (NEW in v1.2!)

### Schedule for Later
1. Create or edit a campaign
2. Click **⚙️ Settings**
3. Set **Scheduled Date & Time**
4. Select your **Timezone**
5. Click **💾 Save**
6. Campaign shows ⏰ badge and will send automatically

### Control Send Rate
1. In Campaign Settings, adjust **Emails per Minute** slider
2. Set to 0 for maximum speed (no limit)
3. Set to 1-60 to control delivery rate
4. Helps improve deliverability and avoid rate limits

### Pause & Resume
1. During sending, click **⏸️ Pause** if needed
2. Campaign state is saved automatically
3. Click **▶️ Resume** to continue from where it stopped
4. If app crashes, campaigns auto-resume on restart

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
- **Use variables** from your CSV with Jinja2 syntax: `{{first_name}}`, `{{email}}`, `{{company}}`, or any CSV column.
- **Legacy syntax** still supported: `{name}` and `{email}` work as before.
- **Add conditions**: `{% if company %}at {{company}}{% endif %}` shows content only if field exists.
- If Name is missing, the **Default Greeting** is used (e.g., "Dear Friend").
- **Load templates** from the Templates tab to reuse your best messages.
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


