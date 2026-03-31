# Redirect Landing Page (Static)

A minimal static landing page that shows a small "Connecting" indicator and automatically redirects after ~2–3 seconds.

## Configure

Edit `index.html`:

- `DEFAULT_TARGET`: destination URL
- `DELAY_MS`: redirect delay in milliseconds

Optional: `?to=` override is supported but restricted by an allowlist (`ALLOWED_HOSTS`).

## Deploy (GitHub + Cloudflare Pages)

1. Create a new GitHub repo (public or private).
2. Upload / commit these files to the repo root:
   - `index.html`
   - `README.md`
3. In Cloudflare Dashboard → **Pages** → **Create a project** → **Connect to Git**.
4. Select your repo and set:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: `/`
5. Deploy. Cloudflare will auto-deploy on every push to your selected branch.

## Test

- Open your Cloudflare Pages URL and verify it redirects.
