---
layout: default
title: "Copying One MT5 Account to Several Accounts: A Short Checklist"
permalink: /tpcopier/
---

# Copying One MT5 Account to Several Accounts: A Short Checklist

Copying trades from one MetaTrader 5 account to others sounds simple: when the master opens a trade, the followers open the same trade. In practice, a few settings decide whether the copies match.

## Lot size per follower

Followers rarely have the same balance as the master. Pick a rule for each follower: the same lot, a multiplier, or a lot sized from the follower's own balance. Write it down before you connect a live account.

## Symbol names

One broker calls gold XAUUSD, another XAUUSD.m or GOLD. Every follower needs a symbol map, or the copy fails on the first trade in a symbol the broker names differently.

## Partial closes and stop changes

When the master closes half a position or moves the stop loss, the follower should do the same on its matching trade. Test this on demo, because many copiers only handle full opens and closes.

## Delay and slippage

Copy speed matters on fast markets. Measure the time between the master's trade and the follower's order on a demo, and check the price difference over a week of trades.

## Where it runs

A local copier needs both terminals open on one machine or VPS. A cloud copier runs the terminals on the provider's servers, so nothing stops when your computer sleeps.

I work on [TPcopier](https://tpcopier.com/mt4-mt5-cloud-trade-copier), a cloud trade copier for MT4 and MT5 accounts with per-follower lot rules and symbol maps. Whatever you use, test on demo first, because trading is risky.

[← All notes](/)
