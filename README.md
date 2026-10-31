# TimeWise

Timesheets, overtime, salary sheets and payroll reports (PDF, Excel, CSV) for small companies. One static file, no server, no cost.

## Put it online (GitHub Pages)
1. Create a new repository on GitHub (public is fine, the file contains no company data).
2. Upload `index.html` and this `README.md`.
3. Repository **Settings > Pages > Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder `/ (root)`. Save.
4. After a minute your site is live at `https://<your-username>.github.io/<repository-name>/`. Share that link with any company.

## Accounts
- Each company opens the link, chooses **Create account** (company name, username, password) and gets its own private workspace. Another company can create its own account the same way.
- Data is encrypted in the browser with the account password (AES-256) and stored only on that device and browser. Nobody else, including you as the site owner, can read it.
- A forgotten password cannot be recovered. Use **Download backup** (Employees tab) regularly, especially at year end. A backup can be restored in any browser after signing in.
- Because data stays in the browser, a second device needs a backup restored on it. Shared multi-device logins would need a cloud database (for example Firebase or Supabase) and is a separate upgrade.

