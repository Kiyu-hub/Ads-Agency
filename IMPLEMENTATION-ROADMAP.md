# Implementation Roadmap — Clasikal Homes

## Overview

| Phase | Timeline | Goal |
|-------|----------|------|
| Foundation | Week 1–2 | Tracking + creative ready |
| Launch | Week 3–4 | Meta ASC + Google PMax live |
| Optimize | Week 5–8 | Kill underperformers, find winners |
| Scale | Week 9–12 | Scale winners, expand platforms |
| Maintain | Month 4+ | 70/20/10 framework, quarterly reviews |

---

## Phase 1: Foundation (Week 1–2)

### Tracking (Do first — no ads without this)
- [ ] Install Meta Pixel on clasikalhomes.com
- [ ] Configure standard events: PageView, ViewContent, AddToCart, Purchase
- [ ] Set up Conversions API (CAPI) — Shopify app or custom
- [ ] Test pixel with Meta Pixel Helper + Events Manager → Test Events
- [ ] Install Google Tag Manager
- [ ] Create Google Ads account + conversion actions (Purchase, AddToCart)
- [ ] Enable Enhanced Conversions in Google Ads
- [ ] Set up Google Analytics 4 + link to Google Ads
- [ ] Create Google Merchant Center account + upload product feed in GHS
- [ ] Verify Merchant Center feed: aim for 0 disapproved products
- [ ] Add UTM parameters to WhatsApp links

### Creative Production
- [ ] Produce Priority 1 assets (see CREATIVE-BRIEF.md):
  - Hero lifestyle static (1080×1080 + 1200×628)
  - 5-card product carousel (1080×1080 each)
  - Transformation Reel (1080×1920, 15s)
  - Brand/founder story static
  - Google PMax images (3 lifestyle per product category)
- [ ] Apply royal blue (#2345C8) branding to all assets
- [ ] Write Google RSA headlines (15) and descriptions (4)

### Account Setup
- [ ] Create Meta Business Manager + ad account
- [ ] Create Google Ads account (if not exists)
- [ ] Set billing in GHS or USD (based on card)
- [ ] Invite agency/collaborator access if applicable

---

## Phase 2: Launch (Week 3–4)

### Meta Launch
- [ ] Create campaign: `META_CONV_ASC_GH_202607`
  - Budget: 70% of Meta spend
  - Bidding: Lowest Cost (let it learn)
  - Upload all Priority 1 creative (5+ ads minimum)
- [ ] Create retargeting campaign: `META_CONV_Retargeting_GH_202607`
  - Budget: 20% of Meta spend
  - Audiences: website visitors 7d, add-to-cart 14d
- [ ] Leave 10% for testing campaign (launch in Week 4)
- [ ] Verify pixel fires correctly after first clicks

### Google Launch
- [ ] Submit product feed to Merchant Center — wait for approval (1–3 days)
- [ ] Create campaign: `GOOG_SHOP_PMax_CoreProducts_GH_202607`
  - Budget: 80% of Google spend
  - Asset groups: Living Room, Dining, Bedroom
  - Upload images, headlines, descriptions, logo
- [ ] Create campaign: `GOOG_BRAND_Search_GH_202607`
  - Budget: 20% of Google spend (small — just brand protection)
  - Keywords: "clasikal homes", "clasikalhomes.com"

### First 7 Days — Daily Monitoring
- Check Meta Ads Manager: are events firing? Any delivery issues?
- Check Google Merchant Center: any new disapprovals?
- Check Google Ads: impressions + clicks (conversions take longer)
- Do NOT change budgets or targeting in the first 7 days (disrupts learning)

---

## Phase 3: Optimize (Week 5–8)

### Creative Audit (Week 5)
- Kill any Meta ad with CTR < 0.8% after $20+ spend
- Kill any Meta ad with CPC > 3× average after $30+ spend
- Identify top 2–3 performing creatives — these are your "champion" ads
- Brief and produce Priority 2 assets (see CREATIVE-BRIEF.md)

### Audience Refinement (Week 6)
- If ASC is performing: increase its budget, don't over-manage it
- Create lookalike audience from early purchasers (even if small pool)
- Launch manual prospecting campaign with 2 audience sets

### Google Optimization (Week 7)
- Review PMax asset performance ratings (Excellent/Good/Low)
- Replace "Low" rated assets
- Check Search Terms report (in PMax Insights) — add negative keywords if irrelevant terms appear
- If Merchant Center shows low click volume: improve product titles (add "Ghana", "luxury", "home decor")

### TikTok Launch (Week 8)
- [ ] Install TikTok Pixel
- [ ] Create campaign: `TIKTOK_CONV_SmartPlus_GH_202607`
- [ ] Upload transformation video + POV content
- [ ] Budget: 10% of total monthly spend

---

## Phase 4: Scale (Week 9–12)

### Scale Winners
- Apply 20% Rule: if CPA < target by 10%, increase budget 20%
- Wait 5–7 days between increases
- Expand Meta ASC creative pool (aim for 15+ active ads)

### Expand to New Campaigns
- [ ] Launch: `META_CONV_Prospecting_GH_202607` (manual interest targeting)
- [ ] Launch: `GOOG_SEARCH_NonBrand_GH_202607` (high-intent keywords)
- [ ] Consider: YouTube pre-roll video (30–60s brand film)

### Build Retargeting Depth
- By now, you have enough pixel data for:
  - Video viewers (75%) retargeting
  - Purchaser lookalike (1–5%)
  - Cross-sell to past buyers

### Month 3 Review
- Calculate MER: Total Revenue ÷ Total Ad Spend (target ≥ 3.0)
- Platform-by-platform ROAS review
- Kill any campaign that hasn't hit 2.0 ROAS after 60 days
- Set quarterly budget for Month 4–6

---

## Phase 5: Maintain (Month 4+)

### Monthly Tasks
| Task | Frequency | Owner |
|------|-----------|-------|
| Creative refresh (Meta) | Every 2–4 weeks | Creative team |
| Keyword review (Google) | Monthly | Campaign manager |
| Audience expansion | Monthly | Campaign manager |
| Budget reallocation (70/20/10) | Monthly | Strategist |
| MER review | Monthly | Account owner |
| Pixel health check | Monthly | Tech |

### Quarterly Tasks
- Full creative audit + new brief
- Platform mix review (add/remove platforms based on performance)
- Seasonal planning (see BUDGET-PLAN.md)
- Landing page CRO review
- Competitor ad audit (Meta Ad Library + Google Ads Transparency)

---

## Quick-Start Checklist (Launch in 2 Weeks)

**Week 1:**
- [ ] Meta Pixel + CAPI installed and verified
- [ ] Google Tag Manager + conversion actions installed
- [ ] Google Merchant Center product feed uploaded
- [ ] Priority 1 creative assets produced (5 assets minimum)

**Week 2:**
- [ ] Meta ASC campaign built and reviewed
- [ ] Google PMax campaign built with asset groups
- [ ] Brand search campaign live
- [ ] All billing set up
- [ ] Launch approved → go live

**First milestone:** 50 Meta purchases/week unlocks algorithmic optimization. Everything before that is data collection.
