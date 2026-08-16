# OneDrum — Server-Certified Rhythm Performance Scoring

**White paper, v1.0 — August 2026.** How [OneDrum](https://onedrum.io) certifies human
timing on consumer devices whose clocks lie: the audible clock, calibration with no
calibration step, drift tracking, an anti-spoof gate that calibration cannot blind, and a
score anyone can verify.

📄 **Read it:** [WHITEPAPER.md](WHITEPAPER.md) · [日本語版 WHITEPAPER.ja.md](WHITEPAPER.ja.md) ·
canonical versions at [onedrum.io/whitepaper](https://onedrum.io/whitepaper) / [onedrum.io/whitepaper-ja](https://onedrum.io/whitepaper-ja)

🥁 **Try the engine:** [onedrum.io](https://onedrum.io) — Viking Row, the first experience
built on it. First beat in ~3 seconds, no install.

🔏 **Verify a score:** [the certified-score spec](https://onedrum.io/blog/verifying-certified-scores)

## What this is

Every mechanism described is running in production and backed by the field data shown
(1,234 genuine attempts across desktop, iPhone, and Android). The short version:

- **The client renders; the server decides.** Clients send timestamps on the media
  timeline; an isolated per-session authority computes calibration, acceptance, and
  plausibility, and issues an HMAC-signed certified payload.
- **Calibration is a side effect of playing.** No calibration screen, no count-in — the
  first bar is an unscored warm-up whose answer becomes the device offset, with a guarded
  adaptive fallback and in-play drift re-centring.
- **Anti-spoof that calibration cannot blind.** Machine-plausibility is computed on raw,
  calibration-invariant residuals — a replay bot at constant offset stays flagged even
  after calibration centres its score.

## Status

**Patent pending** — U.S. Provisional Applications No. 64/089,862 (filed June 13, 2026)
and No. 64/134,723 (filed August 15, 2026).

© 2026 Nick Kovac. Published for reference. All rights reserved; no license — including no
patent license — is granted by this publication. See the
[terms](https://onedrum.io/terms). Operator inquiries welcome.
