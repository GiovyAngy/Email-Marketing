# 📧 Email Campaign Manager v1.6

[![Version](https://img.shields.io/badge/version-1.6-blue.svg)](https://github.com/GiovyAngy/Email-Marketing)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Documentation](https://img.shields.io/badge/docs-online-brightgreen.svg)](https://giovyangy.github.io/Email-Marketing/)

**Professional desktop email marketing tool** - Send beautiful, personalized campaigns in minutes. Manage campaigns, schedule sends, run A/B tests, validate your emails, and optimize deliverability - all in one powerful application!

## 📥 Download

This repository contains the **source code** for Email Campaign Manager. 

**To use the application**, download the ready-to-use executable:

➡️ **[Download EmailCampaignManager.exe](https://github.com/GiovyAngy/Email-Marketing/releases/latest)** ⬅️

> 💡 **No installation required** - Just download and run the `.exe` file!

## 📚 Documentation

For complete guides, tutorials, and feature documentation, visit:

🔗 **[Official Documentation](https://giovyangy.github.io/Email-Marketing/)**

---

## ✨ Features Overview

## 🆕 What's New in v1.6

### 📊 Deliverability Tools OFFLINE (v1.6)
- **Subject line analysis** with spam word detection
- **Subject length check** for optimal open rates (30-50 chars recommended)
- **Excessive capitalization** and special character detection
- **HTML structure validation** for email clients
- **Image alt text checker** for accessibility
- **Broken link detection** and suspicious URLs
- **Text-to-HTML ratio** analysis
- **Attachment size warnings** (>5MB flagged)
- **Suspicious file type detection** (.exe, .bat, etc.)
- **Content quality tips** for better engagement
- **Deliverability score** (0-100) with grade (Excellent/Good/Fair/Poor)
- **Actionable suggestions** for improving inbox placement
- **100% offline** - no data sent to third parties

### 🛡️ CSV Validation & Security (v1.5)
- **Dry-Run validation** with one click before sending
- **Email format check** with regex validation
- **Duplicate detection** to avoid sending multiple emails to same address
- **Missing fields check** for name and template variables
- **SMTP existence verification** (optional, experimental)
- **Detailed reports** with errors, warnings, and statistics
- **Download report** as .txt file for record-keeping
- **Warning threshold** to prevent accidental mass sends (default: 100 recipients)
- **Confirmation modal** when exceeding threshold
- **Customizable validation options** in Settings

### ✍️ Email Signature & Privacy Policy (v1.4.1)
- **Default signature** support in Text and HTML format
- **Privacy policy/unsubscribe** links for GDPR compliance
- **Checkbox selection** in Compose, Campaigns, and A/B Tests
- **Automatic append** to email body (with separator for HTML)
- **Settings panel** for easy configuration
- **Help button** with link to online documentation

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

## � Check Deliverability (NEW in v1.6!)

### Analyze Your Email Before Sending
1. Compose your email in the **Compose** tab
2. Click **📊 Check Deliverability** button (under CSV section)
3. View comprehensive analysis:
   - 📧 **Subject Line**: Spam words, length, capitalization
   - 🎨 **HTML Structure**: Images, links, text ratio
   - 📎 **Attachments**: Size, file types
   - ✍️ **Content**: Length, call-to-action, copy quality
4. Review your **Deliverability Score** (0-100)
5. Follow **Top Suggestions** to improve inbox placement
6. Expand each section for detailed issues and fixes

### Understanding the Score
- **90-100 (Excellent)** 🌟 - Ready to send!
- **75-89 (Good)** 👍 - Minor improvements recommended
- **60-74 (Fair)** ⚠️ - Several issues to fix
- **0-59 (Poor)** ❌ - High spam risk, needs work

### Pro Tips
- Keep subject lines between 30-50 characters
- Avoid spam words like "FREE", "URGENT", "BUY NOW"
- Add alt text to all images
- Keep attachments under 5MB
- Maintain good text-to-HTML ratio
- Use clear call-to-action

## 🔍 Using CSV Validation (v1.5)

### Run a Dry-Run Before Sending
1. Load your CSV file in the **Compose** tab
2. Click **🔍 Dry-Run Validation** button (appears under CSV load)
3. Select validation options:
   - ✓ Check Email Format
   - ⚠️ Check Duplicates
   - 📋 Check Missing Fields
   - 🔍 Check SMTP Existence (slow)
4. Click **▶️ Run Validation**
5. Review the report and fix any errors
6. **NEW**: Click **✅ Use Clean CSV** to automatically remove invalid/duplicate emails
7. Download the full report for your records

### Configure Warning Threshold
1. Go to **Settings** tab
2. Find **Validation & Security** section
3. Set your preferred warning threshold (default: 100)
4. Choose default validation options
5. Click **💾 Save Settings**

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

## ✍️ Add Signature & Privacy Policy (NEW in v1.4.1!)

### Configure Your Signature
1. Click the **⚙️ Settings** tab
2. Enter your signature in the **Text** field (for plain text emails)
3. Optionally, add an **HTML** version for styled emails
4. Click **💾 Save Settings**

### Configure Privacy Policy/Unsubscribe
1. In the **⚙️ Settings** tab, scroll to Privacy Policy section
2. Add your unsubscribe link and privacy policy text
3. For HTML emails, use `<a>` tags for clickable links
4. Click **💾 Save Settings**

### Use in Emails
1. In the **Compose** tab, find the checkboxes above the email editor:
   - ✅ **Include Signature** - Adds your signature at the end
   - ✅ **Include Privacy Policy** - Adds privacy/unsubscribe info
2. Check the boxes you want to include
3. For A/B tests, each variant has its own checkboxes
4. The signature and privacy are automatically appended when sending

💡 **Tip**: HTML versions are used for HTML emails, text versions for plain text emails!

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

## 📞 Support & Contact

Need help or have questions? Get in touch with the developer:

[![Contact Developer](https://img.shields.io/badge/Contact-Developer-blue?style=for-the-badge&logo=person)](https://giovyangy.github.io/Lebenlauf/index.html#kontakt)

📚 **Full Documentation**: [https://giovyangy.github.io/Email-Marketing/](https://giovyangy.github.io/Email-Marketing/)

💡 **In-App Help**: Click the **❓ Help** button in the top-right corner for quick guides

---

## 📦 Repository Contents

This repository includes:
- 📂 **Source Code** - Python/Flask backend and JavaScript frontend
- 📄 **TemplateCSV.csv** - Ready-to-use contact template
- 🛠️ **Build Scripts** - PyInstaller configuration for creating the `.exe`
- 📖 **Documentation Files** - README, changelog, and version history

**For the compiled application**, see [Releases](https://github.com/GiovyAngy/Email-Marketing/releases)

---

## 🛠️ Development

<details>
<summary>Build from Source</summary>

### Requirements
- Python 3.12+
- All dependencies in `backend/requirements.txt`

### Build Steps
```bash
cd backend
pip install -r requirements.txt
python build_exe.bat
```

The executable will be created in `backend/dist/EmailCampaignManager.exe`

</details>

---

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details

## 👨‍💻 Author

**Giovanni Angileri**

- Portfolio: [giovyangy.github.io](https://giovyangy.github.io/Lebenlauf/)
- GitHub: [@GiovyAngy](https://github.com/GiovyAngy)
- Contact: [Get in touch](https://giovyangy.github.io/Lebenlauf/index.html#kontakt)

---

<div align="center">

**⭐ Star this repo if you find it useful!**

[Download](https://github.com/GiovyAngy/Email-Marketing/releases) • [Documentation](https://giovyangy.github.io/Email-Marketing/) • [Report Bug](https://github.com/GiovyAngy/Email-Marketing/issues)

</div>


