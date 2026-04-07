# FoodLog.ai 🥣

You type food descriptions like "two eggs, toast, and coffee," and it logs estimated macros. No dropdowns, accounts, or external data storage. This is your private AI food companion that you host yourself, part of the Cocapn Fleet.

**Live demo:** https://foodlog-ai.casey-digennaro.workers.dev

## Quick Start
1.  **Fork** this repository.
2.  **Deploy** it directly to Cloudflare Workers (no build step).
3.  Optionally, add your own LLM API key for nutrition estimation.

Your personal log will be live in about a minute.

## How It Works
This is a single Cloudflare Worker. It stores your meal history on the edge using KV storage and calls an LLM only when you request nutrition estimates. You control the entire application.

**Features:**
*   **Natural Language Input:** Log meals in plain English.
*   **Private Storage:** All entries remain within your worker instance.
*   **Nutrition Estimates:** Provides rough macro approximations via LLM.
*   **Data Export:** One-click download of your full log as JSON.
*   **Zero Dependencies:** One TypeScript file. No `npm install`.
*   **Free Tier:** Runs entirely on Cloudflare's free plan.
*   **Fleet Compatible:** Connects with other Cocapn agents.

**A Specific Limitation:**
Nutrition estimates are general approximations. For a complex meal like "chicken stir-fry with brown rice," the estimated calories may vary by +/- 20% from a precise calculation. This tool is for trend tracking, not medical-grade accuracy.

## Why Fork This?
You host your own copy. No central service can change, shut down, or monetize your data. If you want new features—like water tracking—you edit the source code directly.

## License
MIT License

<div style="text-align:center;padding:16px;color:#64748b;font-size:.8rem"><a href="https://the-fleet.casey-digennaro.workers.dev" style="color:#64748b">The Fleet</a> &middot; <a href="https://cocapn.ai" style="color:#64748b">Cocapn</a></div>