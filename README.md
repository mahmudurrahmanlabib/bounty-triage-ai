# 🎃 Bounty Triage AI

In-browser, privacy-first triage for bug bounty / vulnerability reports, powered by an **open-weight AI model**.

**Live demo:** https://mahmudurrahmanlabib.github.io/bounty-triage-ai/

Paste a report and get:
- Suggested vulnerability class (XSS, SQLi, IDOR, SSRF, RCE, Auth bypass, CSRF, Info disclosure)
- Suggested severity (Critical / High / Medium / Low)
- A copy-ready triage note

## How it works
- Uses [Transformers.js](https://github.com/huggingface/transformers.js) to run
  [`Xenova/mobilebert-uncased-mnli`](https://huggingface.co/Xenova/mobilebert-uncased-mnli) (Apache-2.0) as a zero-shot classifier.
- Everything runs locally in the browser via WebAssembly — no server, no API key, and the (often sensitive) report never leaves your machine.
- Single static `index.html`, hosted on GitHub Pages.

## Run locally
```bash
python3 -m http.server 8000
```
Then open http://localhost:8000.

## Why
Bug bounty platforms receive many reports; first-pass triage is repetitive. A small open model that runs offline gives triagers a quick, private first guess — a human still makes the call.

Built at **Hacktoberfest Hack Day Khulna x HackZar 2026**. MIT licensed — PRs welcome!
