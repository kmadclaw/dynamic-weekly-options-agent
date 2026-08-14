# Dynamic Weekly Options Agent

A shareable GitHub Pages brief for Krish's dynamic weekly options trading agent.

Live page: https://kmadclaw.github.io/dynamic-weekly-options-agent/

## What it covers

- Daily post-open workflow
- 68-symbol liquid options universe
- Technical scoring inputs
- Alpaca data/execution sources
- Entry filters for weekly contracts under $1
- Risk controls, autonomy model, and status rules
- Autonomous profit booking and stop/risk sell-to-close rules
- Exact-contract wash-sale guard

## Notes

This page is an operational overview only. It does not include API keys, account identifiers, or secret configuration.


## Current autonomy model

As of 2026-08-14, Krish authorized the agent to sell without asking first when the existing strategy rules say to book profit or cut risk. Existing guardrails remain unchanged: limit orders only, one active option position/order, hard buy-side ask cap <= $1.00, no new entries during the first 30 minutes, spread/liquidity/delta filters, exact-contract re-entry block after closes, and status updates for actions taken.
