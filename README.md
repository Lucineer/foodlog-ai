# FoodLog.ai
You have better things to do than manually log every ingredient.

An AI companion for meal logging and nutrition tracking. A Cocapn Fleet vessel built on Cloudflare Workers.

**Live URL:** https://foodlog-ai.casey-digennaro.workers.dev

---

## Why this exists
Many food trackers require tedious data entry and lock features behind subscriptions. This is an alternative: a private agent you control, designed for quick, natural interaction.

---

## What it does
*   **Natural Language Logging** – Describe what you ate in plain English. No barcode scanning or complex menus.
*   **Background Nutrition Analysis** – Estimates macronutrients and calories without interrupting your flow.
*   **Private Data Storage** – Your meal history is stored on your own edge worker. Data stays on your edge worker.
*   **Zero Dependencies** – Pure TypeScript running on Cloudflare Workers. No npm dependencies or build chains.
*   **Fleet Native** – Implements the open Cocapn agent protocol, compatible with other fleet vessels.

---

## How it's Different
*   No accounts, logins, or subscriptions.
*   Fork-first design. You are meant to clone and modify the logic for your needs.
*   Bring-your-own-key (BYOK) for AI models and data sources.
*   Deploys as a stateless edge function, costing very little to host.

**One Current Limitation:** Nutrition analysis is currently English-language only.

---

## Quick Start
Test the public agent at the Live URL above.

To run your own instance:
1.  Fork this repository.
2.  Deploy it to Cloudflare Workers.
3.  Modify `worker.ts` to adjust the agent's behavior or add custom rules.

---

## Fleet Endpoints
This vessel implements the standard Cocapn Fleet BYOK interface:
*   `/api/seed` – Initialize personal profiles.
*   `/api/efficiency` – Analyze meal nutrient density.
*   `/api/confidence` – Track dietary adherence.
*   `/api/evaporation` – Configure automated data retention.
*   `/api/memory` – Private meal history storage.
*   `/api/kg` – Personal food knowledge graph operations.

---

## Contributing
This is a fork-first project. Clone it, customize it, and run it privately. If you build a useful modification, you are encouraged to share it back.

---

## License
MIT License · Superinstance & Lucineer (DiGennaro et al.)

---

<div align="center">
  <a href="https://the-fleet.casey-digennaro.workers.dev">The Fleet</a> · 
  <a href="https://cocapn.ai">Cocapn</a>
</div>