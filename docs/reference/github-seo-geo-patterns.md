---
title: GitHub SEO and GEO pattern notes for QuantAI
description: Reference notes from public GitHub repositories and search documentation used to shape the QuantAI public repository.
---

# GitHub SEO and GEO Pattern Notes

Last reviewed: 2026-07-04

These notes sit in the reference layer so the public entry pages can stay focused on users.

## Repositories Reviewed

| Source | What it does | Pattern worth using for QuantAI |
| --- | --- | --- |
| [Auriti-Labs/geo-optimizer-skill](https://github.com/Auriti-Labs/geo-optimizer-skill) | Open-source AEO/GEO toolkit with docs, references, AI context files, and llms.txt output. | Keep README and public pages direct, then place bot lists, schema notes, scoring logic, and AI-context files in docs or reference folders. |
| [thedaviddias/llms-txt-hub](https://github.com/thedaviddias/llms-txt-hub) | Directory of projects that publish AI-ready documentation and llms.txt files. | Use a curated llms.txt with concise links instead of trying to make every page a keyword dump. |
| [dodopayments/dualmark](https://github.com/dodopayments/dualmark) | AEO infrastructure that pairs human HTML pages with markdown versions for AI agents. | Preserve a human-first page, then expose clean markdown and raw reference material for agents. |
| [jdevalk/specification.website](https://github.com/jdevalk/specification.website) | Website specification covering SEO, accessibility, security, well-known URIs, i18n, and agent readiness. | Treat agent readiness as a standards layer: stable URLs, structured data, language metadata, and well-known files belong in predictable inner paths. |

## External Guidance Checked

- [Google Search generative AI optimization guide](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide): Google says generative AI visibility still depends on core Search systems, crawlability, indexing eligibility, snippets, and helpful content. It also warns that indexing and serving are not guaranteed.
- [llms.txt proposal](https://llmstxt.org/): llms.txt is a markdown index for helping LLMs find concise site context and detailed markdown resources. It complements robots.txt and sitemap.xml; it does not replace them.

## QuantAI Implementation Principles

1. User-facing pages first: README, homepage, research, iOS, pricing, and language pages should explain QuantAI plainly.
2. Reference layer second: keyword maps, schema JSON-LD, search submission notes, AI visibility notes, and this pattern file live under `docs/reference/`.
3. Machine-readable access: keep `llms.txt`, `llms-full.txt`, `pricing.txt`, `humans.txt`, `.well-known/security.txt`, `.well-known/ai-catalog.json`, `robots.txt`, sitemap output, canonical URLs, JSON-LD, alternate language links, and App Store QR assets crawlable.
4. No ranking promises: GitHub Pages, llms.txt, schema, and multilingual pages improve discoverability and extractability, but Google indexing and ranking are never guaranteed.
5. No keyword stuffing: use natural product language at the top level; keep long keyword matrices in the reference layer.

## What Not To Copy Blindly

- Do not turn the public homepage into an SEO/GEO technical manual.
- Do not imply QuantAI is a broker, automated trading bot, order router, guaranteed signal service, portfolio manager, or personalized financial advisor.
- Do not expose personal email addresses; use `support@aiquant.io`.
- Do not create thin locale pages that only repeat keywords without useful product context.
