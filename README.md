# Kipa Web

Web presence for Kipa - landing page, Terms of Service, Privacy Policy, and share collection placeholder.

## Project Structure

```
src/
  pages/
    index.astro       # Landing
    terms.astro       # Terms of Service
    privacy.astro     # Privacy Policy
    share/
      [id].astro      # Share placeholder (future)
  layouts/
    BaseLayout.astro  # Shared layout + footer
    Layout.astro      # Default layout wrapper
  components/
    Footer.astro      # Footer with legal links
public/
  favicon.png
  icon.png
  splash-icon.png
```

## Commands

| Command         | Action                                      |
| :-------------- | :------------------------------------------ |
| `bun install`   | Installs dependencies                       |
| `bun run dev`   | Starts dev server at `localhost:4321`       |
| `bun run build` | Build production site to `./dist/`          |
| `bun run preview` | Preview the build locally                 |

## Deployment (Vercel)

1. Push the repo to GitHub.
2. Go to [vercel.com](https://vercel.com) and import the repository.
3. Vercel auto-detects Astro; no config needed. Deploy.
4. Add custom domain `kipaapp.com` in Project Settings > Domains.

## App Integration

After the web is live, update the Kipa app `app.json`:

```json
"legal": {
  "termsUrl": "https://kipaapp.com/terms",
  "privacyUrl": "https://kipaapp.com/privacy"
}
```
