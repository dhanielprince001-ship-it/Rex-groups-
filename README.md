# Rex Groups — Corporate Website

Responsive React + Vite corporate website concept for Rex Groups, featuring a Three.js animated visual, business divisions, about section, and a Supabase-backed contact form.

## Set up Supabase

1. Create a project at https://supabase.com/.
2. In the Supabase dashboard, open **SQL Editor** and run the SQL in `supabase/schema.sql`.
3. Find the Project URL and publishable/anon key in the Supabase project API settings.
4. Copy `.env.example` to `.env` and fill in these two values for local development.
5. In Vercel, add the same values under **Project Settings → Environment Variables**:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
6. Redeploy after saving environment variables.

The contact form saves submissions to the `contact_messages` table. Row Level Security allows visitors to insert messages but does not allow public reads. Never put a Supabase `service_role` or secret key in frontend code.

## Run locally

```bash
npm install
npm run dev
```

## Build for production

```bash
npm run build
npm run preview
```

## Deploy to Vercel

1. Upload this folder to a GitHub repository.
2. In Vercel, import that repository.
3. Framework preset: Vite (usually detected automatically).
4. Build command: `npm run build`
5. Output directory: `dist`
6. Add the two Supabase environment variables above, then deploy.

## Contact details

- Email: rexgroups.uk@gmail.com
- Phone: +234 803 356 4331
