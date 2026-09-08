# Make KDOG'S STAG live

## 1. Create Supabase project
Create a project at https://supabase.com/.

## 2. Create the database
In Supabase, open SQL Editor, paste the contents of `SUPABASE.sql`, and run it.

## 3. Add your Supabase details
Open `index.html` and replace:
- `YOUR_SUPABASE_URL`
- `YOUR_SUPABASE_PUBLISHABLE_KEY`

Use the project URL and publishable key from Supabase Project Settings > API.

## 4. Test locally
Open `index.html` in a browser. Submit a pub suggestion from two different browsers/devices. Both should see the same word cloud after the realtime update.

## 5. Deploy
Upload the folder to a GitHub repository and import that repository into Vercel, or use the Vercel CLI from the folder:

    npm i -g vercel
    vercel --prod

No build step is required; this is a static HTML site.

## Security note
The public browser key is intended for browser use. Never put a Supabase service-role/secret key into `index.html`.

The one-vote rule is enforced with a browser-generated UUID stored in localStorage plus a database unique constraint. This stops normal repeat voting from the same browser, but it is not a strong identity system: a determined person can clear storage or use another browser/device. For a stag site this is usually sufficient; use Supabase Auth if you need stronger voting controls.
