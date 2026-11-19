# D-Language Studio Karnal — GitHub Pages + Google Sheets Package

This package runs **100% on GitHub Pages** with **no backend server** required. Anyone you sell it to can host it free on GitHub Pages and attach their own custom domain.

## What's Included
- `index.html` — The main website (loads your latest text, photos, and fees automatically).
- `admin.html` — Admin panel to edit website text, photos, and course fees (Default PIN: `1234`).
- `config.js` — Single-line config where you paste your Google Apps Script URL.
- `google_apps_script.gs` — Free script that connects your forms to a **Leads** tab in Google Sheets and stores your website edits in a **SiteContent** tab.

---

## Setup Guide (Zero Coding Required)

### Step 1: Connect Google Sheets (5 minutes)
1. Create a new **Google Sheet** in your Google Drive.
2. Click **Extensions → Apps Script**.
3. Delete any sample code and paste the entire contents of `google_apps_script.gs`.
4. Change `ADMIN_PIN = "1234"` to your own secret PIN if desired.
5. Click **Deploy → New deployment** → Select type **Web app**.
   - **Execute as:** Me
   - **Who has access:** Anyone
6. Click **Deploy**, authorize it, and copy the **Web app URL**.
7. Open `config.js` and paste that URL inside `APPS_SCRIPT_URL: "..."`.

### Step 2: Host on GitHub Pages & Add a Custom Domain
1. Create a new repository on GitHub and upload `index.html`, `admin.html`, and `config.js`.
2. Go to **Settings → Pages** in your GitHub repository.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch` (`main` / `root`) and click **Save**.
4. Your site is now live!
   - Website: `https://yourusername.github.io/your-repo/`
   - Admin Panel: `https://yourusername.github.io/your-repo/admin.html`
   - Student Inquiries: Open your **Google Sheet → Leads** tab.
5. **To connect a buyer's custom domain:** In **Settings → Pages → Custom domain**, enter their domain (e.g. `dlanguagestudiokarnal.com`) and point their domain's DNS records to GitHub Pages.
