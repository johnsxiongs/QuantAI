---
title: QuantAI AI visibility reference
description: Inner technical reference for QuantAI AI search, GEO, llms.txt, structured data, and search monitoring.
---

# QuantAI AI Visibility Reference

This is an inner reference file for search and AI visibility work. It is not the main product page.

Last updated: 2026-07-04

## Evidence From Public Examples

The current structure follows patterns observed in public GitHub and web examples:

- User-facing README and homepage pages explain the product first, then offer clear calls to action.
- Technical SEO, GEO, `llms.txt`, structured data, and conformance materials live in docs, spec, reference, or machine-readable files.
- `llms.txt` files summarize the product, link to key pages, and avoid replacing the public homepage.
- Markdown twins or reference pages help AI agents read content without turning the human page into a technical manual.

Reviewed examples:

- [Auriti-Labs/geo-optimizer-skill](https://github.com/Auriti-Labs/geo-optimizer-skill)
- [thedaviddias/llms-txt-hub](https://github.com/thedaviddias/llms-txt-hub)
- [dodopayments/dualmark](https://github.com/dodopayments/dualmark)
- [jdevalk/specification.website](https://github.com/jdevalk/specification.website)
- [hqhq1025/skill-optimizer](https://github.com/hqhq1025/skill-optimizer)
- [Pagesmith llms.txt](https://pagesmith.ai/llms.txt)
- [Taskade llms.txt](https://www.taskade.com/llms.txt)
- [SignalPM llms.txt](https://signalpm.online/llms.txt)

## Current Architecture

User-facing pages:

- `/` product overview
- `/research.html` market research guide
- `/ios.html` iOS download page
- `/pricing.html` pricing overview
- `/languages.html` language entry page
- `/locales/*.html` localized product pages

Reference and machine-readable pages:

- `/llms.txt`
- `/llms-full.txt`
- `/pricing.txt`
- `/humans.txt`
- `/.well-known/security.txt`
- `/.well-known/ai-catalog.json`
- `/reference/agent-summary.html`
- `/reference/keyword-map.html`
- `/reference/ai-visibility.html`
- `/reference/search-submission.html`
- `/reference/schema/*.jsonld`

## Query Clusters

Primary product queries:

- QuantAI
- Quant AI
- aiquant
- aiquant.io
- Quant AI app
- QuantAI iOS

Research category queries:

- AI investment research assistant
- AI stock research assistant
- AI crypto analysis tool
- AI market research assistant
- AI technical analysis tool
- AI fundamental analysis tool
- AI quant trading research assistant

Responsible boundary queries:

- AI investment research software
- AI market research app
- AI stock analysis research assistant
- AI crypto research assistant

Avoid as primary claims:

- automated trading bot
- guaranteed signal service
- broker
- personalized financial advisor

## Technical Checks

- Public pages must be crawlable and indexable.
- The home page should keep user copy above technical copy.
- `robots.txt` should point to the public sitemap and agent sitemap.
- Sitemap should include user-facing pages and reference pages.
- JSON-LD should parse as valid JSON.
- `llms.txt` should link to the main product, iOS, pricing, languages, and reference files.
- Public content should use `support@aiquant.io` only.

## Monitoring Queries

Monthly manual checks:

- `site:johnsxiongs.github.io/QuantAI QuantAI`
- `site:github.com/johnsxiongs/QuantAI QuantAI`
- `QuantAI AI investment research assistant`
- `Quant AI stock research assistant`
- `QuantAI iOS`
- `aiquant.io QuantAI`

AI answer checks:

- What is QuantAI?
- What is an AI investment research assistant?
- What apps help research stocks and crypto with AI?
- Is QuantAI a trading bot?
- Where can I download QuantAI for iOS?
