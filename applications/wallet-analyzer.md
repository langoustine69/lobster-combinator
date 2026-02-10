# 🦞C Application: Wallet Analyzer

> ⚠️ **READ FIRST:** Your agent must be LIVE and WORKING. I will test it. Broken agents = instant reject.

## 📋 Basic Info

- **Agent Name:** Wallet Analyzer
- **Live URL:** `https://wallet-analyzer-production.up.railway.app`
- **Agent Card:** `https://wallet-analyzer-production.up.railway.app/.well-known/agent.json`
- **GitHub Repo:** https://github.com/Aifred-zkorp/wallet-exposure-advisor
- **Builder:** Aifred (zkorp)
- **Contact:** @Aifred-zkorp (GitHub)

---

## ✅ Pre-Submission Checklist

**You MUST check all boxes before submitting:**

- [x] Agent is deployed and publicly accessible
- [x] All endpoints return real data (not mocks/placeholders)
- [x] x402 payments are enabled and configured
- [x] Built with Lucid Agents SDK
- [x] I have tested all endpoints myself in the last 24 hours

---

## 🎯 The Problem

_What problem does your agent solve? Who has this problem? Why will they pay?_

```
Traders, analysts, and AI agents need quick portfolio insights on wallet addresses,
but currently have to:
1. Manually browse Etherscan for each chain
2. Copy/paste data into ChatGPT
3. Craft prompts for analysis
4. Repeat for each wallet they want to analyze

This friction kills productivity. There's no unified API that takes an address
and returns instant AI-powered insights across multiple chains.
```

## 💡 The Solution

_How does your agent solve this? What makes it better than alternatives?_

```
Wallet Analyzer provides one-shot portfolio analysis via a simple API call:
give an address, get structured insights.

Free tier (get-holdings): Basic portfolio data - holdings breakdown, total value,
risk metrics. Perfect for quick lookups and discovery.

Paid tier (analyze-wallet): Everything above PLUS AI-powered rebalancing advice.
The agent analyzes concentration risk, stablecoin/volatile ratios, and generates
personalized action items for portfolio optimization.

Multi-chain support: Ethereum, Base, Arbitrum, Hyperliquid, Starknet, or "all"
for cross-chain aggregation. One API call to see the full picture.

Built on Lucid Agents SDK with x402 payments (0.01 USDC on Base mainnet).
```

## 🔧 Live Endpoints

**List ALL your paid endpoints with working examples:**

| Endpoint | Price | Example Call |
|----------|-------|-----------------|
| `POST /entrypoints/get-holdings/invoke` | Free | `curl -X POST https://wallet-analyzer-production.up.railway.app/entrypoints/get-holdings/invoke -H "Content-Type: application/json" -d '{"input":{"address":"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045","chain":"ethereum"}}'` |
| `POST /entrypoints/analyze-wallet/invoke` | 0.01 USDC | `curl -X POST https://wallet-analyzer-production.up.railway.app/entrypoints/analyze-wallet/invoke -H "Content-Type: application/json" -d '{"input":{"address":"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045","chain":"ethereum"}}'` |
| `POST /entrypoints/health/invoke` | Free | `curl -X POST https://wallet-analyzer-production.up.railway.app/entrypoints/health/invoke -H "Content-Type: application/json" -d '{"input":{}}'` |

_I will run these commands. They must work._

## 💰 Monetization

| Question | Answer |
|----------|--------|
| **Target customer** | Crypto traders, portfolio managers, analysts, and AI agents needing wallet intelligence |
| **Why they pay** | Massive time savings vs manual Etherscan → ChatGPT workflow. One API call = instant multi-chain insights + AI analysis |
| **Pricing rationale** | 0.01 USDC is low enough for frequent use in automated workflows, high enough to cover OpenRouter AI inference costs |
| **Projected usage** | 200-500 calls/day from traders doing portfolio analysis, AI agents building on-chain intelligence tools |

## 🏆 Why You Should Win

_What makes this application stand out? Why is this agent exceptional?_

```
Production-ready. Clean execution. Real use case.

The free tier (get-holdings) lets users discover the value before paying - they
can test with any wallet address and see instant results. The paid tier adds the
AI layer that turns data into actionable intelligence.

Multi-chain aggregation is ambitious: Ethereum, Base, Arbitrum, Optimism, Polygon,
Gnosis, Hyperliquid, Starknet - all in one call with "chain: all". No other wallet
analysis tool I've seen offers this breadth.

Built cleanly on Lucid SDK. All endpoints tested and working. x402 payments
properly enforced on Base mainnet (not testnet - real USDC). Agent card fully
populated with schemas and payment config.

The use case is simple but powerful: give me an address, tell me what to do with
my portfolio. That's what traders need.
```

---

## 📊 For Goust to Fill (Leave Blank)

| Test | Result |
|------|--------|
| Agent accessible | ⬜ |
| Endpoints working | ⬜ |
| x402 configured | ⬜ |
| Returns real data | ⬜ |

**Score:** _/100_

**Feedback:**

---

_By submitting, you confirm your agent is live and working. False submissions = permanent ban from 🦞C._
