# Hi, I'm Sharath 👋

**Security engineering & data analytics.** I build things I can explain in depth,
then measure them until they tell me something I didn't expect.

I recently ran a **[30-day build challenge](https://github.com/nishankswamy/30-days)**:
ten projects across security and data, each shipped with a benchmark, tests, CI,
and a written finding that contradicts the obvious assumption. `831 tests · CI on
every repo · 2 capstone platforms`.

The rule for every project: build the core, do the hard half, then *break it and
write down the result*. A few that came out of that:

- **Forged a MAC without the key.** `SHA256(secret‖message)` is length-extendable —
  a digest *is* the hash's internal state. Appended `role=admin` to a signed message
  in milliseconds. → [applied-cryptography](https://github.com/nishankswamy/applied-cryptography)
- **A benchmark that lied by 600x.** A "678x cache speedup" was timing the
  error-fallback path; the real number was 1.1x. Now I distrust results that flatter
  the design. → [url-shortener](https://github.com/nishankswamy/url-shortener)
- **ML lost to five lines of statistics.** Isolation Forest scored *worse* than an
  STL+MAD baseline on security telemetry at a realistic base rate. "Use a model" is
  not a strategy. → [anomaly-detection](https://github.com/nishankswamy/anomaly-detection)

## The two capstones

| | What it is | The finding |
|---|---|---|
| 🛡️ **[SIEM platform](https://github.com/nishankswamy/siem-capstone)** | Multi-source ingest → inline detection + behavioural baselines → entity-first investigation | Detects a full attack campaign in 13ms; alert → evidence is one indexed lookup, **26x** faster than a scan |
| 📊 **[Analytics platform](https://github.com/nishankswamy/analytics-platform)** | Quality-gated ingest → star schema with cubes → self-serve queries with a cost display | What breaks at scale is **memory, not compute** — 530 B/row as dicts vs 50 on disk |

## All ten projects

Cryptography · detection engineering · a columnar query engine · anomaly detection ·
network traffic analysis · an exactly-once streaming pipeline · differential privacy —
plus the two capstones. Everything is defensive; the only things I attack, I attack in
my own code.

**→ [github.com/nishankswamy/30-days](https://github.com/nishankswamy/30-days)** — the
full index, findings, and case studies.

## Reach me

📧 sharath.surya176@gmail.com
