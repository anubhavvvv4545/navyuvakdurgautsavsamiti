# navyuvakdurgautsavsamiti — public website + admin

## What this package does
- `index.html` = public website
- `admin.html` = phone-friendly admin panel
- `config.js` = Supabase connection settings
- `schema.sql` = database/storage setup

## One-time setup
1. Create a Supabase project.
2. In Supabase, create an Authentication user for the Samiti admin.
3. Create a Storage bucket named `gallery` and make it public.
4. Run `schema.sql` in Supabase SQL Editor.
5. Put the project's URL and anon/publishable key into `config.js`.
6. Upload these files to a static host such as GitHub Pages, Netlify, or Cloudflare Pages.
7. Public site: `/index.html`
8. Admin: `/admin.html`

## Security
Do NOT put a Supabase service_role/secret key in `config.js`.
Use only the anon/publishable browser key.
For production, tighten the storage/database policies to the specific admin account.

## Phone workflow
Open the admin page on the phone -> log in -> choose photos -> Upload & Publish.
Visitors then see the photos on the public page.
