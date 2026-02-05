# 🦞C Application: Chain Data Agent

> ⚠️ **READ FIRST:** Your agent must be LIVE and WORKING. I will test it. Broken agents = instant reject.

## 📋 Basic Info

- **Agent Name:** Chain Data Agent
- **Live URL:** `https://chain-data-agent-staging.up.railway.app`
- **Agent Card:** `https://chain-data-agent-staging.up.railway.app/.well-known/agent-card.json`
- **GitHub Repo:** https://github.com/henryf10h/chain-data-agent
- **Builder:** henryf10h
- **Contact:** henryf10h (GitHub)

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
AI agents and on-chain traders need real-time, multi-chain crypto data —
prices, gas fees, and TVL — but currently have to hit 3+ fragmented APIs
individually, each with different auth, rate limits, and response formats.
There is no single unified source an agent can call to get a full picture
of the market across chains in one request. Developers and agents waste
time stitching together CoinGecko, Owlracle, and DeFiLlama manually.
```

## 💡 The Solution

_How does your agent solve this? What makes it better than alternatives?_

```
Chain Data Agent aggregates real-time data from CoinGecko (prices),
Owlracle (gas), and DeFiLlama (TVL) into a single Lucid Agent with
clean, typed endpoints. Any agent can call one URL to get prices across
any coins, gas speed tiers across 8 EVM chains, or TVL rankings.

The premium /analysis endpoint goes further: it pulls all three data
sources in parallel, then feeds them to an AI model (via OpenRouter)
to produce actionable market analysis — overviews, DeFi insights,
trading signals, or gas optimization strategies. Pay 0.01 USDC via
x402 on Base Sepolia, get a structured analyst report back.
```

## 🔧 Live Endpoints

**List ALL your paid endpoints with working examples:**

| Endpoint | Price | Example Call |
|----------|-------|--------------|
| `POST /entrypoints/prices/invoke` | Free | `curl -X POST https://chain-data-agent-staging.up.railway.app/entrypoints/prices/invoke -H "Content-Type: application/json" -d '{"coins":["bitcoin","ethereum"],"currencies":["usd"]}'` |
| `POST /entrypoints/gas/invoke` | Free | `curl -X POST https://chain-data-agent-staging.up.railway.app/entrypoints/gas/invoke -H "Content-Type: application/json" -d '{"chains":["eth","base","poly"]}'` |
| `POST /entrypoints/tvl/invoke` | Free | `curl -X POST https://chain-data-agent-staging.up.railway.app/entrypoints/tvl/invoke -H "Content-Type: application/json" -d '{"limit":5}'` |
| `POST /analysis` | 0.01 USDC | `curl -X POST https://chain-data-agent-staging.up.railway.app/analysis -H "Content-Type: application/json" -d '{"focus":"overview"}'` |

_I will run these commands. They must work._

## 💰 Monetization

| Question | Answer |
|----------|---------|
| **Target customer** | AI agents and developers building on-chain trading bots or DeFi dashboards |
| **Why they pay** | The /analysis endpoint saves significant dev time by aggregating 3 data sources + AI synthesis into one call. No need to build, maintain, or prompt an LLM yourself. |
| **Pricing rationale** | 0.01 USDC is low enough to call frequently in automated pipelines, high enough to cover OpenRouter inference costs and sustain the agent. |
| **Projected usage** | 500–2000 calls/day from agent pipelines once discoverable via Lucid network |

## 🏆 Why You Should Win

_What makes this application stand out? Why is this agent exceptional?_

```
This agent is production-ready out of the box. Three free endpoints
deliver real-time data from the most reliable free crypto APIs
(CoinGecko, Owlracle, DeFiLlama) with zero auth required. The paid
/analysis endpoint is the differentiator: it orchestrates all three
data sources in parallel, then runs structured AI analysis via
OpenRouter, returning actionable insights in a single x402-gated call.

The agent card is fully populated, all endpoints are live and tested,
x402 payments are wired on Base Sepolia, and it's built cleanly on the
Lucid Agents SDK with Hono + Bun. No mocks, no placeholders, no TODO
items. Every endpoint returns real data right now.
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
