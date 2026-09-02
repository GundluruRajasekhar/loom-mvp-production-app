# LOOM — MVP to Production

This bundle documents the path from LOOM's current GitHub Pages prototype to a production launch.

## Files
- **`index.html`** — Visual status page laying out the five launch threads (Hosting, CI/CD, Monitoring, Payments & Legal, Go-to-Market) and the BYOK-vs-Hosted decision. Open directly in a browser or deploy as-is.
- **`Requirements.md`** — What must be true for launch, split by whether LOOM stays bring-your-own-key or becomes a hosted product.
- **`tasks.md`** — The actionable checklist, phased to match the requirements.
- **`readme.md`** — This file.

## The Core Decision
Everything here branches on one question: does LOOM stay **bring-your-own-key** (fast, no backend, launch in days), or become a **hosted product** (requires a backend, billing, and legal docs, launch in weeks)?

The current recommendation is to launch BYOK first, on the existing GitHub Pages setup with a custom domain, to validate demand before taking on backend and billing complexity.

## Deploying This Bundle
Push all four files into the LOOM repo (or a `/launch` subfolder) using the **"choose your files"** upload link on GitHub — the drag-and-drop uploader has been unreliable in past deployments. Once GitHub Actions is wired up (see `tasks.md`, Phase 2), future updates deploy automatically on push.
