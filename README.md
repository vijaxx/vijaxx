### Hi, I'm Vijay 👋

Computer Science Engineering graduate (B.Tech, July 2026 — GITAM Deemed University, Hyderabad), based in India and open to relocation.

I build **systems that run themselves** — pipelines that go from raw input to a finished, published product with no manual step in between — and I write my READMEs the way I'd want a reviewer to read code: what actually runs, what's measured, and what isn't there yet.

**Open to:** data & analytics, backend, full-stack, and AI-automation roles.

---

#### Live in production

**[Multi-Platform Content Automation Pipeline](https://github.com/vijaxx/Multi-Platform-Short-Form-Content-Automation-Pipeline)**
Sources stock footage, renders a captioned 9:16 video with FFmpeg, writes platform-tailored copy with Claude, and publishes to YouTube Shorts, Rumble, and Facebook Reels on a cron schedule. YouTube goes through the Data API; Rumble and Facebook ship no usable upload API, so those are driven over the Chrome DevTools Protocol against a real logged-in browser — the only approach that survives Cloudflare bot detection and React's rejection of synthetic clicks.

**[redditreels](https://github.com/vijaxx/redditreels)**
Finds a story, rewrites it into 45-second hook-first narration with an LLM, generates voiceover with per-word timing, renders karaoke-style animated captions, publishes across platforms — then measures how each upload performed and feeds that back into next week's source, title, and hashtag choices. Includes a self-healing layer that pauses the pipeline automatically after a failure streak rather than publishing garbage on a schedule.

**[pinforge](https://github.com/vijaxx/pinforge)**
Turns one theme into a complete digital product line: print-ready PDF, Pinterest pin creatives, SEO copy, and a manifest — then posts the pins and tracks performance in SQLite (impressions, saves, clicks per pin; sales by referrer).

**[kdp-puzzle-engine](https://github.com/vijaxx/kdp-puzzle-engine)**
Generates print-ready puzzle books (word search, Sudoku, mazes) end to end at 300 DPI, with an unattended factory mode that rotates recipes to avoid near-duplicate titles, and a pre-upload compliance check that catches the specific formatting issues that trigger Amazon KDP review flags.

**[stylebyclaud](https://github.com/vijaxx/stylebyclaud)**
A zero-dependency affiliate storefront, machine-generated and deployed on GitHub Pages. **Live:** [vijaxx.github.io/stylebyclaud](https://vijaxx.github.io/stylebyclaud/)

Three of these repos carry green CI, unit tests, and an MIT license. Recurring pattern across all five: Chrome DevTools Protocol automation for platforms with no workable API, a provider-agnostic LLM shim (one interface, routes to whichever of Anthropic/Gemini/Groq/Ollama has a configured key), and failing safe — dry-run modes, pre-publish sanity checks, automatic pause on failure streaks.

---

#### Applied projects

Built to work end-to-end, with real test suites and measured results rather than illustrative numbers — each README states plainly what was run and verified versus what wasn't.

**[book-demand-predictor](https://github.com/vijaxx/book-demand-predictor)** — Flask app pairing content-based recommendations (TF-IDF + cosine similarity) with monthly demand forecasting (Ridge regression on lag and seasonality features). Validated on a temporal holdout against a naive last-month baseline — R² 0.883, 14% better MAE than the baseline. Chart.js admin dashboard, 21 tests including target-leakage guards.

**[algo-trading-system](https://github.com/vijaxx/algo-trading-system)** — backtesting engine for five intraday strategies (ORB, EMA+RSI, VWAP reversion, Supertrend, Bollinger) against a full Indian transaction-cost model (STT, GST, stamp duty, brokerage, exchange charges). 92 tests, including a no-lookahead proof and a real concurrency bug caught by the test suite and fixed (a stale position-count race that could oversubscribe the risk cap). Results are reported honestly — two of five strategies lose money after real costs, which is in the README rather than filtered out. Paper trading only; no live order routing.

**[supermart-erp](https://github.com/vijaxx/supermart-erp)** — Java Servlets/JSP/JDBC MVC app: employee and inventory management, session-based auth with role separation, JOIN-based reporting. 60 tests plus live curl verification against the running server, including a SQL-injection payload attempted against the real login endpoint and confirmed rejected.

**[library-management-system](https://github.com/vijaxx/library-management-system)** — Java Swing + JDBC desktop app: transactional book issue/return workflow, per-tier borrowing limits, overdue fine calculation. 44 tests, including a rollback test built around a JDBC proxy that fails mid-transaction to prove a partial issue never persists.

**[reels-scheduler](https://github.com/vijaxx/reels-scheduler)** — Instagram Reels scheduling and publishing pipeline: SQLite-backed content queue, timezone-aware slot scheduling, content-hash duplicate prevention, dry-run-by-default publisher. 80 tests, including a full clone-and-rerun from a bare `git clone` with zero config to confirm it's genuinely reproducible, not just working in one workspace.

**[marketgen](https://github.com/vijaxx/marketgen)** — client-onboarding platform: a 7-step, 87-question wizard with conditional branching and resumable sessions, multi-tenant data isolation, and a content-generation pipeline behind a provider interface (deterministic offline stub by default). 63 tests plus a live browser walkthrough of the wizard's branching logic. Real Postgres row-level-security policies are included as reviewed SQL but not executed (no live Postgres in this environment) — stated directly in the README rather than implied as tested.

**[wsn-secure-routing](https://github.com/vijaxx/wsn-secure-routing)** — WSN routing simulation comparing baseline LEACH against a hardened variant (RSA-1024 mutual auth, AES-GCM, an Interlock Protocol implementation resisting man-in-the-middle key exchange). 71 tests including live MITM-detection scenarios. Measured result: the secure variant costs ~5.5% more energy under normal conditions, but is ~8% *more* energy-efficient than baseline under an active sybil attack, since it rejects 100% of forged node identities that the baseline wastes energy servicing. Reported as measured, not tuned to a target figure.

---

#### Tech

`Python` · `Java` · `SQL` · `SQLite` / `H2` / `PostgreSQL` · `HTML/CSS/JS`

`Flask` · `FastAPI` · `Servlets/JSP` · `Swing` — application frameworks
`Pandas` · `NumPy` · `scikit-learn` · `Chart.js` — data analysis, ML, reporting
`FFmpeg` · `Pillow` · `reportlab` — media & document generation
Chrome DevTools Protocol · `Selenium` — browser automation
LLM APIs — Anthropic, Gemini, Groq, local Ollama
`JUnit 5` · `pytest` — every repo above ships with a real, passing test suite
`git` · GitHub Actions

---

📫 [LinkedIn](https://www.linkedin.com/in/kondani-vijay-vardhan-b2729035a/) · Hyderabad, India · willing to relocate
