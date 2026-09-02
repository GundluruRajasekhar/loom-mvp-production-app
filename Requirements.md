# Requirements — LOOM: MVP to Production

## Purpose
Define what must be true for LOOM (four-agent orchestration engine: Warp, Weft, Heddle, Selvage) to move from GitHub Pages prototype to a production launch.

## 1. Foundational Decision
- **R1.1** — A decision must be made and recorded: LOOM launches as a bring-your-own-key (BYOK) tool, or as a hosted product with a backend holding the API key.
- **R1.2** — All downstream requirements below are conditional on this decision, as marked.

## 2. Hosting & Infrastructure
- **R2.1** — The live site must be reachable at a custom domain, not a raw `github.io` URL.
- **R2.2** *(Hosted path only)* — A backend service must exist to hold the Anthropic API key server-side and must never expose it to the client.
- **R2.3** *(Hosted path only)* — The backend must meter usage per user to prevent unbounded API spend.

## 3. Continuous Deployment
- **R3.1** — Pushing to `main` must automatically redeploy the live site with no manual upload step.
- **R3.2** — The deploy workflow must not require a build step unless one is introduced for the hosted backend.

## 4. Monitoring
- **R4.1** — Client-side JavaScript errors in the router's agent-dispatch logic must be captured and visible without waiting for user reports.
- **R4.2** *(Hosted path only)* — Backend uptime must be monitored, since a downed backend disables all four agents simultaneously.

## 5. Payments & Legal *(Hosted path only)*
- **R5.1** — A subscription billing flow must exist before any paid access is offered.
- **R5.2** — A Privacy Policy must disclose that user task inputs are transmitted to Anthropic's API.
- **R5.3** — A Terms of Service covering acceptable use must be published before public launch.
- **R5.4** — *(BYOK path)* — None of R5.1–R5.3 are required, since no payment is processed and no key is centrally held.

## 6. Go-to-Market
- **R6.1** — A demo showing the visible reasoning trace across all four agents must be available at launch (video and/or live walkthrough).
- **R6.2** — A launch post must be prepared for Product Hunt and relevant developer communities.
- **R6.3** — Enterprise sales materials (pitch deck, CRM, SLA) are explicitly out of scope for this launch.

## Out of Scope for This Launch
- Enterprise SSO / RBAC
- Custom enterprise contracts or SLAs
- Multi-seat team billing

These remain valid future requirements once BYOK demand is validated, not blockers for this launch.
