# DuckLarry — ducklarry.com

The public pages of the DuckLarry app, served by GitHub Pages at
https://ducklarry.com/.

- `privacy/` — the privacy policy, in English and Ukrainian. Generated, not
  edited here: it is made from `docs/privacy-policy.md` in the app's own
  repository by `tools/privacy-page.py`.
- `index.html` — the start page, also the App Store support address.
- `beta/` — the page for beta testers (16–30 November 2026), in English and
  Ukrainian: what DuckLarry is, how to install it through TestFlight's public
  link, and how to send feedback. Not indexed by search engines.
- `confirmed/` — where the link in the email that confirms an address leads
  (Supabase's Site URL), in English, Ukrainian and Spanish: the address is
  confirmed, go back to the app and sign in; or, when Supabase reports an
  error, that the link did not work. It drops the fragment Supabase adds, so
  the sign-in tokens do not stay in the address bar. Not indexed by search
  engines.
