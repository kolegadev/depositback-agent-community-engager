# Community Engager

> **Agent**: `depositback-agent-community-engager`  
> **Group**: Distribution  
> **Product**: DepositBack — Security Deposit Demand Letter Service

## Purpose

Joins 20-30 tenant groups, observes for 2 weeks, posts value-first answers 3-5x/week. Nextdoor business profile + hyperlocal deposit tips. Reddit/BiggerPockets soft mentions.

## DepositBack Context

DepositBack is a single-page, no-signup transactional product for US renters seeking to recover security deposits. The entire customer journey fits on one URL: landing page → 6-question form → Revolut payment → PDF emailed. Conversion rate target: **4% visitor-to-purchase minimum**.

## Inputs

- Pain signals from pain-signal-monitor
- State deadlines from geo-content-generator

## Outputs

- Engagement logs → analytics/channel-scorer inbox
- Group participation reports

## Human Escalation Points 🛑

- Group ban/removal
- Negative landlord responses
- Legal threats in comments

## Skills

| Skill | Description | Status |
|-------|-------------|--------|
| `noop` | Health check / pipeline verification | ✅ Active |
| `execute` | Primary function for this agent | 🔧 Planned |

## Workflow

1. Poll `data/inbox/` for task manifests from upstream agents.
2. Resolve required skills (local `skills/` or ClawHub fallback).
3. Execute workflow.
4. Write artifacts to `data/outbox/`.
5. Update `data/state.json`.

## Runtime

```bash
pip install -r requirements.txt
python runtime/main.py
```
