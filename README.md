# FoodLog.ai

You don't hate tracking your food. You hate the taps, dropdowns, and serving size math other apps require.

This is a private AI food logger you run yourself. No accounts. No data lock-in. A BYOK agent vessel running as part of the Cocapn Fleet.

**Live Demo:** https://foodlog-ai.casey-digennaro.workers.dev

---

## How it Works
Existing food loggers often work for their business model, not you. This is an agent you control. You describe meals in plain language, and it stores the entries privately on your own infrastructure.

## What it Does
*   **Natural Language Logging** – Type what you ate in your own words.
*   **Private Edge Storage** – Your meal history stays on the Cloudflare Worker you deploy. It is not sent elsewhere.
*   **Nutrition Estimates** – Provides rough macro estimates. It is not a precise calorie calculator.
*   **Fleet Compatible** – Uses the Cocapn Fleet protocol. Can connect to other fleet agents.
*   **Zero Dependencies** – One TypeScript file. No npm install or build step.
*   **Low-Cost Hosting** – Runs on Cloudflare Workers, often within the free tier.

**An Honest Limitation:** The nutrition estimates are based on general food data. For strict dietary tracking requiring lab-grade precision, this is not the right tool.

## Quick Start
1.  Fork this repository.
2.  Deploy it to Cloudflare Workers.
That's it. The code runs as-is.

## Customize It
This is a template. Add your own LLM API key. Modify `worker.ts` for your diet rules or to change how meals are processed. It's built to be edited.

## Philosophy
This is not a service. You run your own copy.
*   **Fork-First:** You don't request features; you build them directly into your fork.
*   **No Lock-In:** Export all data as JSON anytime.
*   **No Fluff:** No gamification, badges, or email reminders.

---

MIT License · Superinstance & Lucineer (DiGennaro et al.)

---

<div align="center">
  <a href="https://the-fleet.casey-digennaro.workers.dev">The Fleet</a> · 
  <a href="https://cocapn.ai">Cocapn</a>
</div>