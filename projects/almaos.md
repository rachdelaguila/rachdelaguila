# AlmaOS | AI Chief of Staff Prototype

**Independent project | Privacy-first, context-aware wellness planning**

AlmaOS is a personal AI Chief of Staff prototype exploring how health and calendar context can inform a realistic daily plan. The goal is to reduce the effort of coordinating schedules, routines, and recovery without exposing sensitive personal data.

## Problem and product approach

Health and calendar information often live in separate systems. AlmaOS brings relevant signals together so that a planning workflow can consider schedule constraints and wellness context, surface a daily brief, and allow a person to review or adjust suggested actions.

## Technical work

The private project uses a Cloudflare Workers application with health-data ingestion and server-side calendar synchronization. Its architecture includes D1 for structured records, R2 for raw archival, Workers AI embeddings and Vectorize for semantic retrieval, authenticated app APIs, and test/validation workflows.

Work on the project spans API integrations, data normalization, storage and retrieval design, product UX, reliability, and privacy controls.

## Current status and validation

A local prototype has been demonstrated and its core planning flow has been checked with automated and browser-based tests. The demonstrated planning flow includes deterministic/rules-based logic. **An autonomous, LLM-powered Chief of Staff is a direction of development, not a claim of production deployment.**

## Product and engineering decisions

- **Privacy by design:** Keep real health records, schedules, identifiers, and secrets out of public material.
- **Human review:** Treat wellness planning as decision support rather than medical advice or unsupervised action.
- **Testable behavior:** Separate synthetic demo examples from private data and distinguish prototype validation from production performance.
- **Reliable data flow:** Use normalized source records and a derived retrieval index rather than treating vector search as the source of truth.

## Live web preview

[Open the AlmaOS prototype preview](https://rach-del-aguila-wellness-sync.vercel.app/). This is an early, personal-use Vercel interface; it may not reflect the latest private implementation or use wholly synthetic data. Do not treat it as a validated production deployment or a public demonstration of autonomous LLM capabilities.

## What is public

This is a **sanitized project case study**, not the application source code. The source repository remains private because it contains personal-context material. New public examples and demos should use fictional fixtures only.

[Back to GitHub profile](../README.md) | [Portfolio website source](https://github.com/rachdelaguila/rachdelaguila.github.io)
