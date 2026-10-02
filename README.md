# Awesome Hyperliquid Copy Trading [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**A curated list of copy-trading and vault platforms, tools, bots and resources on [Hyperliquid](https://hyperliquid.xyz/) — 2026.**

> On Hyperliquid, "copy trading" spans three overlapping models: **native vaults** (pool your funds with a lead trader's on-chain strategy), **third-party copy apps and bots** (mirror a wallet's fills into your own self-custodial account), and the **public leaderboard** you use to find traders worth following. Because every fill is on-chain, you can verify a trader's real record before you follow — "trust, but verify" is enforced by the infrastructure.

> PRs welcome — see [Contributing](#-contributing). Neutral, no referral spam.

---

## Contents

- [How Copy Trading Works on Hyperliquid](#-how-copy-trading-works-on-hyperliquid)
- [Native: Vaults, HLP & the Leaderboard](#-native-vaults-hlp--the-leaderboard)
- [Copy-Trading Apps & Bots](#-copy-trading-apps--bots)
- [Open-Source Copy-Trading Bots](#-open-source-copy-trading-bots)
- [Trader & Vault Analytics](#-trader--vault-analytics)
- [Docs & API](#-docs--api)
- [Risk & Safety](#-risk--safety)
- [Contributing](#-contributing)
- [License](#-license)

> **Legend** — 🟢 Live · 🟡 Beta/Regional · 🔴 Inactive · 🔓 Self-custodial · 🤖 Bot/automation · 📖 Open source

---

## 📖 How Copy Trading Works on Hyperliquid

There is no single "copy trading" button that fits everyone. The three common paths:

- **Vaults (native).** A lead trader (or the protocol) runs a strategy; depositors' funds are pooled and traded together. Depositors share profits pro-rata and pay the vault leader a **10% performance fee** (fixed for user vaults). You deposit and withdraw on-chain; you do not place the trades yourself. Anyone can start a user vault (subject to a minimum deposit and a one-time protocol vault-creation fee).
- **Copy apps & bots (mirroring).** A service watches a target wallet and replicates its opens/closes into **your own account** at your chosen size and leverage. Your funds stay in your account; you grant trade permission via a Hyperliquid API/agent wallet (which can trade but **cannot withdraw**).
- **Leaderboard-driven manual copy.** Use the public leaderboard + analytics tools to find consistent traders, then follow or mirror them.

> ⚠️ Past performance is not indicative of future results. Copying a trader means inheriting their drawdowns and their risk. Nothing here is financial advice.

---

## 🏦 Native: Vaults, HLP & the Leaderboard

Built into Hyperliquid itself — fully on-chain and auditable.

| Name | What it is | Notes | Status | Link |
| --- | --- | --- | --- | --- |
| **Hyperliquid Vaults** 🔓 | Deposit into a lead trader's on-chain strategy | User vaults charge a fixed 10% performance fee; every fill is auditable | 🟢 Live | [app.hyperliquid.xyz/vaults](https://app.hyperliquid.xyz/vaults) |
| **HLP (Hyperliquidity Provider)** 🔓 | Protocol-run market-making & liquidation vault | The "conservative anchor" vault; earns from market-making and liquidations, not a lead trader's calls | 🟢 Live | [app.hyperliquid.xyz/vaults](https://app.hyperliquid.xyz/vaults) |
| **Hyperliquid Leaderboard** | Public ranking of traders by PnL over 24h/7d/30d/all-time | The starting point for finding traders to follow; live positions are public | 🟢 Live | [app.hyperliquid.xyz/leaderboard](https://app.hyperliquid.xyz/leaderboard) |

---

## 📱 Copy-Trading Apps & Bots

Self-custodial apps and services to follow or mirror traders. Your keys / funds stay with you.

| Name | Type | Notable | Status | Link |
| --- | --- | --- | --- | --- |
| **Dexly** 🔓 | Mobile app | Self-custodial iOS/Android app for Hyperliquid perps, spot, tokenized stocks & prediction markets, with copy trading | 🟢 Live | [dexly.trade](https://dexly.trade/) |
| **HyperDash — Copytrade** | Web terminal | Ranks traders by a "Copy Score" and lets you mirror positions from an analytics terminal | 🟢 Live | [hyperdash.com/copytrading](https://hyperdash.com/copytrading) |
| **pvp.trade** 🤖 | Telegram bot | Trade Hyperliquid perps/spot from a Telegram group; share, copy and counter-trade friends | 🟢 Live | [pvp.trade](https://pvp.trade/) |
| **Hypercopy** 🔓📖 | Browser tool | "Hyper stupid" in-browser copy trader; you supply your own API key, it stops when you close the tab | 🟢 Live | [hypercopy.xyz](https://hypercopy.xyz/) |
| **GDEX** 🤖 | Web terminal + agent tools | Multi-chain trading terminal by Gemach DAO; mirror Hyperliquid perp traders picked by volume or PnL with fixed or proportional sizing, optional opposite-direction copying and TP/SL; trades run from GDEX managed wallets. Open-source MCP server and agent skills for AI agents | 🟢 Live | [gdex.pro](https://gdex.pro/) |

> Building a Hyperliquid copy-trading app? Open a PR — accurate, neutral descriptions only.

---

## 🤖 Open-Source Copy-Trading Bots

Run-it-yourself bots that mirror a target wallet into your own account (you provide an API/agent wallet). Review the code and understand the risks before running anything with trade permissions.

- [**MaxIsOntoSomething/Hyperliquid_Copy_Trader**](https://github.com/MaxIsOntoSomething/Hyperliquid_Copy_Trader) 📖🤖 — Automated copy-trading bot with real-time monitoring and position sizing.
- [**jestersimpps/hyperliquid-copytrader**](https://github.com/jestersimpps/hyperliquid-copytrader) 📖🤖 — Copy-trading bot with a real-time dashboard.
- [**Brobicho/HLCopy**](https://github.com/Brobicho/HLCopy) 📖🤖 — Monitors target addresses and replicates their positions.
- [**Gajesh2007/copytrading-agent**](https://github.com/Gajesh2007/copytrading-agent) 📖🤖 — Copytrading agent built on the typed Hyperliquid SDK (TypeScript).
- [**artiya4u/hypercopy-xyz**](https://github.com/artiya4u/hypercopy-xyz) 📖🤖 — Source for the Hypercopy browser service above.

---

## 📊 Trader & Vault Analytics

Tools to research a trader or vault **before** you follow — the "verify" half of "trust, but verify".

- [**HyperDash**](https://hyperdash.com/) — Analytics terminal: wallet cohorts, whale alerts, copy-score rankings.
- [**HyperTracker**](https://hypertracker.io/) — Real-time wallet & whale tracker across 1.6M+ wallets, filterable leaderboard, read-only.
- [**HypurrScan**](https://hypurrscan.io/) — Hyperliquid explorer & dashboard for on-chain activity.
- [**ASXN Hyperliquid Dashboard**](https://hyperscreener.asxn.xyz/) — Perps, spot, HIP-3, revenue and top-trader analytics.
- [**VaultVision**](https://vaultvision.tech/vaults/scanner) — Read-only Hyperliquid vault scanner for risk scores, drawdown, TVL, positions, flows, deposit status, entry context and alerts; supports research and manual mirroring, not automated copy trading.

---

## 📚 Docs & API

- [**Vaults — Hyperliquid Docs**](https://hyperliquid.gitbook.io/hyperliquid-docs/hypercore/vaults) — How vaults, fees and deposits work.
- [**Info endpoint — Hyperliquid API**](https://hyperliquid.gitbook.io/hyperliquid-docs/for-developers/api/info-endpoint) — Read a user's fills, positions and vault details (read-only).
- [**Hyperliquid Python SDK**](https://github.com/hyperliquid-dex/hyperliquid-python-sdk) — Official SDK, useful for building mirroring bots.

---

## 🔒 Risk & Safety

- **API/agent wallets can trade but not withdraw.** When a copy service asks for an API key, it's an *agent* wallet scoped to trading. Never share your seed phrase or a key that can move funds out.
- **Verify the on-chain record.** A leaderboard screenshot proves nothing. Check the full equity curve, drawdowns and whether returns came from consistency or one lucky bet.
- **Understand vault mechanics.** Vault leaders take a performance fee; deposits/withdrawals may have lockups. Read the vault page before depositing.
- **Copying inherits risk.** High-leverage traders can be liquidated fast — and so can you if you mirror them 1:1.

> ⚠️ Availability and legality of leveraged products vary by jurisdiction. This list is informational; nothing here is financial advice.

---

## 🤝 Contributing

PRs welcome — the Hyperliquid copy-trading space ships fast.

1. **Fork** and create a feature branch (e.g. `feature/add-foo`).
2. **Match the column structure** of the section you're editing.
3. **Quality bar:** live (or clearly-marked beta), working link, genuinely serves Hyperliquid copy trading / vaults.
4. **One row/bullet per project.** Use the legend (🟢 / 🟡 / 🔴 / 🔓 / 🤖 / 📖) consistently.
5. **No referral spam.** Neutral, accurate descriptions; disclose affiliations.

For corrections (broken links, inactive projects), open an issue or a small PR.

---

## 📄 License

[CC0](https://creativecommons.org/publicdomain/zero/1.0/) — public domain. Made for the Hyperliquid community.

---

> **Maintainer note:** This list is maintained by the team behind [Dexly](https://dexly.trade/) (Hyper Lion LTD). Dexly is listed among many copy-trading options; the goal is a genuinely useful, neutral directory of the whole category. **Not affiliated with Hyperliquid.** Suggestions and competing projects are welcome via PR.
