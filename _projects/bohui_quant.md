---
layout: page
title: Crude-Oil Market Data & Intelligent Investment-Research Platform
description: multi-asset market data, low-latency streaming, DAG strategy orchestration
img: assets/img/4.jpg # TODO: replace with a real dashboard / architecture screenshot
importance: 4
category: work
related_publications: false
---

Backend development for **Ningbo Bohui Chemical** (Oct 2025 – Apr 2026), building a crude-oil market data and AI quant-strategy investment-research platform.

## AI quant strategy workbench
Used **Codex** and **Claude Code** to design the workbench. Built a strategy-factor **Workflow** with **DAG visual orchestration**, ingested real-time exchange quotes, and constructed a **CTP → Kafka → ClickHouse** low-latency streaming path.

## Multi-asset market & backtest data pipeline
Integrated **FMP**, **TradingView**, a **PostgreSQL hot DB**, **OSS historical archive**, and real-time indicator services across **futures, US equities, and A-shares**. Designed a **main-site + Mac worker + OSS** architecture that decoupled compute tasks from the main pipeline.
