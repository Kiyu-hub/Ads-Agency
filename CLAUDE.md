# Claude Ads: Paid Advertising Audit & Optimization Skill

## Project Overview

This repository contains the full Claude Ads stack — 5 skill packs, 50 skills, 14 agents,
and 54+ reference files for paid advertising across Google, Meta, TikTok, YouTube, LinkedIn,
Microsoft, Apple, and Amazon. Includes the core AgriciDaniel/claude-ads Tier 4 skill (22 sub-skills,
10 agents, 250+ audit checks), plus 4 additional skill packs installed on 2026-06-17:
krusemediallc/arcads-claude-code (UGC video + image ads), Hainrixz/claude-ads (onboarding wizard +
social publishing), mathiaschu/meta-ads-analyzer (Breakdown Effect framework), TheMattBerman/meta-ads-kit
(daily Meta monitoring loop), and zubair-trabzada/ai-ads-claude (video scripts, hooks, funnel architecture).

## Installed Skill Packs

### Pack 1: AgriciDaniel/claude-ads (core)
22 sub-skills, 10 agents, 250+ checks, 26 references

```
ads/SKILL.md                       # Main orchestrator
ads/references/ (26 files)         # Benchmarks, specs, audit guides
ads-audit, ads-google, ads-meta, ads-youtube, ads-linkedin, ads-tiktok
ads-microsoft, ads-apple, ads-amazon, ads-attribution, ads-server-side-tracking
ads-creative, ads-landing, ads-budget, ads-plan, ads-competitor, ads-math
ads-test, ads-dna, ads-create, ads-generate, ads-photoshoot
Agents: audit-google, audit-meta, audit-creative, audit-tracking, audit-budget,
        audit-compliance, creative-strategist, visual-designer, copy-writer, format-adapter
```

### Pack 2: krusemediallc/arcads-claude-code (UGC video + image ads)
5 skills for AI video/image creative via Arcads API (Seedance 2, Sora 2, Veo 3.1)
Requires: `ARCADS_API_KEY` in `.env`

```
arcads-external-api/SKILL.md      # Seedance, Sora2, Veo, Kling, UGC video
chatgpt-image-ad/SKILL.md         # GPT-image-2 static ads (text-heavy, UI-mimicry)
nano-banana-image-ad/SKILL.md     # Gemini/Nano Banana ads (photoreal, lifestyle)
image-ad-clone/SKILL.md           # Reverse-engineer existing ads into templates
generate-youtube-thumbnail/SKILL.md # High-CTR YouTube thumbnails
Shared: 37-template prompt library, meta-ad-builder deploy scripts
```

### Pack 3: Hainrixz/claude-ads (onboarding wizard + social publishing)
4 new sub-skills + 29 new reference files + 4 new scripts

```
ads-start/SKILL.md                # First-run wizard (context, OAuth, profile.json)
ads-next/SKILL.md                 # Continuous coach (Quick Wins ranking)
ads-update/SKILL.md               # Refresh references with 30-day platform changes
ads-publish/SKILL.md              # Publish creatives to 14+ networks via Zernio
New refs: benchmarks-cross, bidding-google/meta/tiktok, setup-meta/google/tiktok,
          tracking-cross/meta/google/tiktok, changelog-30d files (3 platforms)
New scripts: profile.py, zernio_publish.py, run_update.py, ads_sources.py
```

### Pack 4: mathiaschu/meta-ads-analyzer (Breakdown Effect framework)
1 expert skill + 9 official Meta reference docs

```
meta-ads-analyzer/SKILL.md        # Expert Meta diagnosis; Breakdown Effect lens
meta-ads-analyzer/references/
  breakdown_effect.md             # The Breakdown Effect (read first)
  learning_phase.md               # ~50 optimization events needed
  ad_relevance_diagnostics.md     # Quality/Engagement/Conversion rankings
  auction_overlap.md, pacing.md, bid_strategies.md, ad_auctions.md
  core_concepts.md, performance_fluctuations.md
```

### Pack 5: TheMattBerman/meta-ads-kit (daily Meta monitoring loop)
5 skills + meta-ads-copilot agent

```
meta-ads/SKILL.md                 # Daily checks: bleeders, winners, fatigue
ad-creative-monitor/SKILL.md      # CTR decay, frequency creep tracking
budget-optimizer/SKILL.md         # Spend efficiency, budget shift recommendations
ad-copy-generator/SKILL.md        # Copy matched to specific creatives
ad-upload/SKILL.md                # Upload with dry-run guardrails
Agent: meta-ads-copilot.md        # Orchestrates all 5 for daily workflow
```

### Pack 6: zubair-trabzada/ai-ads-claude (video scripts + funnel architecture)
11 new sub-skills + 3 new agents

```
ads-strategy/SKILL.md             # 5-agent full strategy (Ad Readiness Score 0-100)
ads-quick/SKILL.md                # 60-second ad readiness snapshot
ads-video/SKILL.md                # 15s/30s/60s video scripts with shot-by-shot
ads-hooks/SKILL.md                # 20 scroll-stopping hooks by psychological angle
ads-funnel/SKILL.md               # TOFU→MOFU→BOFU→Retargeting architecture
ads-copy/SKILL.md                 # 10+ copy variations (PAS, AIDA, BAB, 4Ps)
ads-keywords/SKILL.md             # Google keyword strategy with match types
ads-audience/SKILL.md             # 5-7 audience personas with targeting params
ads-competitors/SKILL.md          # Competitor ad intelligence + swipe file
ads-testing/SKILL.md              # A/B test roadmap with 90-day calendar
ads-report-pdf/SKILL.md           # Professional PDF report generation
Agents: ads-audience.md, ads-competitive.md, ads-funnel.md
```

## Full Command Reference (50 skills)

### Core Ads Commands
| Command | Purpose |
|---------|---------|
| `/ads start` | First-run wizard — context, OAuth, profile.json setup |
| `/ads next` | Continuous coach — rank Quick Wins after each audit |
| `/ads audit` | Full multi-platform audit (6 parallel agents) |
| `/ads google` | Google Ads deep analysis (incl. AI Max) |
| `/ads meta` | Meta/Facebook Ads analysis (Andromeda + GEM + Lattice) |
| `/ads youtube` | YouTube Ads analysis |
| `/ads linkedin` | LinkedIn Ads analysis |
| `/ads tiktok` | TikTok Ads analysis |
| `/ads microsoft` | Microsoft/Bing Ads analysis |
| `/ads apple` | Apple Ads (AdAttributionKit, dual attribution) |
| `/ads amazon` | Amazon Ads (ACOS/TACOS, Sponsored Products/Brands/Display) |
| `/ads attribution` | Cross-platform attribution audit (AAK, GA4, Consent Mode V2) |
| `/ads tracking` | Server-side tracking audit (sGTM, CAPI Gateway, dedup) |
| `/ads creative` | Creative quality and fatigue assessment |
| `/ads landing` | Landing page conversion analysis |
| `/ads budget` | Budget allocation optimization |
| `/ads plan <type>` | Strategic ad planning by industry |
| `/ads competitor` | Competitor ad research |
| `/ads math` | PPC financial calculator (CPA, ROAS, break-even, LTV:CAC) |
| `/ads test` | A/B test design (hypothesis, significance, sample size) |
| `/ads report` | PDF audit report generation for client deliverables |
| `/ads dna <url>` | Extract brand DNA from website → `brand-profile.json` |
| `/ads create` | Generate campaign concepts + copy briefs → `campaign-brief.md` |
| `/ads generate` | Generate AI ad images from brief → `ad-assets/` |
| `/ads photoshoot` | Product photography in 5 styles |
| `/ads update <platform>` | Refresh references with last 30 days of platform changes |
| `/ads publish` | Publish creatives to 14+ social networks via Zernio |

### Strategy & Analysis Commands (ai-ads-claude pack)
| Command | Purpose |
|---------|---------|
| `/ads strategy <url>` | 5-agent full strategy + Ad Readiness Score 0–100 |
| `/ads quick <url>` | 60-second ad readiness snapshot |
| `/ads audience <url>` | 5–7 audience personas with targeting parameters |
| `/ads competitors <url>` | Competitor ad intelligence + swipe file |
| `/ads copy <platform>` | 10+ copy variations (PAS, AIDA, BAB, 4Ps) |
| `/ads hooks` | 20 scroll-stopping hooks by psychological angle |
| `/ads video <product>` | 15s/30s/60s video scripts with shot-by-shot direction |
| `/ads funnel <url>` | TOFU→MOFU→BOFU→Retargeting architecture |
| `/ads keywords` | Google keyword strategy with match types + ad groups |
| `/ads testing <campaign>` | A/B testing roadmap with 90-day calendar |
| `/ads report-pdf` | Professional PDF strategy report |

### Arcads Creative Commands (krusemediallc/arcads pack)
| Command | Purpose |
|---------|---------|
| `arcads-external-api` skill | UGC video via Seedance 2, Sora 2, Veo 3.1, Kling |
| `chatgpt-image-ad` skill | GPT-image-2 static ads (text-heavy, UI-mimicry style) |
| `nano-banana-image-ad` skill | Gemini/Nano Banana photoreal & lifestyle ads |
| `image-ad-clone` skill | Reverse-engineer existing ads into reusable templates |
| `generate-youtube-thumbnail` skill | High-CTR YouTube thumbnails with reference images |

### Daily Meta Management Commands (meta-ads-kit pack)
| Command | Purpose |
|---------|---------|
| `meta-ads` skill | Daily 5-question check: bleeders, winners, fatigue |
| `ad-creative-monitor` skill | CTR decay and frequency creep tracking |
| `budget-optimizer` skill | Spend efficiency + budget shift recommendations |
| `ad-copy-generator` skill | Copy matched to specific creative images |
| `ad-upload` skill | Upload ads with dry-run guardrails |
| `meta-ads-analyzer` skill | Expert diagnosis with Breakdown Effect framework |

## Development Rules

- Keep SKILL.md files under 500 lines / 5000 tokens
- Reference files should be focused; aim for under 350 lines. Split when a
  single reference exceeds that and starts mixing concerns
- Scripts must have docstrings, CLI interface, and JSON output
- Follow kebab-case naming for all skill directories
- Agents invoked via Task tool with `context: fork`, never via Bash
- No hardcoded credentials; use MCP servers for external API access

## Release Blog Post

After cutting a new release (git tag + `gh release create`), run:

```
/release-blog
```

This generates a blog post on https://agricidaniel.com/blog/, handles cover image generation, SEO metadata, FAQ schema, internal linking, sitemap/llms.txt updates, Vercel deployment, and Google indexing.
