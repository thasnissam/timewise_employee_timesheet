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

## First use
Sign in, then **Employees > Restore backup** to load a prepared employee list (see `my-employees.json`; keep it private, do not upload it to a public repository), or add employees one by one with monthly salary and basic salary.

## Rules built in
- Hourly rate = basic salary / 30 / 8 (editable). Monthly salary is the amount paid; basic only sets the rate.
- Total hrs = start to end. Regular hrs capped at 8. Hours beyond 9 are overtime at rate x 1.25. All Sunday work is overtime at rate x 1.5.
- Each leave day is deducted as monthly salary / 30. Public holidays are paid.
