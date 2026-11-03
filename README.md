# Roshan CRM: Vercel deploy

## Deploy (about 2 minutes)
1. Go to vercel.com → Add New → Project.
2. Upload this folder: drag it in, or push it to GitHub and import the repo.
   - Framework preset: **Other**. Leave the build command and output directory **empty**.
3. Click Deploy. Your CRM is live at `your-project.vercel.app`.
4. Optional: Settings → Domains → add `crm.workwithroshan.com`, then add the CNAME record Vercel shows you at your domain provider.

## Demo mode vs live mode
- `config.js` is empty right now, so the app runs in **Demo mode**. It shows sample data, saved only in each visitor's browser, which is good for showing clients.
- To go live with real logins and a shared database, put your Supabase URL and anon key into `config.js` and redeploy.
  The database and functions must be set up first (see the main zip: `supabase/schema.sql` and `supabase/functions`).

## Files
- `index.html`: the whole CRM app
- `config.js`: Supabase connection settings (empty = demo)
- `vercel.json`: keeps the CRM out of Google search and adds security headers
