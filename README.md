### Hi, I'm Vijay 👋

Computer Science Engineering graduate (B.Tech, July 2026 — GITAM Deemed University, Hyderabad), based in India and open to relocation.

I build **systems that run themselves** — pipelines that go from raw input to a finished, published product with no manual step in between. Most of what's below runs on a schedule, unattended, in production.

**Open to:** data & analytics, backend, full-stack, and AI-automation roles.

---

#### What I've built

**[Multi-Platform Content Automation Pipeline](https://github.com/vijaxx/Multi-Platform-Short-Form-Content-Automation-Pipeline)** — *live in production*
Sources stock footage, renders a captioned 9:16 video with FFmpeg, writes platform-tailored copy with Claude, and publishes to YouTube Shorts, Rumble, and Facebook Reels on a cron schedule. YouTube goes through the Data API; Rumble and Facebook ship no usable upload API, so those are driven over the Chrome DevTools Protocol against a real logged-in browser — the only approach that survives Cloudflare bot detection and React's rejection of synthetic clicks.

**[redditreels](https://github.com/vijaxx/redditreels)** — *live in production*
Finds a story, rewrites it into 45-second hook-first narration with an LLM, generates voiceover with per-word timing, renders karaoke-style animated captions, publishes across platforms — then measures how each upload performed and feeds that back into next week's source, title, and hashtag choices. Includes a self-healing layer that pauses the pipeline automatically after a failure streak rather than publishing garbage on a schedule.

**[pinforge](https://github.com/vijaxx/pinforge)** — turns one theme into a complete digital product line: print-ready PDF, Pinterest pin creatives, SEO copy, and a manifest — then posts the pins and tracks performance in SQLite (impressions, saves, clicks per pin; sales by referrer).

**[kdp-puzzle-engine](https://github.com/vijaxx/kdp-puzzle-engine)** — generates print-ready puzzle books (word search, Sudoku, mazes) end to end at 300 DPI, with an unattended factory mode that rotates recipes to avoid near-duplicate titles, and a pre-upload compliance check that catches the specific formatting issues that trigger Amazon KDP review flags.

**[book-demand-predictor](https://github.com/vijaxx/book-demand-predictor)** — a Flask app pairing content-based recommendations (TF-IDF + cosine similarity) with monthly demand forecasting (Ridge regression on lag and seasonality features). Validated on a temporal holdout against a naive last-month baseline — R² 0.883, and 14% better MAE than the baseline — with a Chart.js admin dashboard and 21 tests, including guards against target leakage in the lag features.

**[stylebyclaud](https://github.com/vijaxx/stylebyclaud)** — a zero-dependency affiliate storefront, machine-generated and deployed on GitHub Pages. **Live:** [vijaxx.github.io/stylebyclaud](https://vijaxx.github.io/stylebyclaud/)

---

#### Recurring themes across these

- **Chrome DevTools Protocol browser automation** for the platforms that ship no workable API — attaching to a real, already-authenticated Chrome rather than launching an automated one, because that's what actually gets past bot detection.
- **A provider-agnostic LLM shim** — call sites use one Anthropic-shaped interface; the shim routes to whichever provider has a configured key (Anthropic, Gemini, Groq, or local Ollama), so a pipeline keeps running without depending on a paid key.
- **Measurement and feedback loops** — reconciling inconsistent per-platform metrics into one comparable signal, then acting on it.
- **Failing safe** — pre-upload sanity checks, dry-run modes, unlisted-by-default publishing, and automatic pause on failure streaks.

Three of these repos carry green CI, unit tests, and an MIT license.

---

#### Experience

**Machine Learning Intern** — Synycs Enterprise, Hyderabad *(June – July 2025)*
Acquired, cleaned, and validated customer datasets from multiple sources; evaluated model performance using precision, recall, F1 and ROC-AUC; analysed the drivers of customer churn and presented findings as recommendations supporting retention decisions.

---

#### Tech

`Python` · `SQL` · `Java` · `SQLite` / `MySQL` · `HTML/CSS/JS`

`Pandas` · `NumPy` · `Matplotlib` · `Chart.js` — data analysis & reporting
`FFmpeg` · `Pillow` · `reportlab` — media & document generation
Chrome DevTools Protocol · `Selenium` — browser automation
LLM APIs — Anthropic, Gemini, Groq, local Ollama
`git` · GitHub Actions

---

📫 [LinkedIn](https://www.linkedin.com/in/kondani-vijay-vardhan-b2729035a/) · Hyderabad, India · willing to relocate
