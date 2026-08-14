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
- Profit/risk alert rules with auto-exit currently disabled
- Exact-contract wash-sale guard

## Notes

This page is an operational overview only. It does not include API keys, account identifiers, or secret configuration.


## Current autonomy model

As of 2026-08-14 latest update, auto sell-to-close is disabled for now because the simple auto-exit rule needs improvement. The agent still checks at an effective 30-second cadence and sends routine status every 5 minutes, but profit/target and risk/stop triggers should emit alerts/status only rather than submit exit orders. Existing entry guardrails remain unchanged: limit orders only, one active option position/order, hard buy-side ask cap <= $1.00, no new entries during the first 30 minutes, spread/liquidity/delta filters, and exact-contract re-entry block after closes.
