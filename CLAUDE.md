# Claude Ads: Paid Advertising Audit & Optimization Skill

## Project Overview

This repository contains the full Claude Ads stack — 9 skill packs, 95+ skills, 15 agents,
and 55+ reference files for paid advertising across Google, Meta, TikTok, YouTube, LinkedIn,
Microsoft, Apple, and Amazon. Includes the core AgriciDaniel/claude-ads Tier 4 skill (22 sub-skills,
10 agents, 250+ audit checks), plus 8 additional skill packs installed on 2026-06-17:
krusemediallc/arcads-claude-code (UGC video + image ads), Hainrixz/claude-ads (onboarding wizard +
social publishing), mathiaschu/meta-ads-analyzer (Breakdown Effect framework), TheMattBerman/meta-ads-kit
(daily Meta monitoring loop), zubair-trabzada/ai-ads-claude (video scripts, hooks, funnel architecture),
the custom `/ads produce` full-pipeline orchestrator (brand DNA → strategy → copy → premium prompts →
visual generation → video scripts → format validation — all in one command),
nowork-studio/NotFair (2,886★ — Google Ads + Meta Ads + SEO skills via NotFair MCP),
realkimbarrett/advertising-skills (670★ — direct response copy frameworks, Schwartz method),
and pixelab-ch/higgsfield-skills (15 Higgsfield video/image generation skills).

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

### Custom: Full-Pipeline Orchestrator (built 2026-06-17)
1 master skill + 1 premium prompt-builder agent

```
ads-produce/SKILL.md              # End-to-end pipeline: DNA → strategy → copy →
                                  # premium prompts → images → video scripts →
                                  # format validation — all from one URL
Agent: ads-prompt-builder.md      # Cinematography-grade prompt construction
                                  # (9-component framework: shot type, subject,
                                  # environment, lighting, color, style, brand
                                  # cues, technical specs, negative constraints)
```

**What makes `/ads produce` different from running individual commands:**
The `ads-prompt-builder` agent combines exact brand hex colors, persona insights
from the strategy, platform-specific composition rules, and photographic
references into 150-350 word prompts that a creative director at BBDO could
hand directly to a production team — ensuring every generated image is on-brand,
on-strategy, and platform-compliant in one pipeline.

### Pack 7: nowork-studio/NotFair (2,886★ — Google Ads + Meta Ads + SEO)
17 skills, installed under `~/.claude/skills/notfair/`
Requires: Google Ads NotFair MCP (notfair.co OAuth), Meta Marketing API, Google Search Console

```
notfair/google-ads/audit/SKILL.md   # google-ads-audit: account health + context setup
notfair/google-ads/manage/SKILL.md  # google-ads: manage keywords, bids, budgets, negatives
notfair/google-ads/copy/SKILL.md    # google-ads-copy: RSA headlines/descriptions, A/B copy
notfair/google-ads/landing/SKILL.md # google-ads-landing: LPX diagnosis, message match
notfair/meta-ads/audit/SKILL.md     # meta-ads-audit: account health + Meta context setup
notfair/meta-ads/manage/SKILL.md    # meta-ads: ROAS, CPM, fatigue, overlap, learning phase
notfair/seo/seo-analysis/SKILL.md   # Full-site SEO audit, traffic drop, Core Web Vitals
notfair/seo/seo-page/SKILL.md       # URL-specific deep audit
notfair/seo/content-writer/SKILL.md # Write or improve content
notfair/seo/content-planner/SKILL.md # Editorial calendar from GSC data
notfair/seo/keyword-research/SKILL.md # Keyword discovery, topic clusters
notfair/seo/meta-tags-optimizer/SKILL.md # Title tags, meta descriptions, OG, CTR
notfair/seo/schema-markup-generator/SKILL.md # JSON-LD structured data
notfair/seo/broken-link-checker/SKILL.md # 404/site-health crawl
notfair/seo/geo-optimizer/SKILL.md  # Rank in ChatGPT/Perplexity/AI Overviews (GEO/AEO)
notfair/seo/setup-cms/SKILL.md      # WordPress, Strapi, Contentful, Ghost integration
notfair/gemini/SKILL.md             # Cross-model second opinion via Google Gemini
Shared playbooks: preamble, analysis-principles, ppc-math, ppc-optimization-patterns
```

### Pack 8: realkimbarrett/advertising-skills (670★ — Direct Response Copy Frameworks)
12 skills, all installed directly in `~/.claude/skills/`

```
# Foundations
avatar-extraction/SKILL.md          # Define exact buyer profile (pains, desires, failed attempts)
offer-extraction/SKILL.md           # Turn product/service into a high-converting offer

# Copy Chief
schwartz-awareness-mapper/SKILL.md  # Eugene Schwartz awareness levels → message match
mechanism-builder/SKILL.md          # Explain WHY your solution works (unique mechanism)
objection-crusher/SKILL.md          # Identify and neutralize buyer objections
headline-matrix/SKILL.md            # High-performing headline variations across angles

# Operator OS
ad-angle-multiplier/SKILL.md        # Expand core idea into multiple creative angles
scroll-stopping-creative/SKILL.md   # Stop attention in first 3 seconds
conversion-path-builder/SKILL.md    # Design optimal funnel: click → conversion
performance-diagnosis/SKILL.md      # Diagnose why campaigns underperform

# Orchestrators
full-funnel-campaign-orchestrator/SKILL.md # Coordinate all skills end-to-end

# QA
generic-language-killer/SKILL.md    # Remove vague/AI-sounding copy, replace with specific human language
```

### Pack 9: pixelab-ch/higgsfield-skills (15 Higgsfield Video/Image Skills)
15 skills installed as `~/.claude/skills/01-cinematic/` through `~/.claude/skills/15-real-estate/`
All use the Higgsfield MCP already connected to this session.

```
01-cinematic/SKILL.md        # Film-grade cinematic video (cinematic_studio_3_0 / veo3_1)
02-3d-cgi/SKILL.md           # 3D rendered / CGI / Pixar-style (seedance_2_0 / wan2_7)
03-cartoon/SKILL.md          # Cartoon, 2D animation, cel-shaded (wan2_7 / seedance_2_0)
04-comic-to-video/SKILL.md   # Animate comic panels / manga (wan2_6 I2V — image required)
05-fight-scenes/SKILL.md     # Fight scenes, action choreography (cinematic_studio_3_0 / kling3_0)
06-motion-design-ad/SKILL.md # SaaS/software/app motion ad (marketing_studio_video)
07-ecommerce-ad/SKILL.md     # E-commerce product ad + product stills (marketing_studio_video)
08-anime-action/SKILL.md     # Anime-style video from reference frame (wan2_7 I2V)
09-product-360/SKILL.md      # Product 360° turntable / reveal (seedance_2_0 I2V)
10-music-video/SKILL.md      # Music video prompts
11-social-hook/SKILL.md      # Viral TikTok/Reels/Shorts hooks (kling3_0 / grok_video)
12-brand-story/SKILL.md      # Brand story narrative video
13-fashion-lookbook/SKILL.md # Fashion lookbook / editorial
14-food-beverage/SKILL.md    # Food/beverage beauty shots
15-real-estate/SKILL.md      # Real estate walkthroughs / property showcases
```

## Full Command Reference (95+ skills)

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
| **`/ads produce <url>`** | **Full pipeline: DNA → strategy → copy → premium prompts → images → video scripts → format validation. One command, everything.** |

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

### NotFair Commands (nowork-studio/NotFair pack)
| Command | Purpose |
|---------|---------|
| `google-ads-audit` skill | Google Ads account health check + persistent business context |
| `google-ads` skill | Manage keywords, bids, budgets, negatives, experiments |
| `google-ads-copy` skill | RSA headlines, descriptions, A/B copy variants |
| `google-ads-landing` skill | Landing page diagnosis, ad-to-page message match |
| `meta-ads-audit` skill | Meta account health check + Meta business context |
| `meta-ads` skill (NotFair) | Facebook/Instagram performance, creative fatigue, overlap |
| `seo-analysis` skill | Full-site SEO audit, GSC analysis, Core Web Vitals |
| `seo-page` skill | URL-specific deep audit |
| `content-writer` skill | Write or improve content for SEO |
| `content-planner` skill | Editorial calendar from GSC data |
| `keyword-research` skill | Keyword discovery, topic clusters |
| `meta-tags-optimizer` skill | Title tags, meta descriptions, Open Graph, CTR |
| `schema-markup-generator` skill | JSON-LD / structured data (FAQ, Product, HowTo) |
| `broken-link-checker` skill | Broken-link / 404 / site-health crawl |
| `geo-optimizer` skill | Rank in ChatGPT / Perplexity / AI Overviews (GEO/AEO) |
| `setup-cms` skill | Connect WordPress, Strapi, Contentful, or Ghost |
| `gemini` skill | Second opinion / cross-model review via Google Gemini |

### Direct Response Copy Commands (realkimbarrett/advertising-skills pack)
| Command | Purpose |
|---------|---------|
| `avatar-extraction` skill | Define exact buyer: who they are, pains, desires, failed solutions |
| `offer-extraction` skill | Turn product/service into a compelling high-converting offer |
| `schwartz-awareness-mapper` skill | Diagnose awareness stage → correct message-to-market match |
| `mechanism-builder` skill | Build the unique mechanism explaining WHY your solution works |
| `objection-crusher` skill | Identify and neutralize every buyer objection |
| `headline-matrix` skill | Generate headline variations across multiple angles |
| `ad-angle-multiplier` skill | Expand one core idea into multiple distinct creative angles |
| `scroll-stopping-creative` skill | Ad concepts that stop attention in the first 3 seconds |
| `conversion-path-builder` skill | Design optimal funnel from ad click to conversion |
| `performance-diagnosis` skill | Diagnose why campaigns are underperforming |
| `full-funnel-campaign-orchestrator` skill | Coordinate all copy skills end-to-end |
| `generic-language-killer` skill | Remove vague/AI-sounding copy, replace with specific human language |

### Higgsfield Video/Image Commands (pixelab-ch/higgsfield-skills pack)
| Command | Purpose |
|---------|---------|
| `01-cinematic` skill | Film-grade cinematic video (dolly, crane, anamorphic, noir) |
| `02-3d-cgi` skill | 3D CGI / Pixar-style / Unreal Engine rendered video |
| `03-cartoon` skill | Cartoon, 2D animation, cel-shaded, motion graphics |
| `04-comic-to-video` skill | Animate comic panels / manga (requires source image) |
| `05-fight-scenes` skill | Fight scenes, combat, martial arts, action sequences |
| `06-motion-design-ad` skill | SaaS/app/software motion design ad |
| `07-ecommerce-ad` skill | E-commerce product ads + product stills |
| `08-anime-action` skill | Anime-style video from reference frame (I2V) |
| `09-product-360` skill | Product 360° turntable / multi-angle reveal (I2V) |
| `10-music-video` skill | Music video cinematic sequences |
| `11-social-hook` skill | Viral TikTok / Reels / YouTube Shorts hooks |
| `12-brand-story` skill | Brand story narrative video |
| `13-fashion-lookbook` skill | Fashion editorial / lookbook video |
| `14-food-beverage` skill | Food/beverage beauty shots and ads |
| `15-real-estate` skill | Real estate walkthroughs / property showcase video |

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
