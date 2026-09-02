# Tasks — LOOM: MVP to Production

## Phase 0 — Decide
- [ ] Choose BYOK or Hosted path
- [ ] Record the decision (this file assumes BYOK unless updated)

## Phase 1 — Hosting
- [ ] Register a custom domain
- [ ] Point the domain at GitHub Pages (BYOK) or Vercel/Railway (Hosted)
- [ ] *(Hosted only)* Stand up a minimal backend to hold the API key

## Phase 2 — Continuous Deployment
- [ ] Add `.github/workflows/deploy.yml` to the LOOM repo
- [ ] Verify a push to `main` triggers an automatic redeploy
- [ ] Confirm the live domain reflects the change within a few minutes

## Phase 3 — Monitoring
- [ ] Create a free Sentry project
- [ ] Add the Sentry snippet to `index.html`
- [ ] Trigger a test error and confirm it appears in Sentry
- [ ] *(Hosted only)* Add UptimeRobot monitoring on the backend URL

## Phase 4 — Payments & Legal *(skip entirely if BYOK)*
- [ ] Set up Stripe Billing
- [ ] Draft Privacy Policy (disclose Anthropic API data flow)
- [ ] Draft Terms of Service
- [ ] Publish both and link them from the site footer

## Phase 5 — Go-to-Market
- [ ] Record a short demo video showing all four agents and the reasoning trace
- [ ] Write the Product Hunt launch post
- [ ] Prepare posts for Hacker News / r/LocalLLaMA / X
- [ ] Schedule launch day

## Deployment Reminder
When pushing these files to the LOOM repo on GitHub, use the **"choose your files"** link rather than drag-and-drop — drag-and-drop has been unreliable in past deployments.
