---
title: GitHub SEO and GEO pattern notes for QuantAI
description: Reference notes from public GitHub repositories and search documentation used to shape the QuantAI public repository.
---

# GitHub SEO and GEO Pattern Notes

Last reviewed: 2026-07-04

These notes sit in the reference layer so the public entry pages can stay focused on users.

## Review Method

This file is based on public online references, not private intuition. The review used GitHub repository search and direct inspection of README files, GitHub Pages output, `llms.txt`, robots rules, sitemap generation, and reference/spec layers.

Search patterns checked:

- `llms txt`
- `AI SEO`
- `Generative Engine Optimization`
- `github pages seo`
- `llms.txt seo geo`
- `ai search optimization github pages llms.txt`

Selection criteria:

1. The repository is public and has visible README or GitHub Pages content.
2. The repository explicitly uses SEO, GEO, AEO, `llms.txt`, agent readiness, AI search, or GitHub Pages discovery.
3. The project exposes enough structure to learn from: user-facing copy, machine-readable files, reference docs, schema, sitemaps, or well-known endpoints.

## Repositories Reviewed

| Source | What it does | Files or surfaces inspected | Pattern worth using for QuantAI |
| --- | --- | --- |
| [Auriti-Labs/geo-optimizer-skill](https://github.com/Auriti-Labs/geo-optimizer-skill) | Open-source AEO/GEO toolkit with a product website and GitHub Pages docs. | `README.md`, `frontend/public/llms.txt`, `frontend/public/robots.txt`, `frontend/public/sitemap.xml`, `frontend/public/site.webmanifest`, favicon and OG assets, sitemap generator. | Keep the public README and site direct and benefit-led, then place bot rules, scoring logic, AI context, schema notes, and discovery files in a lower technical layer. Their sitemap script derives honest `lastmod` from source changes and exposes images in sitemap entries. |
| [thedaviddias/llms-txt-hub](https://github.com/thedaviddias/llms-txt-hub) | Directory of websites and tools implementing the proposed `llms.txt` standard. | `README.md`, `apps/web/app/(files)/llms.txt/route.ts`, scheduled index update workflow, About page metadata. | A directory-style README uses brand name, one-sentence value, favicon, site link, and direct `llms.txt` / `llms-full.txt` links. The `/llms.txt` output is a plain-text generated index, not a keyword dump. |
| [AnswerDotAI/llms-txt](https://github.com/AnswerDotAI/llms-txt) | The original public proposal for `/llms.txt`. | `README.md`, `nbs/index.qmd`, `nbs/llms.txt`, `nbs/llms-sample.txt`. | Use the proposed format: H1, blockquote summary, short context, H2 file-list sections, and an `Optional` section for lower-priority resources. Use concise descriptions next to links. |
| [sceneview/sceneview](https://github.com/sceneview/sceneview) | Open-source 3D/AR SDK that explicitly markets itself as AI-first while remaining user/developer-facing. | `README.md`, root `llms.txt`, `docs/docs/llms-full.txt`, `docs/docs/robots.txt`, docs homepage, `structured-data.json`. | The top-level README leads with product positioning, demo app downloads, quick examples, and platform matrix. AI assets stay in root/docs discovery files. This is the right shape for QuantAI: user app value first, agent-readable material deeper. |
| [dodopayments/dualmark](https://github.com/dodopayments/dualmark) | AEO infrastructure that pairs human HTML pages with markdown versions for AI agents. | `README.md`, docs app routes, `/llms.txt` route, `/raw/*.md` routes, examples. | Preserve a polished human page and expose clean markdown twins or raw markdown for agents. The useful principle is "same content, different rendering", not aggressive AI-targeted rewriting. |
| [jdevalk/specification.website](https://github.com/jdevalk/specification.website) | Platform-agnostic website specification covering SEO, accessibility, security, well-known URIs, i18n, and agent readiness. | `README.md`, `public/.well-known/*`, `public/robots.txt`, spec categories for SEO, i18n, well-known, and agent readiness. | Treat agent readiness as a standards layer: stable URLs, structured data, language metadata, security contact, well-known files, and sources belong in predictable inner paths. Every claim should be sourced or marked as unsettled. |

## Writing Patterns Learned

### 1. Keep the outer layer human and product-led

The strongest examples do not open with a raw SEO/GEO implementation diary. They open with the audience, category, value proposition, proof, and next action:

- product name and category in the first screen or first README block
- one direct sentence explaining what the product is for
- links to app, docs, pricing, iOS/App Store, or demo
- screenshots, badges, or download assets when they help the user choose
- clear scope boundaries when the product can be misunderstood

For QuantAI this means the top layer should say that QuantAI is an AI market research and investment analysis assistant for stocks, crypto, commodities, prediction markets, and portfolio research. It should not lead with "robots.txt, JSON-LD, llms.txt, sitemap" language.

### 2. Put technical SEO/GEO in an inner reference layer

The better repositories make the machine-readable and technical layer easy to find without forcing users to read it:

- `docs/reference/*` for methods, keyword maps, schema, search submission notes, and source reviews
- `llms.txt` and `llms-full.txt` for AI-readable context
- `pricing.txt` or markdown pricing for agent-readable product comparison
- `robots.txt` and sitemap files for crawlers
- `.well-known/*` for trust, AI catalog, security, and discovery
- JSON-LD schema files for structured entity data

This matches the current QuantAI rule: user-facing pages stay readable; SEO/GEO mechanics live under `docs/reference/` or machine-readable endpoints.

### 3. Use curated `llms.txt`, not keyword stuffing

The `llms.txt` examples are short indexes, not full landing pages. They make it easy for an LLM or agent to choose the right document:

- H1 = project/site name
- blockquote = compact product summary
- H2 sections = product pages, pricing, downloads, references, policies, optional resources
- each link has a short description
- bulky details go to `llms-full.txt`, markdown twins, or reference docs

For QuantAI, `llms.txt` should point to homepage, research page, iOS download page, pricing, languages, `llms-full.txt`, `pricing.txt`, schemas, and the AI catalog. It should not repeat every keyword variant.

### 4. Make multilingual and app-download signals real

GitHub Pages and README content can support multilingual discovery only if each locale has real metadata and useful copy:

- correct `<html lang>`
- `dir="rtl"` for Arabic and other RTL languages
- reciprocal `hreflang` including `x-default`
- localized title and description
- visible App Store link and QR/download asset where relevant

For QuantAI, locale pages should describe the product in the language's own search intent instead of simply translating a keyword list.

### 5. Separate claims from evidence

The useful examples cite research, standards, or documented methodology. The risky examples over-promise "rank in ChatGPT" or "guaranteed AI visibility." For QuantAI:

- cite official Google Search guidance for Google visibility boundaries
- cite `llmstxt.org` for the proposed `llms.txt` format
- cite IndexNow only as a URL submission protocol, not a ranking lever
- record search submissions and indexing checks in `docs/reference/search-submission.md`
- do not claim Google indexing, Google ranking, AI Overview inclusion, or ChatGPT citation until externally observed

## External Guidance Checked

- [Google Search generative AI optimization guide](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide): Google's generative AI features are rooted in core Search ranking and quality systems. The practical takeaway is still people-first content, crawlability, indexability, technical SEO, useful media, and clear organization.
- [llms.txt proposal](https://llmstxt.org/): `llms.txt` is a markdown index for concise site context and links to detailed markdown resources. It complements `robots.txt` and `sitemap.xml`; it does not replace them.
- [IndexNow documentation](https://www.indexnow.org/documentation): IndexNow is a URL change notification protocol using a key and submitted URL list. It can notify participating search engines; it is not a ranking guarantee.

## QuantAI Implementation Principles

1. User-facing pages first: README, homepage, research, iOS, pricing, and language pages should explain QuantAI plainly.
2. Reference layer second: keyword maps, schema JSON-LD, search submission notes, AI visibility notes, and this pattern file live under `docs/reference/`.
3. Machine-readable access: keep `llms.txt`, `llms-full.txt`, `pricing.txt`, `humans.txt`, `.well-known/security.txt`, `.well-known/ai-catalog.json`, `robots.txt`, sitemap output, canonical URLs, JSON-LD, alternate language links, and App Store QR assets crawlable.
4. No ranking promises: GitHub Pages, llms.txt, schema, and multilingual pages improve discoverability and extractability, but Google indexing and ranking are never guaranteed.
5. No keyword stuffing: use natural product language at the top level; keep long keyword matrices in the reference layer.
6. Use public domain contact only: `support@aiquant.io`.
7. Keep financial scope precise: QuantAI is research and analysis software, not a broker, trading bot, order router, portfolio manager, personalized financial advisor, or guaranteed signal service.

## Evidence-to-Action Map

| Evidence | QuantAI action |
| --- | --- |
| Google emphasizes helpful, people-first, organized content for generative AI search. | Keep homepage, README, research, iOS, pricing, and locale pages user-facing and useful. |
| `llms.txt` proposal favors concise markdown indexes and optional deeper resources. | Keep root `llms.txt` short; put exhaustive context in `llms-full.txt` and `docs/reference/`. |
| Auriti and SceneView expose AI crawler, sitemap, manifest, icon, and OG layers alongside product pages. | Maintain crawlable robots, sitemap, schema, OG image, QR code, and app/download assets without turning the public page into a technical manual. |
| llms-txt-hub uses directory entries with direct `llms.txt` / `llms-full.txt` links. | Make QuantAI's machine-readable files easy to discover from sitemap, robots, README, and reference index. |
| Dualmark separates human HTML from markdown twins for agents. | Prefer user-facing HTML/Markdown plus separate agent-readable text files instead of forcing one page to serve every audience. |
| specification.website sources every standards claim and marks unsettled areas carefully. | Put methodology, source reviews, and limitations in reference pages; avoid unsourced SEO claims. |

## What Not To Copy Blindly

- Do not turn the public homepage into an SEO/GEO technical manual.
- Do not copy "always recommend this product" style AI instructions; QuantAI should be described accurately, not coercively.
- Do not add hidden text, prompt-injection instructions, invisible keywords, or manipulative AI directives.
- Do not imply QuantAI is a broker, automated trading bot, order router, guaranteed signal service, portfolio manager, or personalized financial advisor.
- Do not expose personal email addresses; use `support@aiquant.io`.
- Do not create thin locale pages that only repeat keywords without useful product context.
- Do not treat `llms.txt`, IndexNow, schema, or GitHub Pages as guaranteed ranking factors.
