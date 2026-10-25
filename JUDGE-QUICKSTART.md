# Run CartGuard locally

First download and extract `cartguard-ai-source.zip` from the public repository. In these instructions, the repository/application root means the extracted `cartguard-ai` folder, which contains package.json, src/, public/, models/ and tests.

CartGuard is a local desktop-browser sandbox prototype. It does not need paid hosting, a paid AI API, a real card or live PayPal funds. The catalog and inventory are fictional. Do not use live credentials or real payment data.

## Prerequisites

- Node.js 24 or newer and npm. Verified locally with Node 24.18.0.
- A desktop browser and network access for npm packages. The pinned model is bundled with license/attribution; inference makes no model download or remote AI call.
- For actual payment testing only: your existing PayPal developer Sandbox application credentials. No credentials are included in this repository. The [official developer dashboard](https://developer.paypal.com/dashboard/applications/sandbox) explains obtaining sandbox access. Account availability and authentication requirements depend on the tester and country.

## Install and start

From this repository's root:

```sh
npm ci --no-fund --no-audit
npm test
npm start
```

Open `http://127.0.0.1:8765/`. Use this exact address, not localhost: the local server deliberately requires the exact Host and Origin. Keep the terminal running and retain the browser's cookies. Data persists in the ignored `data/` directory. Browser sessions are local, with no public user-account system.

## Three-minute functional check

1. Keep Local AI · MiniLM selected and search the supplied request about comfortable long video calls. First use verifies SHA-256 hashes and initializes the bundled pinned weights. Remote model access is disabled. A missing/tampered model fails visibly; it never silently falls back to keyword ranking. CallComfort H2 should be first in the verified model/catalog revision.
2. Change Maximum total to `1.00` and search again: no products qualify. Restore `80.00`. Compare Keyword baseline · TF-IDF if desired; it is explicitly labelled as non-AI.
3. Review a locked quote. Verify quantity 1 and USD 69.00. Before creating a provider order, Release quote closes only that local quote. The catalog, budget and quantity determine totals; browser-supplied price/currency fields are rejected.

Without sandbox credentials the search/quote checks work and payment stays disabled. This is an explicit access boundary, not a mock payment simulation.

## Genuine sandbox checkout

1. Open `http://127.0.0.1:8765/sandbox-setup` in the same browser session. Enter your **Sandbox** client ID and secret there. The local server verifies sandbox OAuth, retains them only in memory and clears the form immediately. Do not enter a Personal buyer password or live credential in this form. Do not save credentials in source, screenshots or evidence.
2. Return to the app, search with the real model, review a fresh quote and approve its exact sandbox total. Click Create PayPal sandbox checkout, then open the approval page.
3. Use an existing sandbox test buyer, entering its password directly on the official sandbox site. Alternatively, if PayPal offers guest checkout, use only [official generated sandbox test-card data](https://developer.paypal.com/credit-card-number-generator) with fictional test-buyer data and turn account creation OFF. Never use a real card or actual person's private contact details. Do not bypass a password, OTP, CAPTCHA or security check.
4. Return to CartGuard within the ten-minute quote window. Check payment state · read only should show APPROVED. Return alone is not payment proof. Click Capture approved sandbox order once.
5. PAID is displayed only after a server-side full-order read verifies the bound order ID, CAPTURE intent, exact quote references and total/currency, and one final COMPLETED capture. The receipt shows sandbox order and capture IDs. Reload retains it. No real goods are fulfilled.

Restarting clears the credentials/tokens, while SQLite retains quote/payment records. Reconnect your own sandbox application for further provider operations. An already verified receipt remains readable in the same browser session after restart. A fresh capture is blocked after quote expiry; read-only reconciliation remains available. Do not silently extend a quote or create another order to conceal an uncertain result.

## Evidence and limits

The documented October 25 run completed a real sandbox capture of USD 69.00, order `2MA31808Y5978251A`, capture `9N875108U25554533`. The receipt is historical test evidence, not credentials or a live demo endpoint. Start with your own fresh database/session for independent testing.

`npm test` currently runs 47 automated tests. Payment failure, simulated process-exit recovery and concurrency tests use fixtures; they are not actual PayPal failure experiments. `npm run evaluate` executes real CPU inference and writes `evidence/ai-evaluation-v2.json` inside the repository. See README.md for the benchmark's agent-authored labels, errors and limitations.

This is not a production checkout, fraud model, compatibility recommender or claim of universal exactly-once payment processing. No real-user benefit or competition rank has been measured. MIT application source and dependency/model notices are included.
