# CartGuard AI

Describe what you need. Compare eligible fictional products. Approve an exact quote and verify its PayPal sandbox capture.

[Watch the actual working demo on YouTube](https://youtu.be/tsteOh_ElLw) — 1 minute 19 seconds, real internal-browser footage with English captions, sandbox funds only.

**Complete runnable source:** [cartguard-ai-source.zip](cartguard-ai-source.zip). The ZIP contains the application, locked dependencies, frozen synthetic evaluation, tests, licensed pinned model assets and sanitized sandbox evidence. It preserves the source tree's paths. Download and extract it before running the commands below. This repository uses an archive distribution because the internal-browser file picker rejected a directory upload; the archive was independently extracted and tested.

## Run the functional build

1. Download `cartguard-ai-source.zip` from this repository. If using GitHub's Download ZIP, also extract the included source ZIP.
2. Extract it to obtain the `cartguard-ai` folder and open a terminal there.
3. With Node.js 24+ and npm installed, run:

```sh
npm ci --no-fund --no-audit
npm test
npm start
```

4. Open `http://127.0.0.1:8765/` in a desktop browser. Use this exact host; `localhost` and public hosting are not configured. The verified setup used Node 24.18.0.

The downloaded package has **47 passing tests** and a real CPU MiniLM inference check from a clean extraction. The pinned model is bundled, hash-checked and loaded with remote model access disabled. Installing npm dependencies still needs internet. No paid inference endpoint, card-backed plan or hosting is required.

Search the supplied long-video-call request with Local AI · MiniLM: CallComfort H2 is first in the verified catalog/model revision. At a USD 1.00 maximum, no products qualify. Review or release a locked local quote. Without sandbox credentials, search/quotes work and payment stays disabled; no mock payment is substituted.

## PayPal sandbox test

See [JUDGE-QUICKSTART.md](JUDGE-QUICKSTART.md), also inside the archive. In the same browser session, open `http://127.0.0.1:8765/sandbox-setup` and connect **your own authorized sandbox app**. Credentials/tokens stay only in local server memory and the form clears immediately. Never use live credentials or real payment data.

Approve an exact fresh quote, create a sandbox order and use official hosted approval. Existing sandbox-account passwords are entered directly by the tester. If PayPal offers guest checkout, use only its official generated synthetic sandbox card and fictional buyer data, with account creation OFF. Do not bypass any security check.

Return alone is not proof of payment. The server must read and match the full bound order, CAPTURE intent, quote references, exact total/currency and one final COMPLETED capture before PAID. Captures are blocked after ten-minute quote expiry. No real goods are fulfilled. Restart clears credentials while SQLite preserves recorded outcomes in ignored local data files.

## Actual evidence and limitations

Two genuine sandbox captures completed October 25, 2026. The recorded run is order `3JR416104F576222F`, capture `0ND61345NK317822H`, USD 69.00. The earlier durable-receipt run is order `2MA31808Y5978251A`, capture `9N875108U25554533`; its receipt survived an actual server restart. Failed and expired test orders are separate and are not presented as successful payments.

Frozen agent-authored synthetic evaluation: 32 relevance queries, top-1 30/32 MiniLM versus 16/32 TF-IDF; nDCG@5 0.9707 versus 0.6770. Four additional no-eligible cases pass; zero tested budget/stock violations. Two ranking disagreements are preserved. These are not independent user labels or real-world impact measurements.

The 47 tests include **fixture** provider failures, process-exit recovery and concurrency. Actual sandbox success is separate evidence; no production reliability, provider idempotency guarantee, fraud reduction, conversion benefit or competition rank is claimed.

The source ZIP SHA-256 and each file's hash are in [SOURCE-PACKAGE-MANIFEST.json](SOURCE-PACKAGE-MANIFEST.json). No credentials, cookies, local database, model cache, node_modules, private research or account pages are distributed. Judges need their own authorized sandbox access for independent payment testing; the app's AI and quote features need no payment account. Keep these source/setup materials available free through December 15, 2026, 21:30 IST, the stated end of judging.

## Provenance and licensing

Original event-local application, catalog and evaluation created October 25, 2026. No code was copied from another competition. Pro/agents assisted concept selection, coding, labels and documentation under the human's delegation; the human did not personally author or review every artifact. The final supplemental Pro reply failed to load; the official-source release review is agent-led fallback. No registration or final submission receipt is implied by this repository.

MIT application source: [LICENSE](LICENSE). The bundled MiniLM assets retain Apache-2.0; their unmodified file hashes, upstream revision, attribution and license are in `models/minilm/` inside the archive. Dependencies retain their own licenses. See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md). CartGuard is not affiliated with or endorsed by PayPal.
