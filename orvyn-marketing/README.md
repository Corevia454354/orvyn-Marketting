# ORVYN Marketing Site

Single self-contained `index.html` — no build step, no framework. Deploy it
to Firebase Hosting, Vercel, Netlify, or any static host.

## Before going live
1. Deploy the backend (`orvyn-backend`) so `submitContactSalesLead` has a
   live URL.
2. In `index.html`, replace:
   ```js
   const CONTACT_SALES_ENDPOINT = "REPLACE_WITH_CLOUD_FUNCTION_URL";
   ```
   with the deployed function's URL, e.g.
   `https://us-central1-<project-id>.cloudfunctions.net/submitContactSalesLead`.
3. Until step 2 is done, the form will show a clear "not configured yet"
   error instead of failing silently — no fake success messages.

## What's real vs. not yet built
- The form genuinely posts to your backend and creates a `contact_sales_leads`
  document once wired up — leads appear in Firestore immediately, ready for
  the Admin Dashboard's Sales Leads view (next slice).
- No analytics/tracking scripts included — add your own if needed.
- Sections match spec §9 (all 14); logo is a simple geometric placeholder
  mark (O/V hexagon) — swap in final brand artwork when ready.
