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
  (Supabase's Site URL), in English: the address is
  confirmed, go back to the app and sign in; or, when Supabase reports an
  error, that the link did not work. It drops the fragment Supabase adds, so
  the sign-in tokens do not stay in the address bar. Not indexed by search
  engines.
  A link for a new password that comes here — when the server is not told
  where else to go — is passed on to `reset/`.
- `reset/` — where the link in the email that resets a password leads, in
  English: a field for the new password, with an eye to show it. The link
  carries a one-time code in the fragment (`#token_hash=…&type=recovery`),
  which never reaches this site's server and is dropped from the address bar
  at once. Opening the page uses nothing up — mail services that open links
  before the reader does leave it working; the code is traded for a session
  (`/auth/v1/verify`) only when the password is saved, the password sent
  (`PUT /auth/v1/user`), and the session ended, here alone, then or when the
  page is left. Supabase's own link, with the session in the fragment, works
  too. When the link was no good, it says so and how to get a new one. Not
  indexed by search engines.
