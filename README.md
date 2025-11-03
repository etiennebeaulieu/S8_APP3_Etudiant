# Insecure CI Demo — Static Web App

This is the static web app used in the Insecure CI demo. The app is intentionally tiny — the pipeline (`.github/workflows/ci-insecure-owasp.yml`) contains the course's insecure CI/CD practices (OWASP Top 10 CI/CD risks).

To build locally:
1. `npm install` (not required; no deps)
2. `npm run build`  # copies public/ -> dist/

To preview locally:
- simply open `public/index.html` in your browser, or use a static server:
  `npx http-server public -p 3000`

Simulate supply chain attack:
- Toggle attack mode with `curl https://5649243.xyz/admin/toggle`
- Get attack mode status with `curl https://5649243.xyz/admin/status`
Note: It doesn't work on Eduroam
