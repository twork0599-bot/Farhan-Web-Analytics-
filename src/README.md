# Farhan Web Analytics

Next.js landing page with Supabase Auth, PostgreSQL, RLS, Realtime and privacy-conscious visitor analytics.

## Setup
1. Install dependencies with npm install.
2. Set NEXT_PUBLIC_SUPABASE_URL and NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY in deployment environment.
3. The connected Supabase project already has the analytics schema and security policies applied.
4. The analytics-ingest Edge Function is deployed in Supabase. It uses the server-side SUPABASE_SERVICE_ROLE_KEY and never exposes it to the browser.
5. Visit /admin, create your account, then run supabase/bootstrap_admin.sql after replacing the email. Sign out and sign in again.

Analytics begins only after consent. Random UUIDs in browser storage identify visitors and sessions; no fingerprinting or sensitive form capture is used. Country is approximate and supplied by the edge platform. Daily retention cleanup is enabled. The dashboard reads real records only; empty states contain no sample data.
